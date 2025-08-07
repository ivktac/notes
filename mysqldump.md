---
created: 2025-08-06
title: mysqldump
tags:
  - mysql
  - backups
  - cli
aliases: 
lang: uk
---

> [!tldr]
> **mysqldump** — утиліта для створення [[Логічні бекапи|логічних]] [[Повна резервна копія (Full Backup)|повних бекапів]] у вигляді [[SQL]]-запитів.
 
> [!warning] За замовчуванням виводить на [[стандартні потоки|STDOUT]], таблиці блокуються ([[Теплі бекапи|теплий бекап]]).

## Синтаксис

```bash
mysqldump -u [user] -p[password] [database] > backup.sql
```

> [!tip] **Для InnoDB:** опція `--single-transaction` для дампу в межах однієї транзакції.

## Опції

- `-A, --all-databases` - всі БД
- `-B, --databases` - конкретні БД
- `--add-drop-table` - додає DROP TABLE
- `--no-data` - тільки структура
- `--single-transaction` - одна транзакція
- `--master-data` - інформація про binlog

## Приклади

> [!example] Бекап конкретної таблиці
> ```bash
> mysqldump -p -u root --databases VoipCompany --tables Customers > backup.sql
> ```

> [!example] З умовою
> ```bash
> mysqldump -p -u root --databases VoipCompany --tables Customers --where="name='John'" > backup.sql
> ```

> [!example] Відновлення
> ```bash
> mysql -u root VoipCompany < backup.sql
> ```

^d354c8

## Див. також

- [[Percona XtraBackup]]