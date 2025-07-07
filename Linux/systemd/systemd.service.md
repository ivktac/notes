---
date: 2025-07-07
title: systemd.service
description: 
draft: false
tags:
  - man/systemd/service
aliases:
  - systemd services
permalink: man-systemd-service
lang: uk
---


## Типи сервісів

| **Тип**   | **Опис**                             |
| --------- | ------------------------------------ |
| `simple`  | Основний процес сервісу              |
| `forking` | Процес створює дочірний процес       |
| `oneshot` | Процес завершується після запуску    |
| `notify`  | Сервіс сповіщає про готовність       |
| `idle`    | Відкладає запуск до завершення інших |
 
## Шаблон

```ini
[Unit]
Description=My Service
After=network.target

[Service]
Type=simple
ExecStart=command
Restart=always
User=root

[Install]
WantedBy=multi-user.target
```

## Див. також

- [[systemd.target]]