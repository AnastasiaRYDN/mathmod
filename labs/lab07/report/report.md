---
## Front matter
title: "Лабораторная работа №7"
subtitle: "Математическое моделирование"
author: "Данилова Анастасия Сергеевна"

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

Решить задачу об эффективности рекламы, используя при этом Julia и OpenModelica. 

# Задание

Постройте график распространения рекламы, математическая модель которой описывается
следующим уравнением:

1. $\frac{dn}{dt}=(0.89+0.000015n(t))(N-n(t))$

2. $\frac{dn}{dt}=(0.000015+0.82n(t))(N-n(t))$

3. $\frac{dn}{dt}=(sin(9t)+0.3sin(4t)n(t))(N-n(t))$

При этом объем аудитории
N = 1500, в начальный момент о товаре знает 15 человек. Для
случая 2 определите в какой момент времени скорость распространения рекламы будет
иметь максимальное значение.

# Теоретическое введение

Математическая модель распространения рекламы описывается
уравнением:

$\frac{dn}{dt}=(\alpha_1(t)+\alpha_2(t)n(t))(N-n(t))$

Модель рекламной кампании описывается следующими величинами.
Считаем, что $\frac{dn}{dt}$ - скорость изменения со временем числа потребителей,
узнавших о товаре и готовых его купить,
t - время, прошедшее с начала рекламной
кампании,
n(t) - число уже информированных клиентов. Эта величина
пропорциональна числу покупателей, еще не знающих о нем, это описывается
следующим образом: $\alpha_1(t)(N-n(t))$, где
N - общее число потенциальных платежеспособных покупателей, $\alpha_1(t) > 0$ - характеризует интенсивность
рекламной кампании (зависит от затрат на рекламу в данный момент времени).
Помимо этого, узнавшие о товаре потребители также распространяют полученную
информацию среди потенциальных покупателей, не знающих о нем (в этом случае
работает т.н. сарафанное радио). Этот вклад в рекламу описывается величиной
$\alpha_2(t)n(t)(N-n(t))$, эта величина увеличивается с увеличением потребителейузнавших о товаре.

# Выполнение лабораторной работы

![1Modelica](image/photo_1.jpg)

![1 результат](image/photo_2.jpg)

![Julia](image/photo_8.jpg)

![1 результат](image/photo_9.jpg)

![2Modelica](image/photo_3.jpg)

![2 результат](image/photo_4.jpg)

![Максимальная скорость](image/photo_5.jpg)

![Julia](image/photo_10.jpg)

![2 результат](image/photo_11.jpg)

![3Modelica](image/photo_7.jpg)

![3 результат](image/photo_6.jpg)

![Julia](image/photo_12.jpg)

![3 результат](image/photo_13.jpg)

# Выводы

Мы решили задачу об эффективности рекламы, рассмотрели 3 разных графика эффективности рекламы, используя при этом Julia и OpenModelica.

# Список литературы

1. Эффективность рекламы // URL: https://esystem.rudn.ru/pluginfile.php/1971741/mod_resource/content/2/Лабораторная%20работа%20№%206.pdf (дата обращения: 25.03.2023).