---
date: 2025-07-13
title: GRANT
description: 
draft: false
tags:
  - databases/mysql
  - programming/sql
aliases: 
permalink: 
lang: uk
---
> [!tldr]
> **GRANT** дозволяє призначити привілеї.
## Синтаксис
```sql
GRANT тип_привілею [(перелік стовчиків)] [, тип_привілею [(перелік стовпчиків)]...] ON {ім'я_таблиці} |*|*.*|ім'я_бази_даних.* TO ім'я_користувача [IDENTIFIED BY 'password'] [, ім'я_користувача [IDENTIFIED BY 'password']...] [WITH GRANT OPTION]
```

> [!example] Наприклад
> ```sql
> GRANT ALL ON world.* TO 'universe'@'localhost' WITH GRANT OPTION;
> ```


## Див. також

- [[REVOKE]]
- [[Привілеї у MySQL]]