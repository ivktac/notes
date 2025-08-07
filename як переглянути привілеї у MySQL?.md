---
created: 2025-08-06
title: як переглянути привілеї у MySQL?
tags:
  - mysql
  - how-to
aliases: 
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

