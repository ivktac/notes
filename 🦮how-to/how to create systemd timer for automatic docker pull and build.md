---
date: 2025-07-08
title: Як створити systemd.timer юніт для автоматичної скомпоновки docker compose?
description: 
draft: false
tags:
  - man/systemd/timer
  - os/automation
  - docker
aliases: 
permalink: systemd-timer-automatic-docker-pull
lang: uk
---

1. Створити systemd.service:

```ini
[Unit]
Description=Update Docker Compose Servies
Wants=network-online.target
After=network-online.target

[Service]
Type=oneshot
WorkingDirectory=/opt/app/docker-compose
ExecStart=/usr/bin/docker compose pull
ExecStartPost=/usr/bin/docker compose up -d
```

2. Створити таймер

```ini
[Unit]
Description=Run Docker Compose update every 1 hour

[Timer]
OnBootSec=1min
OnUnitActiveSec=1h
Persistent=true

[Install]
WantedBy=timers.target
```


