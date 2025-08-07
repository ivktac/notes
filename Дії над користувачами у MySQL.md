---
created: 2025-08-06
title: Дії над користувачами у MySQL
tags:
  - mysql
  - pam
aliases: 
lang: uk
---
## Створення користувача

```sql
CREATE USER 'name_user'@'host' IDENTIFIED BY 'password';
```

> [!tip]
> За допомогою символа `%` можна гнучко вказувати хости. Наприклад:
> - `192.168.0.%` — будь-яка адреса в підмережі
> - `%.mydomain.com` — будь-який піддомен
> - `%` — з будь-якого місця

## Переглянути користувача

```sql
SELECT User, Host FROM mysql.user;
```

> [!info] Або конкретний: `SELECT * FROM mysql.user WHERE Host='localhost' AND User='root'\G`

## Видалити користувача

```sql
DROP USER 'user_name'@'host';
```


## Змінити пароль користувачу

```sql
ALTER USER 'username'@'host' IDENTIFIED BY 'password';
-- або
SET PASSWORD FOR 'username'@'host' = 'password';
```

