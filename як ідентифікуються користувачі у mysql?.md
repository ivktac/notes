---
created: 2025-08-06
title: як ідентифікуються користувачі у mysql?
tags:
  - mysql
  - pam
  - security
aliases: 
lang: uk
---

Користувачі у [[MySQL]] ідентифікуються зв'язкою двох значень: іменем користувача та місцем підключенням (host). 

> [!example] 
> `root@localhost`, `userok@10.9.0.5`

Ця зв'язка відображається у таблиці `mysql.user` я [[Складений ключ]] із полів `Host` та `User`.

