---
date: 2025-07-09
title: Як обробляються ланцюжки у iptables?
description: 
draft: false
tags: 
aliases:
  - how iptables chains work
permalink: how-chains-work-in-iptables
lang: uk
---

Правила у ланцюжку обробляються **послідовно зверху вниз**. Якщо умови правила задоволені і дія остаточна (ACCEPT, DROP), наступні правила не розглядаються.

## Див. також

- [[iptables]]
- [[Політика за замовчуванням у iptables]]