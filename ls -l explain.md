---
date: 2025-07-03
title: Що означають колонки у виводі  `ls -l`?
description: 
tags:
  - man
  - os/filesystem
draft: 
aliases:
  - пояснення ls -l
permalink: explain-long-list-fields-in-ls
lang: uk
---

```bash
$ ls -l
total 4
-rw-r--r-- 1 padavan padavan 1024 Apr 21 10:30 file.txt
```

- `total 4` — загальний розмір у блоках (1КБ)

Кожен наступний рядок показує детальну інформацію про кожен файл у переліку:

- `-rw-r--r--` — права доступу (перший символ показує [[типи файлів у linux|тип файлу]])
- `1` — кількість [[hardlink|жорстких посилань]]
- `padavan` — власник файлу ([[UID]])
- `padavan` — назва групи власника ([[GID]])
- `1024` — розмір у байтах
- `Apr 21 10:30` — час останьої модифікацїі (`mtime`)
- `file.txt` — ім'я файлу

## Див. також

- [[ls]]
