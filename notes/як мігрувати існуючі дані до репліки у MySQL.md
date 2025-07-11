---
date: 2025-07-11
title: як мігрувати існуючі дані до репліки у MySQL
description: 
draft: false
tags:
  - 🦮how-to
  - databases/mysql
  - databases/replication
aliases: 
permalink: 
lang: uk
---

> [!todo]
> 1. Підключитись до source ("мастера")
> 2. Експортувати базу даних: `sudo mysqldump -u root db > db.sql`
> 3. Скопіювати дамп до репліки-серверу
> 4. Створити базу даних та імпортувати дані: `sudo mysql db < db.sql`
