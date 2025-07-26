---
date: 2025-07-25
title: Простір імен
description: 
draft: false
tags:
  - devops/containerzation
  - api/linux
  - os/🐧linux
aliases: 
permalink: 
lang: uk
---


> [!tldr]
> **Простір імен** це абстракція над глобальними системними ресурсами, яка дозволяє [[процес|процесам]] в просторі імен мати власний ізольований екземпляр глобального ресурсу.

![[linux namespaces.png|linux namespacaes]]

> [!warning] Зміни в глобальному ресурсі видимі для процесів, які є членами простору імен, але невидимі для інших просторів імен.
