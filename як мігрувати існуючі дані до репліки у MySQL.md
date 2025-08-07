---
created: 2025-08-06
title: як мігрувати існуючі дані до репліки у MySQL
tags:
  - how-to
  - replication
  - mysql
aliases: 
lang: uk
---
1. Підключитись до source ("мастера")
2. Експортувати базу даних: `sudo mysqldump -u root db > db.sql`
3. Скопіювати дамп до репліки-серверу
4. Створити базу даних та імпортувати дані: `sudo mysql db < db.sql