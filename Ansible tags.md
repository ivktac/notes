---
date: 2025-07-14
title: Ansible tags
description: 
draft: false
tags:
  - devops/ansible
aliases: 
permalink: 
lang: uk
---

> [!tldr]
> **Теги** дозволяють виконувати лише певні частини [[ansible playbook|плейбука]].

> [!question] Навіщо?
> - частоково оновити
> - пропустити певні завдання
> - протестувати окремо компоненти

> [!example]
> ```bash
> ansible-playbook -i inventory.ini playbook.yml --tags "apache"
> ```

## Див. також

- [[Ansible variables]]