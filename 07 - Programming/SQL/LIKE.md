---
date: 2025-07-05
title: LIKE
description: 
draft: 
tags:
  - programming/sql
aliases:
  - sql like
permalink: sql-like
lang: uk
---

> [!tldr]
> **LIKE** дозволяє шукати текстові значення за шаблоном використовуючи спеціальні символи (wildcards).

## Синтаксис

```sql
SELECT columns FROM table_name
WHERE column LIKE 'pattern';
```

> [!info] **Спеціальні символи**
> - `%` — будь-яка к-сть символів (0 або більше)
> - `_` — рівно один символ

##  Приклади

- Значення, що починаються на 'ABC'

```sql
SELECT * FROM table_name WHERE column LIKE "ABC%";
```

- Значення, що закінчуються на 'XYZ'

```sql
SELECT * FROM table_name WHERE column LIKE '%XYZ';
```

- Значення, що містять "TUX"

```sql
SELECT * FROM table_name WHERE column LIKE "%TUX%";
```

## Див. також

- [[WHERE|WHERE]]
- [[SQL]]