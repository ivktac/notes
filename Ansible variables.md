---
date: 2025-07-14
title: Ansible variables
description: 
draft: false
tags:
  - devops/ansible
aliases: 
permalink: 
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
## Див. також

- [[Ansible vault]]