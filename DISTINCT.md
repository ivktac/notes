---
created: 2025-08-06
title: DISTINCT
tags:
  - sql
aliases: 
lang: uk
---

> [!tldr]
> **DISTINCT** видаляє дублікати з результатів запиту, залишаючи лише унікальні комбінації значень.


> [!warning]
> **DISTINCT** працює з усіма вказеними колонками. 
> Напр: `SELECT DISTINCT name, email FROM users;` унікальною парою буде `name`+`email`

```sql
SELECT DISTINCT col1, col2, ...
FROM table_name;
```

## Навіщо?

- потрібні унікальні значення в стовпчику
- знайти усі можливі варіанти без повторень
- порахувати к-сть унікальних записів