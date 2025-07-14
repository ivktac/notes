---
date: 2025-07-09
title: Стани з'єднань iptables
description: 
draft: false
tags:
  - man/iptables
  - 🌐network/firewall
aliases:
  - iptables connection tracked
permalink: 
lang: uk
---

**Основні стани:**

- **NEW** - перший пакет з'єднання (запит)
- **ESTABLISHED** - з'єднання встановлено (була вже відповідь)
- **RELATED** - нове з'єднання, пов'язане з існуючим

> [!tip] 99% дозволеного трафіку в stateful фаєрволах припадає на правило `--state ESTABLISHED`.



## Див. також

- [[Скільки потрібно правил для роботи протоколу TCP?]]