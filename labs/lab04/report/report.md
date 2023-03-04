---
## Front matter
title: "Математическое моделирование"
subtitle: "Лабораторная работа №4"
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

Построить фазовый портрет гармонического осциллятора и решение уравнения
гармонического осциллятора с помощью языков: Julia и Modelica

# Задание

**Вариант 15**

Постройте фазовый портрет гармонического осциллятора и решение уравнения
гармонического осциллятора для следующих случаев
1. Колебания гармонического осциллятора без затуханий и без действий внешней
силы 

    $\ddot{x}+7.5x=0\\$
2. Колебания гармонического осциллятора c затуханием и без действий внешней
силы
    $\ddot{x}+5\dot{x}+7x=0\\$

3. Колебания гармонического осциллятора c затуханием и под действием внешней
силы
    $\ddot{x}+4\dot{x}+2x=5sin(t)\\$

На интервале
t [0;40] (шаг 0.05) с начальными условиями: $x_{0} = 0, y_{0} =-1$



# Теоретическое введение

Техника и окружающий мир являются примерами того, что существуют такие процессы, которые повторяются через определенные промежутки времени, то есть периодически. Их называют **колебательными**.

Действия внутренних сил системы после выведения из равновесия порождают свободные колебания, простейшим видом колебаний являются **гармонические колебания**.


Движение грузика на пружинке, маятника, заряда в электрическом контуре, а
также эволюция во времени многих систем в физике, химии, биологии и других
науках при определенных предположениях можно описать одним и тем же
дифференциальным уравнением, которое в теории колебаний выступает в качестве
основной модели. Эта модель называется линейным гармоническим осциллятором.

Уравнение свободных колебаний гармонического осциллятора имеет
следующий вид:

 $$\dot{x}+2\gamma\dot{x}+\omega_{0}^2x=0\\$$

 x – переменная, описывающая состояние системы (смещение грузика, заряд
конденсатора и т.д.), $\gamma$ – параметр, характеризующий потери энергии (трение в механической системе, сопротивление в контуре),
$\omega_{0}$ – собственная частота
колебаний, t – время. 
(Обозначения
$\ddot{x}= \frac{d^2x}{dt^2}, \dot{x}= \frac{dx}{dt}$
)

Независимые переменные x, y определяют пространство, в котором
«движется» решение. Это фазовое пространство системы, поскольку оно двумерно
будем называть его фазовой плоскостью.

# Выполнение лабораторной работы

1. Колебания гармонического осциллятора без затуханий и без действий внешней
силы 

    $\ddot{x}+7.5x=0\\$

 ![Код OM 1 случай](image/%D1%80%D0%B8%D1%811.jpg)

 ![Результат](image/%D1%80%D0%B8%D1%812.jpg)

 ![Фазовый портрет](image/%D1%80%D0%B8%D1%813.jpg)

 ![Julia 1 случай](image/%D1%80%D0%B8%D1%8110.jpg)

 ![Результат](image/%D1%80%D0%B8%D1%8111.jpg)

2. Колебания гармонического осциллятора c затуханием и без действий внешней
силы
    $\ddot{x}+5\dot{x}+7x=0\\$

![2 случай OM](image/%D1%80%D0%B8%D1%814.jpg)

![Результат](image/%D1%80%D0%B8%D1%815.jpg)

![Фазовый портрет](image/%D1%80%D0%B8%D1%816.jpg)

![Julia 2 случай](image/%D1%80%D0%B8%D1%8112.jpg)

![Результат](image/%D1%80%D0%B8%D1%8113.jpg)

3. Колебания гармонического осциллятора c затуханием и под действием внешней
силы
    $\ddot{x}+4\dot{x}+2x=5sin(t)\\$

![3 случай OM](image/%D1%80%D0%B8%D1%817.jpg)

![Результат](image/%D1%80%D0%B8%D1%818.jpg)

![Фазовый портрет](image/%D1%80%D0%B8%D1%819.jpg)

![Julia 3 случай](image/%D1%80%D0%B8%D1%8114.jpg)

![Результат](image/%D1%80%D0%B8%D1%8115.jpg)


# Выводы

Мы построили фазовый портрет гармонического осциллятора и решили уравнения
гармонического осциллятора с помощью языков: Julia и Modelica

# Список литературы

1. Гармонические колебания // URL: https://zaochnik.com/spravochnik/fizika/mehanicheskie-kolebanija/garmonicheskie-kolebanija/ (дата обращения: 04.03.2023). 
2. Модель гармонических колебаний // URL: https://esystem.rudn.ru/pluginfile.php/1971729/mod_resource/content/2/Лабораторная%20работа%20№%203.pdf (дата обращения: 04.03.2023).
