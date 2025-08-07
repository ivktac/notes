---
created: 2025-08-06
title: як перевірити чи працює репліка у MySQL?
tags:
  - mysql
  - how-to
aliases: 
lang: uk
---

На репліці сервері:

```sql
SHOW SLAVE STATUS\G
-- або
SHOW REPLICA STATUS\G
```

> [!todo] Далі перевірити
> - `Replica_IO_Running`: "Yes"
> - `Replica_SQL_Running`: "Yes"
> - `Seconds_Behind_Master`: показує лаг-час (lag time)

> [!warning] Важливо
> Регулярний моніторинг роботи репліки дозволяє уникнути потенційних проблем у майбутньому.