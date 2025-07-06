---
date: 2025-07-06
title: Перейменування у SQL
description: 
draft: 
tags:
  - programming/sql
aliases:
  - sql aliases
  - sql renaming
permalink: sql-aliases
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

## Див. також

- [[SELECT]]
- [[SQL]]