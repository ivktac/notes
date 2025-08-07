---
created: 2025-08-06
title: Statement-based реплікація
tags:
  - database
  - replication
aliases: 
lang: uk
---
- записує як **SQL запити**
- малі розміри логів, менше використання мережі
- певні обмеження у не-детермічних запитах

> [!example] Приклад зберігання
> ```sql
> UPDATE users SET status = 'active';
> ```