---
date: 2025-07-13
title: Додавання даних у SQL
description: 
draft: false
tags:
  - programming/sql
aliases: 
permalink: 
lang: uk
---

## Синтаксис

```sql
INSERT INTO table_name (column1, column2) 
VALUES (value1, value2);
```

> [!example]
> ```sql
> INSERT INTO Persons (P_id, LastName, FirstName) VALUES (5, 'Tjessem', 'Jakob');
> ```

> [!tip] Можна вказувати конкретні колонки або всі по порядку.
## Див. також

- [[Оновлення даних у SQL]]