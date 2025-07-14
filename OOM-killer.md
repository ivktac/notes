---
date: 2025-07-14
title: OOM-killer
description: 
draft: false
tags:
  - troubleshooting
  - os/process
aliases: 
permalink: 
lang: uk
---
> [!tldr]
> **OOM-killer (Out Of Memory killer)** - системний процес, який завершує [[Процес|процеси]] при нестачі пам'яті.

> [!question]- Перевірити активність кілера
> ```bash
> dmesg | grep killed
>```

> [!warning]- Як запобігти цій хуйні?
> - встановити ліміти по ресурсам для сервісів
> - у [[MySQL]]: `innodb-buffer-pool-size`
> - У [[Apache HTTP Server|Apache]]: `ServerLimit`, `ThreadLimit`, `MaxConnectionsPerChild`