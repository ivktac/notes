---
date: 2025-07-14
title: Ansible vault
description: 
draft: false
tags:
  - devops/ansible
aliases: 
permalink: 
lang: uk
---
**Ansible Vault** дозволяє шифрувати чутливі дані (паролі, API ключі).

Створити:

```bash
ansible-vault create secrets.yml
```

Використовувати:

```bash
ansible-playbook -i inventory.ini playbook.yml --ask-vault-pass
```

## Див. також

- [[Ansible variables]]