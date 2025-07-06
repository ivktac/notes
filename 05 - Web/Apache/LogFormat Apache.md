---
date: 2025-07-04
title: Формат журналювання доступу в Apache
description: 
draft: 
tags:
  - configuration
  - web/apacahe
aliases:
  - logformat apache
permalink: apache-logformat
lang: uk
---

> [!info] **Директива** `LogFormat "%v %h %t %T %b (%r - %>s)" myfmt`
> 
>- `%v` — сервер
> - `%h` — адреса клієнта
> - `%t` — коли завітав
> - `%T` — витрачений час
> - `%b` — розмір відповіді
> - `%r` — [[Види запитів http|запит]]
> - `%>s` — [[Коди статусу HTTP|фінальний статус]]
> - `myfmt` — назва формату

## Див. також

- [[Директиви Apache|apache directive]]
- [[Журналювання у Apache]]