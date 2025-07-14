---
date: 2025-07-13
title: Основи роботи з MySQL
description: 
draft: false
tags:
  - databases/mysql
aliases: 
permalink: 
lang: uk
---

## Довідка

[[MySQL]] має вбудовану систему довідки, доступну через команди:

- `\h` - загальна довідка
- `HELP 'search_string'` - пошук по темах
- `HELP 'data types'` - довідка по типах даних
- `HELP 'create table'` - довідка по створенню таблиць

## SQL Команди у MySQL

> [!info] Усі [[SQL]] команди у MySQL:
> - закінчуються символом `;`
> - ключові слова нечутливі до регістру
> - можна писати в кілька рядків
> - можна виконувати послідовність запитів через `;`

> [!tip] Щоб відмінити команду: `\c`

## Робота з БД

- `SHOW DATABASES` - список всіх баз даних
- `USE database_name` - вибір активної БД
- `CREATE DATABASE` - створення БД
- `DROP DATABASE` - видалення БД

## Робота з таблицями

- `SHOW TABLES` - список таблиць в БД
- `DESC table_name` - опис структури таблиці
- `SHOW CREATE TABLE` - команда створення таблиці
- `CREATE TABLE` - створення таблиці
- `DROP TABLE` - видалення таблиці
- `TRUNCATE TABLE` - видалення всіх рядків

## Див. також

- [[Числові типи даних у MySQL]]
- [[SQL]]
- [[SELECT]]
