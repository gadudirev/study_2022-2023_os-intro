---
## Front matter
title: "Отчет по лабораторной работе"
subtitle: "Анализ файловой системы Linux. Команды для работы с файлами и каталогами"
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

Ознакомление с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобретение практических навыков по применению команд для работы
с файлами и каталогами, по управлению процессами (и работами), по проверке исполь-
зования диска и обслуживанию файловой системы.

# Выполнение лабораторной работы

Для начала выполним все примеры, которые предлагаются в начале лабораторной работе, я не добавляю скриншоты и описание процесса выполнения этих примеров, так как в лабораторной работе этого не требовалось, то как я выполнял эти примеры, вы моможете посмотреть в скринкасте к лабораторной работе.

Итак, нам предлагают скопировать файл в домашний каталог и переименовать его в equipment, команда cp(рис. @fig:001).

![Копипрование файла](image/1.jpg){#fig:001 width=70%}

Далее в домашнем каталоге создадим директорию ski.places и переместим туда файл equipment, переименовав в equiplist, команда mv(рис. @fig:002).

![Перемещение и изменение имени файла](image/2.jpg){#fig:002 width=70%}

Теперь, используя команду touch, создадим файл abc1 и уже с помощью знакомым нам командам переместим его в ski.places, переименовав в equiplist2(рис. @fig:003).

![Работа с файлом abc1](image/3.jpg){#fig:003 width=70%}

Создадим каталог ~/ski.places/equipment и переместим раннее созданные файлы в него, используя команду mv(рис. @fig:004).

![Работа с каталогом ~/ski.places/equipment](image/4.jpg){#fig:004 width=70%}

Создадим каталог ~/newdir и переместим его в каталог ski.places, переименовав в plans(рис. @fig:005).

![Работа с каталогом ~/newdir](image/5.jpg){#fig:005 width=70%}

Создадим каталоги и файлы australia, play, my_os, feathers. Зададим им права доступа как в лабораторной работе.
Для каталога australia команда будет выглядеть следующим образом: chmod 744 australia (рис. @fig:006).

![Определение прав доступа](image/6.jpg){#fig:006 width=70%}

Для каталога play: chmod 711 play(рис. @fig:007).

![Определение прав доступа](image/7.jpg){#fig:007 width=70%}

Для файла my_os: chmod 544 my_os
Для файла feathers: chmod 664 feathers(рис. @fig:008).

![Определение прав доступа](image/8.jpg){#fig:008 width=70%}

Нам предлагается проверить содержимое файла /etc/password, забыл сделать скриншот, но для этого можно воспользоваться командой cat.
Скопируем файл feathers в файл file.old(команда cp), а затем переместим файл file.old в каталог play(команда mv)(рис. @fig:009).

![Работа с файлом feathers](image/9.jpg){#fig:009 width=70%}

Теперь скопируем каталог play в каталог fun, используя опцию -r, затем перепестим каталог fun в каталог play/games(рис. @fig:010).

![Работа с каталогом play](image/10.jpg){#fig:010 width=70%}

Также нам предлагается лишить владельца файла feathers прав на чтение. После этого у нас не получится просмотреть или скопировать его содержимое.
Затем на предлагают лишить владельца каталога play прав на выполнение, после этого мы не сможем в него перейти.
После выполненных действий вернем отнятые раннее права.(рис. @fig:011).

![Работа с правами доступа](image/11.jpg){#fig:011 width=70%}

В конце необходимо с помощью команды man посмотреть команды mount, fsck, mkfs, kill(рис. @fig:012).

![Работа с правами доступа](image/12.jpg){#fig:012 width=70%}

# Выводы

Были получены навыки работы с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобретены практические навыки по применению команд для работы
с файлами и каталогами, по управлению процессами (и работами), по проверке исполь-
зования диска и обслуживанию файловой системы.



