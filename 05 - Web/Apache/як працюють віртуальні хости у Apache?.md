---
date: 2025-07-04
title: Як працюють віртуальні хости у Apache?
description: 
draft: 
tags:
  - web/apacahe
aliases:
  - how virtual hosts work in apache
permalink: how-virtual-hosts-work-in-apache
lang: uk
---


1. Віртуальний хост обирається по IP-адресі і порту, на які прийшов запит
2. Якщо таких віртуальних хостів декілька, враховується `ServerName` [[Директиви Apache|директива]]
3. Якщо віртуальний хост не був знайдений по імені, то обирається перший в переліку із згаданими IP та портом.

## Див. також

- [[Віртуальні хости apache|віртуальні хости]]