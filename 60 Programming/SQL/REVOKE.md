---
date: 2025-07-13
title: REVOKE
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
> **REVOKE** дозволяє відмінити привілеї.

## Синтаксис

```sql
REVOKE тип_привілею [(перелік стовчиків)] [, тип_привілею [(перелік стовпчиків)]...]
ON {ім'я_таблиці} |*|*.*|ім'я_бази_даних.*
FROM ім'я_користувача [, ім'я_користувача...]
```

> [!example]
> ```sql
> REVOKE DELETE, UPDATE ON world.* FROM 'userok'@'localhost';
> ```

## Див. також

- [[GRANT]]
- [[Привілеї у MySQL]]
- [[чому користувач має доступ навіть після відміни привілеїв?]]