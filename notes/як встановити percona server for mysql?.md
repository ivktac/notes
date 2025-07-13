---
date: 2025-07-13
title: як встановити percona server?
description: 
draft: false
tags:
  - 🦮how-to
  - databases/mysql
aliases: 
permalink: 
lang: uk
---

1. Встановити Percona repository:

```bash
sudo dnf install https://repo.percona.com/yum/percona-release-latest.noarch.rpm
```

2. Перевірити, чи  пакети є в наявності:

```bash
sudo percona-release setup ps80
sudo dnf list | grep percona | grep server
```

3. Встановити MySQL

```bash
sudo dnf install percona-server-server
```

4. Запустити MySQL

```bash
sudo systemctl start mysqld
```
## Див. також

- [[Percona Server for MySQL]]