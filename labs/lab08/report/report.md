---
## Front matter
title: "Отчёт по лабораторной работе"
subtitle: "Поиск файлов. Перенаправление ввода-вывода. Просмотр запущенных процессов"
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

Ознакомление с инструментами поиска файлов и фильтрации текстовых данных.
Приобретение практических навыков: по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.

# Выполнение лабораторной работы

Первым делом нам необходимо, записать все файлы из каталога /etc и домашнего каталога в файл file.txt, 
для этого воспользуемся командой find с опцией -type f(рис. @fig:001).

![Работа команды find](image/1.jpg){#fig:001 width=70%}

Теперь из файла file.txt нам надо найти все файлы, у которых расширение .conf, для этого применим команду grep
и перенаправим вывод в файд conf.txt(рис. @fig:002).

![Работа команды grep](image/2.jpg){#fig:002 width=70%}

Теперь определим, какие файлы в нашем домашнем каталоге начинаются на "c", для этого в команде find укажем опцию -name, 
аргументом которой будет "*c", таким образом мы получим ожидаемый результат, но также можно воспользоваться командой ls,
конвейером и командой grep(рис. @fig:003).

![Поиск файлов по названию](image/3.jpg){#fig:003 width=70%}

Также найдем в каталоге /etc файлы, которые начинаются на "h"(рис. @fig:004).

![Поиск файлов по названию](image/4.jpg){#fig:004 width=70%}

Запустим в фоновом режиме процесс, который будет записывать в файл ~/logfile
файлы, имена которых начинаются с log. Для этого воспользуемся командой find и укажем в конце &,
что запустит процесс в фоновом режиме. Удалим этот файл командой rm(рис. @fig:005).

![Запуск процесса в фоновом режиме](image/5.jpg){#fig:005 width=70%}

Запустим gedit в фоновом режиме, используя команду ps, конвейер и grep, узнаем индентификатор процесса,
также это можно сделать используя команду jobs. Теперь с помощью команды kill и индентификатора завершим этот процесс(рис. @fig:006).

![Команды ps, jobs, kill](image/6.jpg){#fig:006 width=70%}

Команда df показывает размер каждого смонтированного раздела диска(рис. @fig:007).

![Команда df](image/7.jpg){#fig:007 width=70%}

Команда du показывает число килобайт, используемое каждым файлом или каталогом(рис. @fig:008).

![Команда du](image/8.jpg){#fig:008 width=70%}

Вывод всех директорий в домашнем каталоге, используя команду find(рис. @fig:009).

![Команда find](image/9.jpg){#fig:009 width=70%}

# Выводы

Были получены навыки работы с инструментами поиска файлов и фильтрации текстовых данных, а также по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.


