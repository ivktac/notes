---
date: 2025-07-05
title: GROUP BY
description: 
tags:
  - programming/sql
aliases:
  - sql групування
  - sql grouping
  - Групування даних
permalink: sql-group-by
lang: uk
---

> [!tldr]
> **GROUP BY** об'єднує рядки з однаковими значеннями в групи та дозволяє застосувати [[Агрегатні функції у SQL|агрегатні функції]] до кожної групи.

## Синтаксис

```sql
SELECT col1, AGG_FUNCTION(col2)
FROM table_name
GROUP BY col1;
```

## Коли використовувати?

- Потрібна статистика по групам
- Підрахунок к-сть запитів за категоріями
- Обчислити суму, середні значення по групам
- Створити звіти

## Приклади

- К-сть клієнтів по містах

```sql
SELECT city, COUNT(*) AS customer_count
FROM customers
GROUP BY city;
```

- Максимальна та мінімальна ціна по категоріях
```sql
SELECT 
	category,
	MIN(price) AS min_price, 
	MAX(price) AS max_price,
	COUNT(*) AS product_count 
FROM products
GROUP BY category;
```

- Аналіз продажів по днях тижня

```sql
SELECT
	DAYNAME(order_date) AS day_of_week,
	COUNT(*) AS orders_count
	AVG(total) AS avg_order_value
FROM orders
GROUP BY DAYNAME(order_date), DAYOFWEEK(order_date)
ORDER BY DAYOFWEEK(order_date);
```
