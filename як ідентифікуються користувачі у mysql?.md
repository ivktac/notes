---
date: 2025-07-13
title: як ідентифікуються користувачі у mysql?
description: 
draft: false
tags:
  - databases/mysql
aliases: 
permalink: 
lang: uk
---

Користувачі у [[MySQL]] ідентифікуються зв'язкою двох значень: іменем користувача та місцем підключенням (host). 

> [!example] 
> `root@localhost`, `userok@10.9.0.5`

Ця зв'язка відображається у таблиці `mysql.user` як [[Складений ключ]] із полів `Host` та `User`.

