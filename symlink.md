---
date: 2025-07-03
title: Символьне посилання
description: 
draft: 
tags:
  - os/filesystem
  - os/🐧linux
aliases:
  - символьне посилання
permalink: 
lang: uk
---

> [!tldr]
> **Символьне посилання (або "soft")** — це спеціальний [[типи файлів у linux|тип файлу]], який містить шлях у вигляді тексту до іншого файлу або каталогу.

> [!note] 
> У [[Linux]] символьні посилання працюють так само як ярлики у [[Windows]].

## Особливості

> [!info] Особливості
> - Має власний [[Метадані файлу (inode)]]
> - Зберігає лише шлях до іншого файлу (розмір файлу = довжина шляху)

> [!warning] Якщо оригінальний файл видалити, посилання стане "broken" ("висячим"): вказуватиме на неіснуючий файл


## Див. також

- [[ln]]
- [[hardlink|жорстке посилання]]