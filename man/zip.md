---
date: 2025-07-07
title: zip
description: 
draft: false
tags:
  - man/zip
aliases:
  - zip man
permalink: man-zip
lang: uk
---

> [!tldr]
> Створює zip архів з стисненням.
> 

> [!warning] Важливо
> Не зберігає права доступу до файлів.

## Синтаксис

```bash
zip [options] [archive_name] [files]
```

## Основні опції

- `-r` - рекурсивно (для директорій)
- `-d` - видалити файли з архіву
- `-0` - архівування без стиснення
- `-9` - максимальне стиснення

## Приклади

> [!example] Створити архів з директорії #games/minecraft
> ```bash
> zip -r mods.zip mods/
> ```

## Див. також

- [[unzip]]