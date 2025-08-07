---
created: 2025-08-06
title: як вказати яку БД реплікувати у mysql
tags:
  - how-to
  - mysql
  - replication
aliases: 
lang: uk
---
> [!note]-
> - **replicate-do-db**: перелік БД, які потрібно реплікувати (якщо цієї змінни не існує, то реплікує усі бази дани)
> - **replicate-ignore-db**: перелік, які ігнорується для реплікації
> - **replicate-wild-do-table**: дозволяє динамічно визначати

> [!example] Конфігурація у `/etc/my.cnf`
> ```ini
> replicate-do-db=sales
> replicate-ignore-db=categories
> replicate-wild-do-table=user%.%
> ```