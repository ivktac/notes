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


**DISTINCT** працює з усіма вказеними колонками. Напр: `SELECT DISTINCT name, email FROM users;` унікальною парою буде `name`+`email`

## Синтаксис

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

##  Коли використовувати?

- Потрібно знайти унікальні значення в колонці
- Потрібно знайти усі можливі варіанти без потворень
- Порахувати кількість унікальних записів

##  Приклади

- Усі унікальні міста

```sql
SELECT DISTINCT city FROM cities;
```

- Унікальні категорії продуктів

```sql
SELECT DISTINCT category FROM products ORDER BY category;
```

## Див. також

- [[Фільтрація результатів у SQL]]