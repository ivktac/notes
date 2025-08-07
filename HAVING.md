---
created: 2025-08-06
title: HAVING
tags:
  - sql
aliases: 
lang: uk
---

> [!tldr]
> **HAVING** фільтрує результати після [[GROUP BY|Групування даних]] та дозволяє застосувати умови до результатів [[Агрегатні функції у SQL|агрегатних функцій]].

> [!warning] Важливо
> **HAVING** працює значно повільніше за [[WHERE]].


```sql
SELECT col1, AGG_FUNC(col2)
FROM table_name
GROUP BY col1
HAVING condition;
```

## Навіщо?

- потрібно відфільтрувати групи після їх створення
- умови містять [[Агрегатні функції у SQL|агрегатні функції]]