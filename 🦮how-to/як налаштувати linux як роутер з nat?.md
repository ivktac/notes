---
date: 2025-07-03
title: Як налаштувати Linux як Роутер з NAT?
description: 
draft: 
tags:
  - 🦮how-to
  - 🐧linux
  - os/network
aliases:
  - how to configure linux as router with nat
permalink: how-to-configure-linux-as-router-with-nat
lang: uk
---

1.  Дозволити переадрасацію IP:

```bash
sysctl -w net.ipv4.ip_forward
```

2. Налаштувати NAT:

```bash
iptables -t nat -A POSTROUTING -o <eth1> -j MASQUERADE
```

3. Дозволити трафік з eth1 до eth0:

```bash
iptables -A FORWARD -i <eth0> -o <eth1> -j ACCEPT 
```

4. Дозволити встановлені з'єднання з зовні

```bash
iptables -A FORWARD -i <eth1> -o <eth0> --ctstate RELATED,DESTABLISHED -j ACCEPT
```

5. Дропнути увесь інший трафік

```bash
iptables -A FORWARD -j DROP
```

## Див. також

- [[Роутер]]
- [[Налаштування Linux-машрутизатора]]
