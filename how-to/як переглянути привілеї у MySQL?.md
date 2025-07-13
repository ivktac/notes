---
date: 2025-07-13
title: як переглянути привілеї?
description: 
draft: false
tags:
  - databases/mysql
  - 🦮how-to
aliases: 
permalink: 
lang: uk
---

```sql
SHOW GRANTS FOR 'username'@'host';
```

```sql
+-----------------------------------------+
| Grants for username@host                |
+-----------------------------------------+
| GRANT USAGE ON *.* TO `username`@`host` |
+-----------------------------------------+
```

