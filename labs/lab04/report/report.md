---
## Front matter
title: "Лабораторная работа"
subtitle: "Основы интерфейса взаимодействия
пользователя с системой Unix на уровне командной строки"
author: "Дудырев Глеб Андреевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение навыков взаимодействия пользователя с системой посредством командной строик

# Выполнение лабораторной работы

Откроем терминал, в котором будем выполнять нашу работу.
Первым делом нам предлагают узнать полное имя домашнего каталога, для этого перейдем в него (команда cd),
затем, используя команду pwd, узнаем полное имя домашнего каталога(рис. @fig:001).

![Работа команды pwd](image/1.jpg){#fig:001 width=70%}

Иногда есть необходимость посмотреть содержимое каталога, для этого существует команда ls, посмотрим, как она работает.
Перейдем в каталог /tmp и вызовем команду ls(рис. @fig:002).

![Работа команды ls](image/3.jpg){#fig:002 width=70%}

У команды ls существует различные опции, которые добавляют доп. функционал, так ,например, опция -а дополнительно выводит скрытые файлы(рис. @fig:003).

![Работа команды ls, опция -а](image/2.jpg){#fig:003 width=70%}

Существует возможность одновременно применить несколько опций, команда ls -alF, выведет все объекты каталога, в том числе скрытые, подробную информацию об этих объектах и их тип.(рис. @fig:004).

![Работа команды ls, опция -alF](image/6.jpg){#fig:004 width=70%}

Теперь нам предлагает узнать, есть ли в каталоге /var/spool подкаталог cron. В моем случае такого подкаталога не существует.(рис. @fig:005).

![Просмотр содержимого /var/spool](image/7.jpg){#fig:005 width=70%}

Давайте узнаем, какие каталоги содержит домашний каталог, а также кто является владельцем этих каталогов.
Воспользуемся командой ls -l(рис. @fig:006).

![Просмотр содержимого '~'](image/8.jpg){#fig:006 width=70%}

Следующим шагом научимся создавать и удалять каталоги. Создадим каталог newdir, для этого существует команда mkdir(рис. @fig:007).

![Создание newdir](image/9.jpg){#fig:007 width=70%}

А в нем подкаталог morefun(рис. @fig:008).

![Создание morefun](image/10.jpg){#fig:008 width=70%}

Можно одной командой создавать несколько каталогов одновременно, для этого необходимо через пробел перечислить названия этих каталогов. Создадим каталоги letters, memos, misk. Теперь удалим эти каталоги, используя команду rmdir(рис. @fig:009).

![Создание нескольких каталогов](image/11.jpg){#fig:009 width=70%}

Попробуем с помощью команды rm удалить каталог newdir, у нас не получится, потому что это каталог. Чтобы удалить каталог необходимо использовать опцию -r, которая удаляет каталоги и все их содержимое(рис. @fig:010).

![Удаление newdir](image/12.jpg){#fig:010 width=70%}

Чтобы узнать подробную информацию о команде и ее опциях, можно воспользоваться командой man.
Давайте с помощью команды man узнаем, какая опция команды ls выводит содержимое всех подкаталогов относительно нашего каталога. Для этого используется опция -R(рис. @fig:011).

![Команда man](image/13.jpg){#fig:011 width=70%}

С помощью команды man узнаем как вывести отсортированный по времени создания список содержимого каталога. Для этого нам понадобится опция -t(рис. @fig:012).

![Команда man](image/14.jpg){#fig:012 width=70%}

Также используем man для cd, pwd, mkdir, rmdir, rm.(рис. @fig:013).

![Команда man](image/15.jpg){#fig:013 width=70%}

Команда history, выводит упорядоченный список команд обращений к командной строке(рис. @fig:014).

![Команда history](image/16.jpg){#fig:014 width=70%}

Выполним модификацию и исполнение команды из буфера обмена команд(рис. @fig:015).

![Модификация команды](image/17.jpg){#fig:015 width=70%}

# Выводы

Были получены навыки работы с системой посредством командной строки.


