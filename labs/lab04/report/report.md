---
## Front matter
title: "Лабораторная работа №4"
subtitle: "Архитектура компьютера"
author: "Казначеева Кристина Никитична"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучение процесса компиляции и сборки программ на ассемблере NASM.

# Задание

Этот практикум посвящена освоению языка ассемблера NASM. В ходе лабораторного работы мы познакомимся с основами программирования на ассемблере NASM. Мы создадим программу "Hello world!", узнаем, как работает транслятор NASM, освоим расширенные возможности командной строки NASM, научимся использовать компоновщик LD и запускать получившийся исполняемый файл.

# Выполнение лабораторной работы

Создадим каталог для работы с программами на языке ассемблера NASM, затем перейдём в него (рис. [-@fig:101]).

![Создание каталога и переход в него](image/101.png){#fig:101 width=70%}

Создадим текстовый файл с именем hello.asm (рис. [-@fig:102]).

![Создание текстового файла](image/102.png){#fig:102 width=70%}

Откроем этот файл с помощью gedit (рис. [-@fig:103]).

![Открытие файла с gedit](image/103.png){#fig:103 width=70%}

Введём в созданный текстовый файл текст (рис. [-@fig:104]).

![Ввод текста](image/104.png){#fig:104 width=70%}

Компилируем текст программы «Hello World» (рис. [-@fig:105]).

![Компиляция текста](image/105.png){#fig:105 width=70%}

Скомпилируем исходный файл hello.asm в obj.o  (рис. [-@fig:106]).

![Компиляция файла в obj.o](image/106.png){#fig:106 width=70%}

Передадим на обработку компоновщику объектный файл необходимо, чтобы получить исполняемую программу (рис. [-@fig:107]).

![Обработка файла компоновщиком](image/107.png){#fig:107 width=70%}

Ключ -o с последующим значением задаёт имя создаваемого исполняемого файла.
Выполним следующую команду (рис. [-@fig:108]):

![Выполнение команды с ключом -o](image/108.png){#fig:108 width=70%}

Запустим на выполнение созданный исполняемый файл, находящийся в текущем каталоге (рис. [-@fig:109]).

![Запуск файла на выполнение](image/109.png){#fig:109 width=70%}

В каталоге ~/work/arch-pc/lab04 с помощью команды cp создадим копию файла
hello.asm с именем lab4.asm (рис. [-@fig:110]).

![Создадие копию файла](image/110.png){#fig:110 width=70%}

С помощью gedit внесём изменения в текст программы в файле lab4.asm так, чтобы вместо Hello world! на экран выводилась строка с фамилией и именем (рис. [-@fig:111]).

![Изменение текста программы](image/111.png){#fig:111 width=70%}

Оттранслируем полученный текст программы lab4.asm в объектный файл (рис. [-@fig:112]). Выполняем
компоновку объектного файла и запустите получившийся исполняемый файл (рис. [-@fig:113]).

![Оттранслирование текста программы](image/112.png){#fig:112 width=70%}

![Запуск получившегося исполняемого файла](image/113.png){#fig:113 width=70%}

Скопируем файлы hello.asm и lab4.asm в локальный репозиторий в каталог ~/work/study/2023-2024/"Архитектура компьютера"/arch-pc/labs/lab04/ (рис. [-@fig:114]).

![Копирование файла в локальный репозиторий](image/114.png){#fig:114 width=70%}

Загрузим файлы на Github (рис. [-@fig:115]) и (рис. [-@fig:116]).

![Загрузка файлов на Github](image/115.png){#fig:115 width=70%}

![Загрузка файлов на Github](image/116.png){#fig:116 width=70%}

# Выводы

В ходе лабораторной работы мы получили практические навыки работы с ассемблером NASM, создали программу "Hello world!", изучили процесс компиляции и сборки с помощью транслятора NASM и компоновщика LD, а также разобрались с расширенными возможностями командной строки NASM.


