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

## Синтаксис

```bash
systemctl [OPTIONS] COMMAND [UNIT...]
```

## Команди

### Запуск та зупинка сервісів

| Команда                                    | Опис                                           |
| ------------------------------------------ | ---------------------------------------------- |
| `systemctl start service_name`             | Запустити сервіс                               |
| `systemctl stop service_name`              | Зупинити сервіс                                |
| `systemctl restart service_name`           | Перезапустити сервіс                           |
| `systemctl reload service_name`            | Перезавантажити конфігурацію без перезапуску   |
| `systemctl reload-or-restart service_name` | Перезавантажити конфігурацію або перезапустити |

### Автозапуск

| Команда                               | Опис                          |
| ------------------------------------- | ----------------------------- |
| `systemctl enable service_name`       | Увімкнути автозапуск          |
| `systemctl disable service_name`      | Вимкнути автозапуск           |
| `systemctl enable --now service_name` | Увімкнути та запустити одразу |
| `systemctl disable --now service_name | Вимкнути та зупинити одразу   |

## Перегляд стану

| Команда                             | Опис                                |
| ----------------------------------- | ----------------------------------- |
| `systemctl status service_name`     | Статус сервісу                      |
| `systemctl is-active service_name`  | Перевірити чи активний              |
| `systemctl is-enabled service_name` | Перевірити чи увімкнений автозапуск |
| `systemctl is-failed service_name`  | Перевірити чи завершився невдало    |

## Інформація про юніти


| Команда                                     | Опис                     |
| ------------------------------------------- | ------------------------ |
| `systemctl list-units`                      | Список всіх юнітів       |
| `systemctl list-units --type=service`       | Список всіх сервісів     |
| `systemctl list-units --failed`             | Список невдалих юнітів   |
| `systemctl list-unit-files --state=enabled` | Список увімкнених юнітів |
| `systemctl list-dependencies service_name`  | Дерево залежностей       |


## Див. також

- [[journalctl]]