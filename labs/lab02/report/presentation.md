---
## Front matter
lang: ru-RU
title: Лабароторная работа
subtitle: Установка OC Linux
author:
  - Дудырев Глеб Андреевич
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 15 февраля 2023

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---






## Цель

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

## Ход работы

Перед началом работы необходимо настроить VirtualBox, указать путь для виртуальных машин и задать хост-клавишу.

![Настройка VirtualBox](image/2.png){#fig:002 width=70%}

![Настройка VirtualBox](image/3.png){#fig:003 width=70%}

## Ход работы

Теперь перейдем к процессу создания виртуальной машины, в ходе которого надо будет произвести некоторые настройки: настройка жесткого диска и т.д.

![Настройка жесткого диска](image/6.png){#fig:006 width=70%}

## Ход работы

После того как виртуальная машина будет создана необходимо ее запустить, и начать установку ОС, задать начальные настройки и создать пользователей

![Установка ОС](image/9.png){#fig:009 width=70%}

## Ход работы

После завершения установки необходи извечь образ

![Извлечение образа](image/10.png){#fig:010 width=70%}

## Ход работы

Теперь после запуска вирутальной машины, надо загрузить программное обеспечение, но так. как. я проходил курс "Архитектура компьютера", то у меня уже есть необходимое ПО, поэтому я его не загружал.

## Вывод

Были получены навыки работы с VirtualBox и OC Linux, а именно мы научились устанавливать ОС на виртуальную машину 

