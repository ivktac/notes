---
date: 2025-07-14
title: Метрики у команді top
description: 
draft: false
tags:
  - man/top
  - troubleshooting/metrics
aliases: 
permalink: 
lang: uk
---

Кожне поло в утиліті [[top]] показує на що процесор витрачає час (у відсотках `%`)


- **User (us)** — виконання коду користувача без змінених nice (user space)
- **System (sy)** — виконання процесів ядра (kernel/system space)
- **Nice (ni)** — виконання коду користувача із зміненим nice
- **Idle (id)** — простій процесора
- **Wait (wa)** — очікування завершення задач вводу/виводу
- **Hardware interrupts (hi)** — обробка апаратних переривань
- **Software interrupts (si)** — обробка програмних переривань
- **Stolen (st)** — забраний від ВМ гіпервізором