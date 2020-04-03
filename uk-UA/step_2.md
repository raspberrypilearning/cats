## Малювання ліній

\--- task \---

Відкрий початковий проєкт "КОТИ!" у Скретч.

**Онлайн:** відкрий стартовий проєкт на [rpf.io/cats-on](http://rpf.io/cats-on){:target="_ blank"}.

Якщо у тебе є обліковий запис Скретч, то ти можеш зробити його копію, натиснувши **Ремікс**.

**Офлайн:** відкрий [початковий проєкт](http://rpf.io/p/en/cats-go) в офлайн-редакторі. Якщо тобі треба завантажити та встановити офлайн-редактор Скретч, то ти можеш його знайти на [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Додай розширення Олівець до свого проєкту.

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

Клацни на спрайт з назвою "Олівець" та додай код, щоб встановити колір того ж відтінку синього, що й перешкоди на сцені.

![Спрайт олівець](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Щоб вибрати колір, натисни на кольоровий квадрат у `надати олівцю колір`{:class="block3extensions"}, та вибери піпетку, а потім натисни нею на потрібний колір на сцені.

\--- /task \---

\--- task \---

Додай ще деякий код, щоб спрайт рухався за вказівником миші. Протестуй свою програму, для перевірки правильності коду.

![Спрайт олівець](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Додай код, щоб спрайт міг намалювати лінії на сцені, якщо натиснута кнопка миші.

![Спрайт олівець](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`Якщо`{:class="block3control"} `мишку натиснуто?`{:class="block3sensing"}, то `опустити олівець`{:class="block3extensions"} `інакше`{:class="block3control"}, ` підняти олівець`{:class="block3extensions"}.

\--- /hint \---

\--- hint \---

Ось необхідні тобі блоки коду:

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

\--- /hint \---

\--- hint \---

Ось як має виглядати твій код:

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
forever
go to (mouse pointer v)
+ if <mouse down?> then
pen down
else
pen up
end
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Протестуй свій код. Ти повинен (-на) мати можливість клікнути й перетягнути мишку, для малювання лінії на сцені.

![Намалювати лінію](images/draw-a-line.png)

\--- /task \---

Напевно, ти бачиш, що синя крапка завжди з’являється у верхньому правому куті сцени (це проілюстровано на зображенні зверху). Це тому, що, коли ти натискаєш зелений прапорець, щоб почати гру, ти натискаєш кнопку миші, і олівець негайно починає малювати.

\--- task \---

Щоб цього уникнути додай блок `підняти олівець`{:class="block3extensions"} на початку скрипта, а `чекати 1 секунд`{:class="block3control"} перед блоком `завжди`{:class="block3control"}.

![Спрайт олівець](images/pen-sprite.png)

```blocks3
when flag clicked
+ pen up
set pen color to [#0000ff]
erase all
set pen size to (5)
+ wait (1) seconds
forever
go to (mouse pointer v)
if <mouse down?> then
pen down
else
pen up
end
```

\--- /task \---