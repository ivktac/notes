---
created: 2025-08-06
title: GRANT
tags:
  - mysql
aliases: 
lang: uk
---
> [!tldr]
> **GRANT** дозволяє призначити привілеї.

```sql
GRANT тип_привілею [(перелік стовчиків)] [, тип_привілею [(перелік стовпчиків)]...] ON {ім'я_таблиці} |*|*.*|ім'я_бази_даних.* TO ім'я_користувача [IDENTIFIED BY 'password'] [, ім'я_користувача [IDENTIFIED BY 'password']...] [WITH GRANT OPTION]
```

## Див. також

- [[REVOKE]]