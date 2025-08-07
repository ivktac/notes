---
created: 2025-08-06
title: LIMIT
tags:
  - sql
aliases: 
lang: uk
---

> [!tldr]
> **LIMIT** обмежує кількість рядків, які повертає запит.

```sql
SELECT columns FROM table_name LIMIT number;
SELECT columns FROM table_name LIMIT offset, number; -- MySQL
SELECT columns FROM table_name LIMIT number OFFSET offset; -- PostgreSQL
```

## Навіщо?


- Велика таблиця і не потрібні усі результати
- [[Pagination|Пагінація]] для веб-додатків
- Швидкий перегляд даних
- Топ-N запити