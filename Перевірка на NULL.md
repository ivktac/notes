---
created: 2025-08-06
title: Перевірка на NULL
tags:
  - sql
aliases: 
lang: uk
---

- `IS NULL` - значення відсутнє
- `IS NOT NULL` - значення присутнє

```sql
SELECT column_name FROM table_name 
WHERE column_name IS NULL;
```