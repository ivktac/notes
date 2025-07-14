---
date: 2025-07-07
title: unzip
description: 
draft: false
tags:
  - man
aliases: 
permalink: man-unzip
lang: uk
---

> [!tldr]
> Розпаковує [[zip]] архіви в поточний каталог або вказане місце.

## Синтаксис

```bash
unzip [options] [archive_file] -x [exclude] -d [destination]
```

## Основні опції

- `-l` - показати список файлів в архіві
- `-t` - тестування архіву на цілісність
- `-u` - оновити існуючі файли
- `-j` - ігнорувати структуру директорій
- `-q` - тихий режим
- `-d` - вказати каталог призначення

## Приклади

> [!example] Розпакувати у вказану директорію #games/minecraft #os/🐧linux 

```bash
unzip mods.zip -d $HOME/.var/app/org.prismlauncher.PrismLauncher/data/PrismLauncher/instances/$INSTANCE_NAME/minecraft/mods/
```