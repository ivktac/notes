---
created: 2025-07-14
title: ansible playbook
tags:
  - ansible
aliases: 
lang: uk
---

> [!tldr]
> **Playbook** - це [[YAML]]-файл, що описує [[ansible tasks|завдання]] для різних груп машин.
> 

Кожен playbook містить:
 - Цільові хости (hosts)
 - Список завдань (tasks)
 - *Опціонально: змінні, обробники подій*

> [!question]- Як запустити?
> ```bash
> ansible-playbook -i inventory.ini playbook.yml
> ```
> 
> Після запуску можна йти пити каву - [[Ansible]] все зробить сам. :)))

> [!tip] Краще створювати окремі playbooks для логічних завдань: (один для веб-серверу, інший для БД і так далі)

Плейбуки можуть викликати інші плейбуки
 
 > [!example]
> ```yaml
> - hosts: localhost
>   tasks:
> 	 - name: Run common setup tasks
> 	   include_tasks: common_setup.yml
> ```



## Див. також

- [[Ansible inventory]]
