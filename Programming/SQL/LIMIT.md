---
date: 2025-07-06
title: LIMIT
description: 
draft: 
tags:
  - programming/sql
aliases: 
permalink: sql-limit
lang: uk
---

> [!tldr]
> **LIMIT** обмежує кількість рядків, які повертає запит.

## Синтаксис

```sql
SELECT columns FROM table_name LIMIT number;
SELECT columns FROM table_name LIMIT offset, number; -- MySQL
SELECT columns FROM table_name LIMIT number OFFSET offset; -- PostgreSQL
```

## Для чого потрібен?

- Велика таблиця і не потрібні усі результати
- [[Pagination|Пагінація]] для веб-додатків
- Швидкий перегляд даних
- Топ-N запити

## Приклади

- Перші 10 записів

```sql
SELECT * FROM users LIMIT 10;
```

- Топ-5 найдорожчих товарів

```sql
SELECT name, price FROM products ORDER BY price DESC LIMIT 5;
```

- Випадковий запис

```sql
SELECT * FROM products ORDER BY RAND() LIMIT 1;
```

- Пагінація для вебсайту

```sql
SELECT * FROM products ORDER BY NAME LIMIT 0, 20;
SELECT * FROM products ORDER BY NAME LIMIT 20, 40;
```

- Остання активність користувачів 

```sql
SELECT user_id, last_login
FROM users
ORDER BY last_login DESC
LIMIT 5;
```

## Див. також

- [[SELECT]]
- [[Фільтрація результатів у SQL]]