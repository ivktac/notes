---
date: 2025-07-13
title: Point-in-Time відновлення
description: 
draft: false
tags:
  - databases/backups
  - man/mysql
aliases: 
permalink: 
lang: uk
---

**Point-in-Time Recovery** дозволяє відновити БД до конкретного моменту в минулому, використовуючи бекап + бінарні журнали.


> [!question] Що потрібно для цього?
> - Бекап (базовий стан)
> - Бінарні журнали (зміни після бекапу)
> - Позиція в журналі (курсор в байтах)

> [!tip] Використовуйте утиліту[[mysqlbinlog]] для роботи з бінарними журналами.
## Див. також

- [[Процес Point-in-Time Recovery]]
- [[Бінарні журнали у MySQL]]