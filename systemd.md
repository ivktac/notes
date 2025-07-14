---
date: 2025-07-07
title: systemd
description: 
draft: false
tags:
  - man/systemd
  - os/process
  - os/initialization
aliases:
  - systemd
  - сістемд
permalink: man-systemd
lang: uk
---

> [!tldr]
> **systemd** — система ініціалізації та менеджер сервісів для [[Linux]].

> [!note] Перший [[Процес]] (**PID** 1), який керує запуском та управлінням усіх системних сервісів.

## Функції

- Ініціалізація системи
- Управління сервісами
- Журналювання (systemd journal)
- Управління юнітами (units)
- Паралельний запуск сервісів

> [!tip] **systemd** дозволяє автозапускати програми при завантаженні системи.

## Каталоги systemd

| Каталог                                        | Опис                   | Пріоритет   |
| ---------------------------------------------- | ---------------------- | ----------- |
| `/etc/systemd/system` або `~/.config/systemd/` | Користувацькі юніти    | Найвищий    |
| `/usr/lib/systemd/system`                      | Встановлені з пакетами | Стандартний |
| `/run/systemd/system/`                         | Тимчасові юніти        |             |

## Див. також

- [[Як створити systemd юніт?]]
- [[Типи юнітів у systemd]]
- [[systemctl]]
- [[journalctl]]