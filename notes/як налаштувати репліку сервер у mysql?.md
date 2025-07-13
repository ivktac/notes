---
date: 2025-07-03
title: Як налаштувати репліку сервер у MySQL?
description: 
draft: 
tags:
  - 🦮how-to
aliases:
  - how to configure replica mysql
  - replica mysql
  - how to setup replica
permalink: how-to-configure-replica-mysql
lang: uk
---
## Налаштувати source-сервер

1. Редагувати `/etc/my.cnf` на source-сервері:

> [!note]-
> - **server-id**: ідентифікатор сервера (має бути унікальне значення)
> - **log_bin**: ім'я файлу бінарного лога або шлях до нього
> - **binlog_do_db**: перелік баз даних, яких потрібно реплікувати. Якщо не вказати, то реплікуватимуться усі БД.

```toml
[mysqld]
server-id = 1
log_bin = mysql-bin
binlog_do_db = world
```

2. Перезавантажити `mysqld`:

3. Створити користувача для репліки:

> [!note]-
> Обов'язкові права:
> - **REPLICATION SLAVE**: дозвіл на підключення до серверу та отримати оновлені дані
> - **REPLICATION CLIENT**: привілей на команди: `SHOW MASTER STATUS`, `SHOW REPLICA STATUS`, `SHOW BINARY LOGS`

```sql
CREATE USER 'repl'@'%' IDENTIFIED BY 'ReplicaPASS1!';  
GRANT REPLICATION SLAVE, REPLICATION CLIENT ON *.* TO 'repl'@'%';
FLUSH PRIVILEGES;
```

4. Отримати дані про поточний файл бінарних логів (**File**) та позицію (**Position**):

```sql
+------------------+----------+--------------+------------------+
| File             | Position | Binlog_Do_DB | Binlog_Ignore_DB |
+------------------+----------+--------------+------------------+
| mysql-bin.000001 |      107 | rating       |                  |
+------------------+----------+--------------+------------------+
```

5. Зробити [[how to create databases dump in mysql|дамп бази даних]] ([[mysqldump]])

## Налаштувати replica-сервер

1. Редагувати `/etc/my.cnf` на replica-сервері:

> [!note]-
> - **server-id**: індентифікатор сервера (унікальний і відмінний від source-сервера)
> - **skip_replica_start**: не запускати режим реплікації
> - **relay_log**: файл у який репліка записуватиме дані
> - **binlog_do_db** (replicate_do_db): перелік бази даних. Якщо не вказати, реплікуються усі

```toml
[mysqld]
server-id = 2
relay_log = mysql-relay-bin
replicate_do_db = rating
```

2. Перезавантажити `mysqld`

3. Створити базу даних і скопіювати дамп бази з source-сервера ([[mysqldump#^d354c8]])

4. Запустити процес реплікації

```sql
CHANGE REPLICATION TO  
SOURCE_HOST='IP_MASTER',  
SOURCE_PORT=3306,  
SOURCE_USER='repl',  
SOURCE_PASSWORD='ReplicaPASS1!',  
SOURCE_LOG_FILE='mysql-bin.000001',  
SOURCE_LOG_POS = 107,  
GET_SOURCE_PUBLIC_KEY=1;

START REPLICA;
```

5. Перевірити стан репліки

```sql
SHOW REPLICA STATUS\G
```

