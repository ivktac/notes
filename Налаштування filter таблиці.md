---
date: 2025-07-09
title: Налаштування filter таблиці
description: 
draft: false
tags:
  - configuration
  - man
  - 🌐network/firewall
aliases:
  - config filter table iptables
permalink: 
lang: uk
---

- **INPUT** доступ до локальних процесів
- **OUTPUT** вихідний трафік
- **FORWARD** фільтрація транзитного трафіку (для [[роутер|роутерів]])

## Базова конфігурація

- Встановити політику за замовчуванням

```bash
iptables -P INPUT DROP
iptables -P OUTPUT ACCEPT
iptables -P FORWARD DROP
```

- Дозволити `loopback`

```bash
iptables -A INPUT -i lo -j ACCEPT
```

> [!warning] Важливо
> - Якщо дозволити запити, то рекомендовано дозволити відповіді.
> - **Порядок** правил має значення
> - **Останнє правило** може виконувати роль [[Політика за замовчуванням|політики за замовчуванням]]

## Див. також

- [[Таблиці iptables]]
- [[Правила iptables]]
- [[Стани з'єднань iptables]]