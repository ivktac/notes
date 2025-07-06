---
date: 2025-07-03
title: Як працює ARP?
description: 
draft: 
tags:
  - 🌐network/architecture
aliases:
  - how arp works
permalink: how-arp-works
lang: uk
---

1. Хост надсилає ARP запит (по brodacast): "Хто має IP x.x.x.x?"
2. Усі пристрої отримують запит, але лише той із відповідною IP відповідає
3. Відповідь містить MAC адресу
4. Хост зберігає IP та MAC адреси як пару в [[arp таблиця|ARP таблицю]]
5. Дані надсилаються в Ethernet фреймах з цим MAC

> [!info] Запит надсилається на `FF:FF:FF:FF:FF:FF`

## Див. також

- [[ARP]]
- [[навіщо потрібен ARP?]]