---
created: "2025-08-06"
title: "LogFormat Apache"
tags: 
aliases: 
lang: uk
---

 **Директива** `LogFormat "%v %h %t %T %b (%r - %>s)" myfmt`

- `%v` — сервер
- `%h` — адреса клієнта
- `%t` — коли завітав
- `%T` — витрачений час
- `%b` — розмір відповіді
- `%r` — [[Види запитів http|запит]]
- `%>s` — [[Коди статусу HTTP|фінальний статус]]
- `myfmt` — назва формату

## Див. також

- [[Директиви Apache|apache directive]]
- [[Журналювання у Apache]]