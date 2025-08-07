---
created: 2025-08-06
title: Стани з'єднань iptables
tags:
  - network
  - iptables
aliases:
  - iptables connection tracked
lang: uk
---


- **NEW** - перший пакет з'єднання (запит)
- **ESTABLISHED** - з'єднання встановлено (була вже відповідь)
- **RELATED** - нове з'єднання, пов'язане з існуючим

> [!tip] 99% дозволеного трафіку в stateful фаєрволах припадає на правило `--state ESTABLISHED`.

