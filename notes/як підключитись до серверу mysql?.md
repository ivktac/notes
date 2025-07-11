---
date: 2025-07-11
title: як підключитись до серверу mysql?
description: 
draft: false
tags:
  - 🦮how-to
  - databases/mysql
aliases: 
permalink: 
lang: uk
---

З'єднання за замовчуванням

```bash
mysql -u root -p
```

З'єднання по хосту

```bash
mysql -u root -h 127.0.0.1 -p
```

З'єднання по сокету:

```bash
mysql -u root -S /var/lib/mysql/mysql.sock -p
```

З'єднання по мережі:

```bash
mysql -u root -h 127.0.0.1 -P 3306 -p
```

## Див. також

- [[Основи роботи з MySQL]]