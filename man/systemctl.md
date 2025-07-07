---
date: 2025-07-07
title: systemctl
description: 
draft: false
tags:
  - man/systemctl
  - os/process
  - os/initialization
aliases:
  - systemctl man
permalink: man-systemctl
lang: uk
---

> [!tldr]
> **systemctl** — команда для управління [[systemd]].

## Команди
### Управління станами

| **Команда**                      | **Пояснення**              |
| -------------------------------- | -------------------------- |
| `systemctl start name.service`   | Запустити сервіс           |
| `systemctl stop name.service`    | Зупинити сервіс            |
| `systemctl restart name.service` | Перезапустити сервіс       |
| `systemctl reload name.service`  | Перечитати конфігурацію    |
| `systemctl kill name.service`    | Примусово завершити сервіс |

### Перевірка станів


| **Команда**                         | **Пояснення**              |
| ----------------------------------- | -------------------------- |
| `systemctl status name.service`     | Подивитись детальний стан  |
| `systemctl is-active name.service`  | Чи активний                |
| `systemctl is-enabled name.service` | Чи увімкнений (автозапуск) |
| `systemctl is-failed name.service`  | Чи завершився з помилкою   |

### Автозапуск

| **Команда**                         | **Пояснення**                 |
| ----------------------------------- | ----------------------------- |
| `systemctl enable name.service`     | Увімкнути автозапуск          |
| `systemctl disable name.service`    | Вимкнути автозапуск           |
| `systemctl is-enabled name.service` | Перевірити статус автозапуску |


```bash
systemctl enable name.service
```

> [!note] Добавити у автозапуск і одразу запустити сервіс: `systemctl enable --now name.service`


## Див. також

- [[journalctl]]