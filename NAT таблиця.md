---
created: 2025-08-06
title: NAT таблиця
tags:
  - network
  - nat
  - iptables
aliases: 
lang: uk
---
## Основні ланцюжки

- **PREROUTING** - DNAT (зміна адреси призначення)
- **POSTROUTING** - SNAT (зміна адреси джерела)
- **OUTPUT** - для локально генерованого трафіку

## Типи NAT

- **SNAT** - Source NAT (зміна адреси відправника)
- **DNAT** - Destination NAT (зміна адреси призначення)
- **MASQUERADE** - динамічний SNAT для змінних IP

## Приклади

- Masquerading для приватної мережі

```bash
iptables -t nat -A POSTROUTING -s 192.168.1.0/24 -o eth0 -j MASQUERADE
```

- Port forwarding

```bash
iptables -t nat -A PREROUTING -p tcp --dport 80 -j DNAT --to-destination 192.168.1.10:8080
```

## Див. також

- [[NAT]]
- [[Таблиці iptables]]