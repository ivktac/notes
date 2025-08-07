---
created: 2025-08-06
title: LIKE
tags:
  - sql
aliases: 
lang: uk
---

> [!tldr]
> **LIKE** дозволяє шукати текстові значення за шаблоном використовуючи спеціальні символи (wildcards).

```sql
SELECT columns FROM table_name
WHERE column LIKE 'pattern';
```


> [!info] **Спеціальні символи**
> - `%` — нуль або більше символів
> - `_` — рівно один символ
