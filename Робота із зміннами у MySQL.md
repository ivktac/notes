---
date: 2025-07-11
title: Перегляд змінних у MySQL
description: 
draft: false
tags:
  - databases/mysql
aliases: 
permalink: 
lang: uk
---

## Перегляд змінн

> [!example]  Щоб переглянути змінні у MySQL:
> ```sql
> SHOW VARIABLES;
> SHOW VARIABLES LIKE 'validate_password%';
>```

## Редагування змінн

Існує два способа змінити значення:


> [!example] Динамічна змінна на "льоту" (існує до перезавантаження сервера)
> ```sql
> SET GLOBAL validate_password.policy = LOW;
> ```

> [!example] Статична зміна у конфігураційному файлі
> ```ini
> [mysqld]
> validate_password.policy=LOW
> ```
> Зберігається завжди, застосовується тільки після перезавантаження сервера.


## Див. також

- [[Налаштування MySQL]]