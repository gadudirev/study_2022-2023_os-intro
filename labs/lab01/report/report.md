---
## Front matter
title: "Отчёта по лабораторной работе"
subtitle: "Установка OC Linux"
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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

Установить OC Linux на виртуальную машину

# Выполнение лабораторной работы

Создадим каталог для виртуальных машин используя команду mkdir(рис. @fig:001).

![Создание каталога для вирт. машин](image/1.png){#fig:001 width=70%}

Далее настроим путь для виртуальных машин в VirtualBox(рис. @fig:002).

![Настройка VirtualBox](image/2.png){#fig:002 width=70%}

А также настроим хост-клавишу(рис. @fig:003).

![Настройка VirtualBox](image/3.png){#fig:003 width=70%}

Теперь перейдем к установке виртуальной машины, прописываем имя и выбираем iso образ(рис. @fig:004).

![Установка VirtualBox](image/4.png){#fig:004 width=70%}

Устанавливаем основную память(рис. @fig:005).

![Выбор основной памяти](image/5.png){#fig:005 width=70%}

Затем настраиваем виртуальный жесткий диск(рис. @fig:006).

![Настройка жесткого диска](image/6.png){#fig:006 width=70%}

Выбираем размер видеопамяти (рис. @fig:007).

![Размер видеопамяти](image/7.png){#fig:007 width=70%}

Теперь виртуальная машина готова к запуску.
После запуска необходимо выбрать WIN модификатор и используя команду "win + enter" открыть терминал, в терминале запускаем liveinst(забыл сделать скриншот)

Теперь займемся установкой системы на диск, выбираем язык, настраиваем часовой пояс, устанавливаем имя и пароль для Нашего пользователя и пользователя root, запускаем установку(рис. @fig:009). 

![Установка ОС](image/9.png){#fig:009 width=70%}

После установки необходимо извлечь образ(рис. @fig:010).

![Извлечение образа](image/10.png){#fig:010 width=70%}

Теперь система готова к запуску.
Для дальнейшей работы необходимо установить программное обеспечение, так как я проходил курс "Архитектура компьютера", то у меня уже все настроено и загружено, поэтому перейдем сразу к выполнению домашнего задания.

#Домашнее задание

1)Проанолизировать последовательность загрузки системы(рис. @fig:011).

![Извлечение образа](image/11.png){#fig:011 width=70%}

Используя команду dmesg | grep -i "то, что ищем"
Получите следующую информацию.

1.Версия ядра Linux (Linux version)(рис. @fig:011).

![Linux Version](image/11.png){#fig:011 width=70%}

2.Частота процессора (Detected Mhz processor).

![Mhz](image/11.png){#fig:011 width=70%}

3.Модель процессора (CPU0)(рис. @fig:011).

![CPU0](image/11.png){#fig:011 width=70%}

4.Объём доступной оперативной памяти (Memory available)(рис. @fig:011).

![Memory](image/11.png){#fig:011 width=70%}

5.Тип обнаруженного гипервизора (Hypervisor detected)(рис. @fig:011).

![Hypervisor](image/11.png){#fig:011 width=70%}

6.Тип файловой системы корневого раздела(рис. @fig:011).

![File system](image/11.png){#fig:011 width=70%}

7.Последовательность монтирования файловых систем(рис. @fig:011).

![Fyle system](image/11.png){#fig:011 width=70%}

# Выводы

Были получены навыки работы с VirtualBox и OC Linux, а именно мы научились устанавливать ОС на виртуальную машину 


