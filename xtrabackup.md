---
created: 2025-08-06
title: xtrabackup
tags:
  - cli
  - database
  - backups
  - mysql
aliases: 
lang: uk
---

##  Створити бекапи ([[Інкрементальна резервна копія|інкрементальні]])

**Створити повний бекап**

```bash
xtrabackup -u[user] -p[password] --backup --target-dir=/data/backups/full
```

**Інкрементальний бекап:**

```bash
xtrabackup --backup --target-dir=/data/backups/inc1 --incremental-basedir=/data/backups/full
```

**Ланцюжок інкрементальних бекапів:**

```bash
xtrabackup --backup --target-dir=/data/backups/inc2 --incremental-basedir=/data/backups/inc1
```

> [!warning] Чим довший ланцюжок, тим довше відновлення.


## Відновити дані

> [!warning] Бекап потрібно підготувати перед відновленням, бо "гарячий" дамп не є цілісним.

**Підготовка повного бекапу:**

```bash
xtrabackup --prepare --target-dir=/data/backups/full
```

**Підготовка інкрементального ланцюжка:**

```bash
xtrabackup --prepare --apply-log-only --target-dir=/data/backups/full
xtrabackup --prepare --apply-log-only --target-dir=/data/backups/full --incremental-dir=/data/backups/inc1
xtrabackup --prepare --target-dir=/data/backups/full --incremental-dir=/data/backups/inc2
```

> [!warning] `--apply-log-only` на всіх кроках окрім останнього.

## Див. також

- [[mysqlbackup]]