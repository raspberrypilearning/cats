## Клонируй котов

То, что ты хочешь, это бесконечный поток котов, которых игрок должен вести к выходу.

\--- task \---

Нажми на спрайт с именем «Кот‎» и добавь код `cпрятаться`{:class="block3looks"} в спрайт, а также `клонировать`{:class="block3control"} каждые три секунды.

![Спрайт кота](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

Если ты запустишь программу сейчас, на сцене ничего не произойдет. Чтобы проверить, что новый клон спрайта Кот создается каждые три секунды, сделай так, чтобы каждый клон появлялся и падал с неба.

\--- task \---

Добавь это код, чтобы сказать спрайту `когда я начинаю как клон`{:class="block3control"}, он должен `показаться`{:class="block3looks"} и падать пока не `касается`{:class="block3sensing"} синего пола, нарисованного на Сцене.

![Спрайт кота](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`когда я начинаю как клон`{:class="block3control"}, `покажи`{:class="block3looks"} спрайт. `Повторно`{:class="block3control"} `изменять`{:class="block3motion"} координату `y` спрайта на `-2`, пока спрайт не `коснется`{:class="block3sensing"} синей Сцены.

\--- /hint \---

\--- hint \---

Вот блоки кода, которые тебе нужны:

```blocks3
repeat until <>
end

show

<touching color [#0000ff]?>

change y by (-2)

when I start as a clone
```

\--- /hint \---

\--- hint \---

Вот как должен выглядеть твой код:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

When you click the green flag, you should see a new cat fall from the top of the Stage every three seconds. Every cat should land in a big pile of overlapping cats on the blue floor at the bottom.

![Falling cats](images/falling-cats.png)