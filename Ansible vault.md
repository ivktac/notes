---
created: 2025-08-06
title: Ansible vault
tags:
  - ansible
aliases: 
lang: uk
---
> [!tldr]
> **Ansible Vault** дозволяє шифрувати чутливі дані (паролі, API ключі).

Створити:

```bash
ansible-vault create secrets.yml
```

Використовувати:

```bash
ansible-playbook -i inventory.ini playbook.yml --ask-vault-pass
```
