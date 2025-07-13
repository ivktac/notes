---
date: 2025-07-06
title: DISTINCT
description: 
draft: 
tags:
  - programming/sql
aliases:
  - sql distinct
permalink: sql-distinct
lang: uk
---

> [!tldr]
> **DISTINCT** видаляє дублікати з результатів запиту, залишаючи лише унікальні комбінації значень.


> [!warning] Важливо
> **DISTINCT** працює з усіма вказеними колонками. Напр: `SELECT DISTINCT name, email FROM users;` унікальною парою буде `name`+`email`

## Синтаксис

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

## Навіщо?

- Потрібні унікальні значення в колонці
- Знайти усі можливі варіанти без повторень
- Порахувати кількість унікальних записів

##  Приклади

> [!example] Усі унікальні міста
> 
> ```sql
> SELECT DISTINCT city FROM cities;
> ```

 > [!example] Унікальні категорії продуктів
> 
> ```sql
> SELECT DISTINCT category FROM products ORDER BY category;
> ```

## Див. також

- [[Фільтрація результатів у SQL]]