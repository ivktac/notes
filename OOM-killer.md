---
created: 2025-08-06
title: OOM-killer
tags:
  - troubleshooting
  - process
aliases: 
lang: uk
---
> [!tldr]
> **OOM-killer (Out Of Memory killer)** - системний процес, який завершує [[Процес|процеси]] при нестачі пам'яті.

> [!question]- Перевірити активність кілера
> ```bash
> dmesg | grep killed
>```

> [!warning]- Як запобігти цій цьому?
> - встановити ліміти по ресурсам для сервісів
> - у [[MySQL]]: `innodb-buffer-pool-size`
> - У [[Apache HTTP Server|Apache]]: `ServerLimit`, `ThreadLimit`, `MaxConnectionsPerChild`