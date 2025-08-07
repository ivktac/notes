---
created: 2025-08-06
title: IN
tags:
  - sql
aliases: 
lang: uk
---
> [!tldr]
> **IN** дозволяє перевірити, чи міститься значення в списку можливих значень.

> [!tip] Використовується як альтернатива багатьом OR умовам.

```sql
SELECT columns FROM table_name WHERE column IN (value1, value2, ...);
SELECT columns FROM table_name WHERE column IN (SELECT ...);
```