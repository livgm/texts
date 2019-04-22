
![Image1](https://imgs.xkcd.com/comics/exploits_of_a_mom.png)
# Why you should NOT use raw SQL queries
## Introduction
This short blog post will explain why you should not use raw [SQL](https://www.w3schools.com/whatis/whatis_sql.asp) queries in a server by showing how easy a SQL injection attack is. It assumes very basic understanding of both web servers and SQL commands but it does not assume any previous experience with cybersecurity. In our example we are trying to get the birthday(and later, more information) from a random person in a database.
## The problem
SQL injections are a way to insert possibly malicious SQL code into a website which gives the person performing them access to a part of the database they were not supposed to be able to access. </br> This could be a possible SQL query:
```sql
SELECT birthday FROM users WHERE username = '' + name + '' AND password= '' + password + '';
```
This does not check for valid username and password input in a field and is therefore not sufficiently protected against breaches. if we tried to enter ```sampleuser ``` as a username and ```helloworld``` as a password, it should display ```sampleuser```'s birthday. Let's assume that we have knowledge of the column names and the table name.</br> But if we entered something in the username and password box that contained special characters reserved in SQL, it would break our SQL string and render it incapable of performing what we expect it to perform. Let's try to enter something that would break the query! Special characters in SQL that are useful for us are the single quote, three dashes and the semicolon. A single quote ```'``` would automatically end the input at whichever point we insert it, the three dashes ```---``` create a comment, therefore commenting out the rest of the query, and the semicolon ```;``` ends the query allowing us to write the next, independent query. </br> </br>
If we wanted to access a part of the database we are not supposed to able to access, we could simply manipulate the query by entering characters that modify the actual <b> SQL </b> query. If we enter
```sql
1' = '1'; ---'
```
into the username field, it would break the SQL query because we ended the username field with the single quote. It also ends with a semicolon, signifying the end of the query and commenting out the rest of the code, making the compiler ignore it. Our query now says:
```sql
SELECT birthday FROM users WHERE username =  '1' = '1';--- '' AND password= '' + password + '';
```
'1' = '1' is always going to be true, so our query will select the birthday from all users where the username exists and we have successfully gotten information from the database we were not supposed to be able to access. We can also simply append another query that would give us back everything like this:
```sql
SELECT birthday FROM users WHERE username = '1' = '1'; SELECT * FROM users; --Liv AND password= helloworld;
```
</br> Obviously manipulating the SQL query is a huge security concern so we need to find a way to prevent people from being able to do this on a website of ours.

## The solution

We have already identified that directly inserting usernames and passwords into our query is potentially dangerous. So we need to think of a way to prevent this from happening. A better way to write our query is using something called <b> Prepared Statements </b>. </br> The way prepared statements work is by creating a template for the request that is compiled and stored. Later on, the values are inserted where the ```?``` in the original query used to be. This is particularly safe as it performs the query in two steps and the parameters, which are inserted later, use a different protocol. Prepared statements or equivalent ideas exist in most common programming languages and are also, due to their compiled nature, faster.
```sql
SELECT birthday FROM users WHERE username = ? AND password= ?;
```
Another solution is to use a <b> query builder </b> such as knex for node.js. These give you the opportunity to build a query without knowing the exact syntax as well as filtering the input, making it safer than using raw SQL.


## Sources and Resources
Comic: https://xkcd.com/327/ </br>
https://www.hacksplaining.com/exercises/sql-injection </br>
https://www.youtube.com/watch?v=ciNHn38EyRc



:tada:
