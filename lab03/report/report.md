---
## Front matter
title: "Лабораторная работа № 3"
subtitle: " Управляющие структуры"
author: "Пакавира Арсениу Висените Луиш"

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
lot: false # List of tables
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

Основная цель работы — освоить применение циклов функций и сторонних для Julia
пакетов для решения задач линейной алгебры и работы с матрицами.

# Задание

1. Используя Jupyter Lab, повторите примеры из раздела 3.2.
2. Выполните задания для самостоятельной работы (раздел 3.4)

# Теоретическое введение

Julia -- высокоуровневый свободный язык программирования с динамической типизацией, созданный для математических вычислений [@julialang]. Эффективен также и для написания программ общего назначения. Синтаксис языка схож с синтаксисом других математических языков, однако имеет некоторые существенные отличия.

Для выполнения заданий была использована официальная документация Julia [@juliadoc].

# Выполнение лабораторной работы

Для начала выполним примеры из лабораторной работы, чтобы познакомиться с циклами, условными операторами, функциями и работой со сторонними библиотеками (рис. [-@fig:001]-[-@fig:003]).

![Выполнение примеров с циклами](image/1.png){#fig:001 width=70%}

![Выполнение примеров с условными выражениями](image/2.png){#fig:002 width=70%}

![Выполнение примеров со сторонними библиотеками](image/3.png){#fig:003 width=70%}

Теперь перейдем к выполнению заданий для самостоятельной работы.

Используя циклы while и for (рис. [-@fig:004]-[-@fig:015]):

- выведем на экран целые числа от 1 до 100 и напечатаем их квадраты;
- создадим словарь squares, который будет содержать целые числа в качестве ключей и квадраты в качестве их пар-значений;
- создадим массив squares_arr, содержащий квадраты всех чисел от 1 до 100.

![Задание №1](image/4.png){#fig:004 width=70%}

![Задание №1](image/14.png){#fig:014 width=70%}

![Задание №1](image/15.png){#fig:015 width=70%}

Напишем условный оператор, который печатает число, если число чётное, и строку
«нечётное», если число нечётное. Перепишем код, используя тернарный оператор (рис. [-@fig:005]).

![Задание №2](image/5.png){#fig:005 width=70%}

Напишем функцию add_one, которая добавляет 1 к своему входу (рис. [-@fig:006]).

![Задание №3](image/6.png){#fig:006 width=70%}

Используем map() или broadcast() для задания матрицы 𝐴, каждый элемент которой увеличивается на единицу по сравнению с предыдущим. (рис. [-@fig:007])

![Задание №4](image/7.png){#fig:007 width=70%}

Зададим матрицу A. Найдем A^3. Заменим третий столбец матрицы 𝐴 на сумму второго и третьего столбцов (рис. [-@fig:008]).

![Задание №5](image/8.png){#fig:008 width=70%}

Задание 6 (рис. [-@fig:016])

![Задание №6](image/16.png){#fig:016 width=70%}

Задание 7 (рис. [-@fig:017])

![Задание №7](image/17.png){#fig:017 width=70%}

Напишем свою функцию, аналогичную функции outer() языка R. Функция
должна иметь следующий интерфейс: `outer(x,y,operation)` (рис. [-@fig:009],[-@fig:010]).

![Реализация функции outer()](image/9.png){#fig:009 width=70%}

![Проверка работы функции outer()](image/10.png){#fig:010 width=70%}

Решим систему линейных уравнений с 5 неизвестными (рис. [-@fig:011]). 

![Решение систему линейных уравнений](image/11.png){#fig:011 width=70%}

В 10 задании произведем анализ количества элементов матрицы, удовлетворяющих необходимым условиям (рис. [-@fig:012]). 

![Задание №10](image/12.png){#fig:012 width=70%}

Вычислим выражения (рис. [-@fig:013]).

![Задание №11](image/13.png){#fig:013 width=70%}

# Выводы

В результате выполнения данной лабораторной работы я освоил применение циклов функций и сторонних для Julia
пакетов для решения задач линейной алгебры и работы с матрицами.

# Список литературы{.unnumbered}

::: {#refs}
:::
