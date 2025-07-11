---
date: 2025-07-11
title: Statement-based реплікація
description: 
draft: false
tags:
  - databases/replication
aliases: 
permalink: 
lang: uk
---
- записує як **SQL запити**
- малі розміри логів, менше використання мережі
- певні обмеження у не-детермічних запитах

> [!example] Приклад зберігання
> ```sql
> UPDATE users SET status = 'active';
> ```