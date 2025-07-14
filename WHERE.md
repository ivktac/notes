---
date: 2025-07-05
title: WHERE
description: 
draft: 
tags:
  - programming/sql
aliases: []
permalink: sql-where
lang: uk
---

> [!tldr]
> **WHERE** — це команда, яка дозволяє фільтрувати рядки таблиці за певним критерієм (або критеріями).

> [!warning] Важливо
> **WHERE** не працює з агрегатними функціями.
## Синтаксис

```sql
SELECT columns
FROM table_name
WHERE condition;
```

## Приклади

> [!example] Прості порівняння
> 
> ```sql
> SELECT * FROM products WHERE price > 100;
> SELECT * FROM customers WHERE age = 25;
> SELECT * FROM orders WHERE status = 'completed'; 
> ```

 > [!example] Комбінування умов 
> 
> ```sql
> SELECT * FROM products WHERE price > 50 AND category = 'electronics';
> SELECT * FROM customers WHERE age < 18 OR age > 65;
> ```

## Див. також

- [[Різниця між WHERE та HAVING]]
- [[Фільтрація результатів у SQL]]