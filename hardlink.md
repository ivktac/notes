---
date: 2025-07-03
title: Жорстке посилання
description: 
draft: 
tags:
  - os/🐧linux
  - os/filesystem
aliases:
  - жорстке посилання
permalink: hardlinks
lang: uk
---

> [!tldr]
> **Жорстке посилання** — це додаткове ім'я для існуючого [[Метадані файлу (inode)]] файлу.

## Особливості

> [!info] Особливості
> - усі жорсткі посилання = той самий _inode_
> - зробивши зміни в одному місці — змінються решта
> - повноцінно видаляється, лише коли лічильник посилання = 0
> - створювати можна лише для звичайних файлів і на тому ж диску (файловій системі)

## Див. також

- [[ln]]
- [[symlink|символьне посилання]]