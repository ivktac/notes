---
created: 2025-08-06
title: Скільки потрібно правил для роботи протоколу TCP?
tags:
  - network
  - iptables
aliases: 
lang: uk
---
2 правила, а саме для:

- **NEW** - для SYN-запиту (1 правило)
- **ESTABLISHED** - для пітвердження з'єднання (відповідь SYN-ACK->ACK)