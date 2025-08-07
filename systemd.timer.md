---
created: 2025-08-06
title: systemd.timer
tags:
  - systemd
aliases: 
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