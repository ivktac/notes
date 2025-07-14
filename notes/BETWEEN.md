---
date: 2025-07-06
title: BETWEEN
description: 
draft: 
tags:
  - programming/sql
aliases:
  - sql between
permalink: sql-between
lang: uk
---

> [!tldr]
> **BETWEEN** перевіряє чи знаходиться значення в межах заданого діапазону (включно з границями).

## Синтаксис

```sql
SELECT columns FROM table_name
WHERE column BETWEEN value1 AND value2;
```

## Приклади

- Числовий діапазон

```sql
SELECT * FROM example WHERE column BETWEEN 333 AND 666;
```

- Діапазон дат

```sql
SELECT * FROM example WHERE column_date BETWEEN '2025-01-01' AND '2025-12-31';
```

- Поза діапазоном

```sql
SELECT * FROM example WHERE column NOT BETWEEN 18 AND 99;
```

## Див. також

- [[WHERE]]
- [[Фільтрація результатів у SQL]]