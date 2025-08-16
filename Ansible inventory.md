---
created: 2025-07-14
title: Ansible inventory
tags:
  - ansible
aliases: 
lang: uk
---

> [!tldr]
> **Інвенторія (Inventory)** — це файл, що містить список машин для управління.


> [!tip] Машини можна групувати за ролями (напр. webservers, workstations, databases).

> [!example] Наприклад
> ```ini
> [webservers]
> 192.168.1.10
> 192.168.1.11
> 
> [workstations]
> 192.168.2.52
> 192.168.2.53
> 
> [databases]
> 192.168.3.5
> ```
