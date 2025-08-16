---
created: 2025-07-14
title: Ansible variables
tags:
  - ansible
aliases: 
lang: uk
---

> [!tldr]
> **Змінні** дозволяють уникнути жорстко закодованих значень.

Можна визначити:

- Глобально в [[ansible playbook|playbook]]
- В [[Ansible inventory|інвенторії]] файлу
- В окремих файлах змінних

> [!example]
> ```yaml
> vars:
> 	apache_port: 8080
> ```
