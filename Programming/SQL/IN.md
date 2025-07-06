---
date: 2025-07-05
title: IN
description: 
draft: 
tags:
  - programming/sql
aliases:
  - sql in
permalink: sql-in
lang: uk
---

> [!tldr]
> **IN** дозволяє перевірити, чи міститься значення в списку можливих значень.

> [!tip] Використовується як альтернатива багатьом OR умовам.

## Синтаксис

```sql
SELECT columns FROM table_name WHERE column IN (value1, value2, ...);
SELECT columns FROM table_name WHERE column IN (SELECT ...);
```

## Приклади

- Пошук за конкретними значеннями

```sql
SELECT * FROM users WHERE first_name IN ('Maksim', 'Andrew', 'Ivan');
```

- З підзапитом 

```sql
SELECT * FROM users WHERE user_id IN (SELECT id FROM users WHERE city = 'Kyiv');
```

## Див. також

- [[Фільтрація результатів у SQL]]