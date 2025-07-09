---
date: 2025-07-05
title: SQL
description: 
draft: false
tags:
  - programming/sql
aliases:
  - select sql
permalink: sql-select
lang: uk
---

> [!tldr]
> **SELECT** основна команда [[SQL]] для отримання (вибірки) даних з таблиць бази даних.

## Синтаксис

```sql
SELECT column1, column2, ...
FROM table_name;
```

## Для чого потрібен SELECT?

- Переглянути, що зберігається у таблиці
- Створити звіт даних
- Проаналізуавти інформацію
- Отримати дані для додатків

## Приклади

 - Вибрати всі колонки

```sql
SEELCT * FROM customer;
```

-   Вибрати конкретні колонки

```sql
SELECT name, email FROM customer;
```

- Перейменувати колонку (аліас)

```sql
SELECT name AS 'Ім\'я', email AS "Пошта" FROM customer;
```

## Див. також

- [[SQL]]
- [[Перейменування назв у SQL]]
- [[Фільтрація результатів у SQL]]