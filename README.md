# The importance of not writing raw sql


```sql
SELECT birthday FROM users WHERE username = %{user.name} AND password=%{user.password};
```

```sql
SELECT birthday FROM users WHERE username = Liv AND password= helloworld;
```
```sql
SELECT birthday FROM users WHERE username = ""; SELECT * FROM users; --Liv AND password= helloworld;
```

:tada:
