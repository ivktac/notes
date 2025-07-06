---
date: 2025-07-05
title: SELF JOIN
description: 
draft: 
tags:
  - programming/sql
aliases: 
permalink: sql-self-join
lang: uk
---

> [!tldr]
> **SELF JOIN** це [[Об'єднання таблиць|об'єднання таблиці]] самої з собою.

## Синтаксис

```sql
SELECT columns FROM table_name a
JOIN table_name b
ON condition;
```

> [!warning] `a` та `b` — аліаси одніє і тієї ж таблиці `table_name`. ([[Перейменування назв у SQL]])

## Приклади


-  Знайти усі фільми, що вийшли до "Star Wars"

```sql
SELECT a.title, a.year FROM Movie a
JOIN Movie b ON b.title = 'Star Wars' AND a.year < b.year;
```

- Знайти співробітників, що заробляють більше за свого керівника :)

```sql
SELECT e1.name, e1.salary FROM employees e1
JOIN employees e2 ON e1.manager_id = e2.id AND e1.salary > e2.salary;
```

- Знайти клієнтів з одного міста

```sql
SELECT a.name, b.name, a.city FROM customers a
JOIN customers b ON a.city = b.city AND a.id <> b.id;
```

## Див. також

- [[Об'єднання таблиць]]