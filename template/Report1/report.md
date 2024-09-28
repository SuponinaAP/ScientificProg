---
## Front matter
title: "Отчёт по лабораторной работе 1"
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

Ознакомиться с системой контроля версий git. Изучить базовые конфигурации и научиться вносить изменения в репозиторий при помощи функций git.

# Задание

1) Создать базовую конфигурацию для работы с git.
2) Создать ключ SSH.
3) Создать ключ PGP.
4) Настроить подписи git.
5) Зарегистрироваться на Github.
6) Создать локальный каталог для выполнения заданий по предмету.

# Теоретическое введение

## Базовая настройка git

git config --global user.name "Name Surname" - задает имя владельца репозитория 

git config --global user.email "work@mail" - задает email владельца репозитория 

git config --global core.quotepath false - настройка utf-8 в выводе сообщений git

git config --global init.defaultBranch master - задает имя начальной ветки

git config --global core.autocrlf input - настройка параметра autocrlf

git config --global core.safecrlf warn - настройка параметра safecrlf

## Команды для создания ключей ssh

ssh-keygen -t rsa -b 4096 - по алгоритму rsa с ключём размером 4096 бит

ssh-keygen -t ed25519 - – по алгоритму ed25519

## Команды для работы с ключами gpg

gpg --full-generate-key - генерация gpg ключа с настройками

gpg --list-secret-keys --keyid-format LONG - вывод списка ключей

gpg --armor --export <PGP Fingerprint> | xclip -sel clip - копирование ключа в буфер обмена

## Команды для настройки автоматических подписей коммитов git

git config --global user.signingkey <PGP Fingerprint>

git config --global commit.gpgsign true

git config --global gpg.program $(which gpg2)

## Для настройки каталога курса

cd - переход в нужную папку

make - создание новой папки/файла

rm - удаление ненужной папки/файла 

***Отправка файлов на сервер:***

git add .

git commit -am 'feat(main): make course structure'

git push


# Выполнение лабораторной работы

1) Создать базовую конфигурацию для работы с git. (рис. [-@config1])(рис. [-@config2])
Описываются проведённые действия, в качестве иллюстрации даётся ссылка на иллюстрацию (рис. [-@fig:001]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:001 width=70%}

# Выводы

Здесь кратко описываются итоги проделанной работы.

# Список литературы{.unnumbered}

::: {#refs}
:::
