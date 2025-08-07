---
created: 2025-08-06
title: SELF JOIN
tags:
  - sql
aliases: 
lang: uk
---

> [!tldr]
> **SELF JOIN** це [[Об'єднання таблиць|об'єднання таблиці]] самої з собою.

```sql
SELECT columns FROM table_name a
JOIN table_name b
ON condition;
```


> [!warning] `a` та `b` — аліаси одніє і тієї ж таблиці `table_name`. ([[Перейменування назв у SQL]])
