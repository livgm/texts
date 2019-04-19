# The importance of not writing raw sql


```sql
SELECT birthday FROM users WHERE username = %{user.name} AND password=%{user.password};
```
:tada:
