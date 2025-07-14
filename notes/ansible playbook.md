---
date: 2025-07-14
title: Плейбук
description: 
draft: false
tags:
  - devops/ansible
aliases:
  - ansible плейбуки
  - плейбуки
  - плейбук
  - playbook
permalink: 
lang: uk
---

> [!tldr]
> **Playbook** - це [[YAML]]-файл, що описує завдання для різних груп машин.
> 

> [!info] Кожен playbook містить:
> - Цільові хости (hosts)
> - Список завдань (tasks)
> - *Опціонально: змінні, обробники подій*

> [!question]- Як запустити?
> ```bash
> ansible-playbook -i inventory.ini playbook.yml
> ```
> 
> Після запуску можна йти пити каву - [[Ansible]] все зробить сам. :)))

> [!tip] Краще створювати окремі playbooks для логічних завдань: (один для веб-серверу, інший для БД і так далі)
## Див. також

- [[Ansible inventory]]
- [[Ansible Tasks]]