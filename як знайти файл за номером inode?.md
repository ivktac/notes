---
date: 2025-07-03
title: Як знайти файл за номером inode?
description: 
draft: 
tags:
  - 🦮how-to
aliases: 
permalink: how-to-find-file-by-inode
lang: uk
---

```bash
$ find -inum 101537091
```

Результат:

```bash
./file.txt
```