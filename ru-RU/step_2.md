## Нарисуй линии

--- task ---

Открой стартовый проект «КОТЫ».

**Онлайн:** открой стартовый проект по адресу [scratch.mit.edu/projects/382684919](https://scratch.mit.edu/projects/382684919){:target="_blank"}.

Если у тебя есть учетная запись Scratch, то ты можешь сделать копию, нажав **Ремикс**.

**Оффлайн**: открой [стартовый проект](https://rpf.io/p/ru-RU/cats-go) в оффлайн-редакторе. Если тебе нужно скачать и установить оффлайн редактор Scratch, ты можешь найти его по адресу [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

Добавь расширение Перо в свой проект.

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

Нажми на спрайт под названием «Перо» и добавьте код, чтобы установить цвет пера таким же синим, как и у объектов на сцене.

![Спрайт пера](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Чтобы выбрать цвет, нажми на цветовой квадрат в блоке `установить цвет для пера`{:class="block3extensions"}, чтобы курсор мыши превратился в пипетку, а затем щёлкни нужный цвет на Сцене.

--- /task ---

--- task ---

Добавь еще немного кода, чтобы спрайт следовал за указателем мыши. Протестируй свою программу, чтобы убедиться, что код работает.

![Спрайт пера](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

Добавь код, чтобы cпрайт рисовал линию на Сцене, если кнопка мыши нажата.

![Спрайт пера](images/pen-sprite.png)

--- hints ---
 --- hint ---

`Если`{:class="block3control"} `мышь нажата`{:class="block3sensing"}, то `опустить перо`{:class="block3extensions"}, `иначе`{:class="block3control"}, `поднять перо`{:class="block3extensions"}.

--- /hint ---

--- hint ---

Вот блоки кода, которые тебе нужны:

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

--- /hint ---

--- hint ---

Вот как должен выглядеть твой код:

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

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Проверь свою программу. Ты должен иметь возможность нажать и перемещать мышку, чтобы нарисовать синюю линию на Сцене.

![Рисовать линию](images/draw-a-line.png)

--- /task ---

Ты, вероятно, видишь, что в правом верхнем углу Сцены всегда появляется синяя точка (обведено на рисунке выше). Это потому, что, когда ты нажимаешь на зелёный флажок, чтобы начать игру, ты нажимаешь кнопку мыши, и поэтому перо сразу начинает рисовать.

--- task ---

Чтобы это перестало происходить, добавь блок `поднять перо`{:class="block3extensions"} в начало своего кода и блок `ждать 1 секунд`{:class="block3control"} перед блоком `всегда`{:class="block3control"}.

![Спрайт пера](images/pen-sprite.png)

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

--- /task ---
