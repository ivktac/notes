---
created: 2025-07-14
title: Ansible Roles
tags:
  - ansible
aliases: 
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
