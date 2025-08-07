---
created: 2025-08-06
title: перейменування назв у SQL
tags:
  - sql
aliases:
  - aliases in sql
lang: uk
---

- Явне використання AS

```sql
SELECT first_name AS "Ім'я"
FROM users;
```

-  Неявне використання (без AS)

```sql
SELECT first_name "Ім'я"
FROM users;
```

> [!tip]
> Щоб перейменувати колонку на ім'я, що містить пробіли потрібно використовувати лапки (\` \`, ' ', " ")
