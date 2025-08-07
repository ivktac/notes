---
created: 2025-08-06
title: mysql command
tags:
  - cli
  - mysql
aliases: 
lang: uk
---

> [!tldr]
> **mysql** команда, що дозволяє запускати сервер mysql.

## Опції

- `-?`, `--help` — Довідка
- `-b`, `--basedir=[path]` — Шлях до директорії із встановленим mysql-сервером
- `-h`, `--datadir [homedir]` — Шлях до директорії із базою даних
- `-l`, `--log=[filename]` — Ім'я журналу транзакцій
- `-L`, `--language=[language]` — Мова за замовчуванням (English)
- `-P`, `--port=[port]` — Порт для з'єднання
- `-h`, `--hostname=[hostname]` — Хост серверу mysql
- `-u`, `--user=[user]` — Ім'я користувача для доступу до mysql
- `-p`, `--pasword=[password]` — Пароль користувача
- `-V`, `--version`  — Інформація про версію

> [!example] Підключення
> ```bash
> mysql -h localhost -u root -p -P 3306
> ```

## Див. також

- [[як підключитись до серверу mysql?]]
- [[Основи роботи з MySQL]]