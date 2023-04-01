---
## Front matter
title: "Oтчёта по лабораторной работе"
subtitle: "Текстовый редактор vi"
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

Познакомиться с операционной системой Linux. Получить практические навыки рабо-
ты с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Выполнение лабораторной работы

Итак, для начала нам предлагается изучить теоретическую часть касательно редактора vi, в которой мы узнаем
основные команды и как переключаться между режимами vi. После изучения теории перейдем к выполнению задания.
Переместимся в каталог лабораторной работы номер 8, в откроем файл hello.sh, используя текстовый редактор vi(рис. @fig:001).

![Запуск файла в vi](image/1.jpg){#fig:001 width=70%}

В данном файле перейдем в режим вставки(клавиша i), вставим предложенный нам текст. Затем перейлем в командный режим(клавиша esc),
открываем последнюю строку(":"), сохраняем введенные нами изменения и выходим(команда wq)(рис. @fig:002).

![Работа с файлом в vi](image/2.jpg){#fig:002 width=70%}

Дадим пользователям права на выполнения нашего файла(команда chmod). И выполним наш файл. Как можно заметить на рисунке,
то наш код содержит ошибки, давайте их исправим(рис. @fig:003).

![Запуск файла](image/3.jpg){#fig:003 width=70%}

Снова откроем наш файл в редакторе vi, исправим HELL на HELLO, предварительно перейдя в режим вставки. Между словами можно переключаться
используя команду "w", теперь перейдем на строку, которая содержит LOCAL, и удалим это слово, используя команду "d". На его место впишем local.
Теперь скопируем предпоследнюю строку, команда "Y". Переместим курсор на последнюю строку, команда "G", и при помощи команды "p", вставим скопированную строку. Удалим последнюю строку, команда "d", и отменим последнее действие, команда "u". Сохраняем изменения и выходим.(рис. @fig:004).

![Изменение файла](image/4.jpg){#fig:004 width=70%}

Проверяем работу нашего файла и наблюдаем чудо))(рис. @fig:005).

![Запуск файла](image/5.jpg){#fig:005 width=70%}


# Выводы

Были получены практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.



