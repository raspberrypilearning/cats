## Нарисуй линии

\--- task \---

Открой стартовый проект «КОТЫ».

**Онлайн:** открой стартовый проект по адресу [rpf.io/cats-on](http://rpf.io/cats-on){:target="_blank"}.

Если у тебя есть учетная запись Scratch, то ты можешь сделать копию, нажав **Ремикс**.

**Оффлайн**: открой [стартовый проект](http://rpf.io/p/en/cats-go) в оффлайн-редакторе. Если тебе нужно скачать и установить оффлайн редактор Scratch, ты можешь найти его по адресу [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Добавь расширение Перо в свой проект.

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

Нажми на спрайт под названием «Перо» и добавьте код, чтобы установить цвет пера таким же синим, как и у объектов на сцене.

![Pen sprite](images/pen-sprite.png)

```blocks3
когда флажок установлен
установи цвет пера на [# 0000ff]
сотри все
установи размер пера на (5)
```

Чтобы выбрать цвет, нажми на цветовой квадрат в блоке `установить цвет для пера`{:class="block3extensions"}, чтобы курсор мыши превратился в пипетку, а затем щёлкни нужный цвет на Сцене.

\--- /task \---

\--- task \---

Добавь еще немного кода, чтобы спрайт следовал за указателем мыши. Протестируй свою программу, чтобы убедиться, что код работает.

![Pen sprite](images/pen-sprite.png)

```blocks3
forever
перейти на (указатель мыши v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Добавь код, чтобы cпрайт рисовал линию на Сцене, если кнопка мыши нажата.

![Pen sprite](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`Если`{:class="block3control"} `мышь нажата`{:class="block3sensing"}, то `опустить перо`{:class="block3extensions"}, `иначе`{:class="block3control"}, `поднять перо`{:class="block3extensions"}.

\--- /hint \---

\--- hint \---

Вот блоки кода, которые тебе нужны:

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

This is what your code should look like:

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

Test your code. You should be able to click and drag with the mouse to draw a blue line on the Stage.

![Draw a line](images/draw-a-line.png)

\--- /task \---

You probably see that a blue dot always appears in the top right-hand corner of the Stage (it's circled in the image above). This is because, when you click the green flag to start the game, you press the mouse down, and so the pen immediately starts drawing.

\--- task \---

To stop this from happening, add a `pen up`{:class="block3extensions"} block at the start of the script, and a `wait one second`{:class="block3control"} block above the `forever`{:class="block3control"} block.

![Pen sprite](images/pen-sprite.png)

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