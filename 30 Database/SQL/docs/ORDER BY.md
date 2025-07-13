---
date: 2025-07-05
title: ORDER BY
description: 
draft: 
tags:
  - programming/sql
aliases:
  - sql order by
  - sql sorting
permalink: sql-order-by
lang: uk
---

> [!tldr]
> **ORDER BY** — [[SQL оператори|оператор]], який сортує результати запиту за вказаними колонками.

> [!warning] Завжди є останінм кроком у запиті [[SELECT]].

## Синтаксис

```sql
SELECT columns FROM table_name
ORDER BY column1 [ASC|DESC], column2 [ASC|DESC], ...;
```

> [!note]
> -  `ASC`  — за зростанням (за замовчуванням)
> - `DESC` — за спаданням

##  Коли використовувати?

- Потрібно побачити найбільші/найменші значення першими
- Потрібен передбачуваний результат для звітів
- Потрібно відсортувати результати в алфавітному чи іншому порядку

## Приклади

- Базове сортування

```sql
SELECT name, age FROM customers ORDER BY age;
```

- Сортування за колонкою

```sql
SELECT name, age, city FROM customers ORDER BY 2;
```


> [!warning] Важливо
> Сортувати можна як і за назвою колонкою, так і за номером (не рекомендується). 

- Сортування за кількома колонками

```sql
SELECT name, city, age FROM customers 
ORDER BY city ASC, age DESC;
```


- Сортування NULL значень (NULL завжди в кінці при `ASC`)

```sql
SELECT name, email FROM customers
ORDER BY email DESC:
```

- Випадкове сортування

```sql
SELECT * FROM products ORDER BY RAND() LIMIT 5; -- 5 випадкових товарів
```

## Див. також

- [[Фільтрація результатів у SQL]]
- [[GROUP BY]]