---
## Front matter
title: "Отчёт по лабораторной работе 6"
author: "Супонина Анастасия Павловна"

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

Ознакомиться с вычислением пределов, последовательностей и рядов в Octave. 

# Задание.

## Вычислить 

- Предел
- Частичные суммы
- Сумму ряда
- Интеграллы
- Аппроксимирование суммами

# Выполнение работы

## Предел

Записываю функцию f и @ обозначаю переменую данной функции, которую мы можем отдельно задавать и позднее изменять

![](photo/1.JPG)

Заднаю переменную и выполняю функцию с этой переменной

![](photo/2.1.JPG)

## Частичные суммы

Записываю значения вектора a

![](photo/2.2.JPG)

И в цикле от одного до десяти, суммирую i - значений 

![](photo/3.JPG)

Отобразила результат на графике

![](photo/4.JPG)

## Сумма ряда часть 1

Генерирую матрицу n, созначениями от 1 до 1000

![](photo/sum1.JPG)

Генерирую матрицу а

![](photo/sum2.JPG)

Считаю сумму и вывожу результат

![](photo/sum3.JPG)

## Вычисление интеграллов

Создаю функцию f и при помощи quad получаю значение интеграла от данной функции

![](photo/int.JPG)

## Аппроксимирование суммами

Создаю файл для вычисления аппроксимации первым способом

![](photo/approx1.JPG)

Сохраняю файл под названием midpoint и запускаю, чтобы в консоли увидеть результат выполнения

![](photo/approx2.JPG)
![](photo/approx3.JPG)

Создаю ещё один файл для вычисления аппроксимации вторым способом

![](photo/approx4.JPG)

Сохраняю файл под названием midpoint_v и запускаю, чтобы в консоли увидеть результат выполнения

![](photo/approx5.JPG)
![](photo/approx6.JPG)

Использую tic и toc, чтобы узнать время выполнения каждого файла и сравниваю результаты

![](photo/midpoint.JPG)
![](photo/res1.JPG)

![](photo/midpoint_v.JPG)
![](photo/res2.JPG)

Исходя из результатов мы можем сделать заключение, что второй способ для нахождения аппроксимации является более быстрым.

# Выводы

В процессе выполнения работы, я научилась вычислять пределы, последовательности и ряды в Octave.


