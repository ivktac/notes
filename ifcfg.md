---
date: 2025-07-16
title: Конфігураційний файл ifcg
description: 
draft: false
tags:
  - configuration
  - os/network
  - fixme
  - 🌱todo
aliases: 
permalink: 
lang: uk
---
> [!info] Конфігурації знаходяться у каталозі /etc/sysconfig/network-scripts #deprecated 

## Параметри

- `TYPE` - тип мережевого з'єднання
- `DEVICE` - назва мережевого пристрою
- `IPADDR` - IP-адреса
- `PREFIX` - розмір мережі (або NETMASK)
- `GATEWAY` - шлюз за замовчуванням
- `DNS1` - перший DNS-сервер
- `ONBOOT` - вмикати при старті системи
- `DEFROUTE` - використовувати шлюз цього пристрою
- `PEERDNS` - записувати DNS в /etc/resolv.conf

## Див. також

- [[nmcli]]