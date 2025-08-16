---
created: 2025-08-11
title: як описати таблицю у SQLite?
tags:
  - database
  - sqlite
  - how-to
aliases: 
lang: uk
---
```sql
.schema table_name
```

> [!warning]
> Після назви таблциі немає крапки з комою, якщо додати `;` в кінець, то `.schema` вважатиме `table_name;` назву таблиці.

Для того, щоб вивести не саму схему як [[SQL]]-запит, а у вигляді структури таблиці:

```sql
.header on
.mode column
```

Або

```sql
pragma table_info('table_name');
```

Також можна отримати стуктуру через SQL-запит:

```sql
SELECT sql FROM sqlite_schema
WHERE name = 'table_name';
```