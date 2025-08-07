---
created: 2025-08-06
title: Конфігураційні файли для DNS у Linux
tags:
  - network
  - config
  - linux
aliases:
  - configure dns in linux
lang: uk
---
##  /etc/nsswitch.conf
> [!info] загальні налаштування вибору систем для резолву імен)

- вибирає систему для резолву
- визначає порядок систем
- можна налаштувати для різних типів даних

> [!note]- системи резолву
> - `files` — брати з `/etc/hosts`
>- `dns` — використовувати dns-службу

## /etc/hosts

> [!info] локальні налаштування вирішення імен, локальний DNS


> [!example] Формат
> `192.168.5.5 domain1.com domain2.ua`

> [!question]- Як працює?
> При зверненні до domain1.com або domain2.ua, трафік направляється на IP 192.168.5.5.

> [!tip] Можна встановити приорітет над [[DNS]] (у /etc/nsswitch.conf)

## /etc/resolv.conf

> [!info] перелік DNS-серверів для вирішення імен

> [!example] Формат
> ```
> nameserver 8.8.8.8
> nameserver 8.8.4.4
> search google.com gearxxed.com
> ```

Дозволяє підстановку піддоменів: `ping docs` → `ping docs.gearxxed.com`