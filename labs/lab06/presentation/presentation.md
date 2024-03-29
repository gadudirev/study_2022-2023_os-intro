---
## Front matter
lang: ru-RU
title: Лабораторная работа
subtitle: Поиск файлов. Перенаправление ввода-вывода. Просмотр запущенных процессов
author:
  - Дудырев Г. А.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 11 марта 2023

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

Ознакомление с инструментами поиска файлов и фильтрации текстовых данных.
Приобретение практических навыков: по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.

## Ход выполнения

Первым делом нам необходимо, записать все файлы из каталога /etc и домашнего каталога в файл file.txt, 
для этого воспользуемся командой find с опцией -type f
![Работа команды find](image/1.jpg){width=70%}

## Ход выполнения

Теперь из файла file.txt нам надо найти все файлы, у которых расширение .conf, для этого применим команду grep
и перенаправим вывод в файд conf.txt
![Работа команды grep](image/2.jpg){width=70%}

## Ход выполнения

Теперь определим, какие файлы в нашем домашнем каталоге начинаются на "c", для этого в команде find укажем опцию -name, 
аргументом которой будет "*c", таким образом мы получим ожидаемый результат, но также можно воспользоваться командой ls,
конвейером и командой grep
![Поиск файлов по названию](image/3.jpg){width=70%}

## Ход выполнения

Запустим в фоновом режиме процесс, который будет записывать в файл ~/logfile
файлы, имена которых начинаются с log. Для этого воспользуемся командой find и укажем в конце &,
что запустит процесс в фоновом режиме. Удалим этот файл командой rm
![Запуск процесса в фоновом режиме](image/5.jpg){width=70%}

## Ход выполнения

Запустим gedit в фоновом режиме, используя команду ps, конвейер и grep, узнаем индентификатор процесса,
также это можно сделать используя команду jobs. Теперь с помощью команды kill и индентификатора завершим этот процесс
![Команды ps, jobs, kill](image/6.jpg){width=70%}

## Ход выполнения

Команда df показывает размер каждого смонтированного раздела диска(
![Команда df](image/7.jpg){width=70%}

## Ход выполнения

Команда du показывает число килобайт, используемое каждым файлом или каталогом
![Команда du](image/8.jpg){width=70%}

## Выводы

Были получены навыки работы с инструментами поиска файлов и фильтрации текстовых данных, а также по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.

