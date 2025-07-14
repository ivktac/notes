---
date: 2025-07-07
title: systemd.timer
description: 
draft: false
tags:
  - man
  - devops/systemd
aliases:
  - systemd timers
permalink: systemd-timer
lang: uk
---

> [!info] Аальтернатива [[cron]].

## Типи таймерів

| Параметр            | Опис                             |
| ------------------- | -------------------------------- |
| `OnCalendar`        | Дата (календарна)                |
| `OnBootSec`         | Через N секунд після завнтаження |
| `OnUnitActiveSec`   | Через N секунд після активації   |
| `OnUnitInactiveSec` | Через N секунд після деактивації |

## Приклад

```ini
[Unit]
Description=Run backup daily

[Timer]
OnCalendar=daily
Persistent=true

[Install]
WantedBy=timers.target
```

## Див. також

- [[systemd.service]]