---
date: 2025-07-06
title: HAVING
description: 
draft: 
tags:
  - programming/sql
aliases:
  - sql having
permalink: sql-having
lang: uk
---

> [!tldr]
> **HAVING** фільтрує результати після [[GROUP BY|Групування даних]] та дозволяє застосувати умови до результатів [[Агрегатні функції у SQL|агрегатних функцій]].

> [!warning] Важливо
> **HAVING** працює значно повільніше за [[WHERE]].

## Синтаксис

```sql
SELECT col1, AGG_FUNC(col2)
FROM table_name
GROUP BY col1
HAVING condition;
```

## Коли використовувати?

- Потрібно відфільтрувати групи після їх створення
- Умови містять агрегатні функції

## Приклади

- Категорії з середньою ціною > 100

```sql
SELECT category, AVG(price) AS avg_price 
FROM products 
GROUP BY category
HAVING AVG(price) > 100;
```

## Див. також

- [[WHERE]]
- [[Різниця між WHERE та HAVING]]