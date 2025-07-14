---
date: 2025-07-14
title: Ansible Roles
description: 
draft: false
tags:
  - devops/ansible
aliases: 
permalink: 
lang: uk
---
> [!tldr]
> **Roles** - це спосіб організації [[ansible tasks|завдань]] у повторно використовувані компоненти. 

> [!tip] Кожна роль має власну структуру директорій для завдань, змінних, обробників.

```yaml
- hosts: workstations
  tasks:
    - name: Include Powershell roll
      include_role:
          name: powershell
```

## Див. також

- [[ansible playbook]]