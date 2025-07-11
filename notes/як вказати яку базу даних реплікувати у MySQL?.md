---
date: 2025-07-11
title: як вказати яку базу даних реплікувати у MySQL?
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