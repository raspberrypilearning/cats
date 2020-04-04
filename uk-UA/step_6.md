## Шлях до безпечного місця

Мета гри — скерувати котів у безпечне місце, створюючи шлях, щоб вони могли дістатися до дверей. Створи змінну для балів, щоб відстежувати, скільки котів доходить до дверей.

\--- task \---

Створи нову змінну з назвою `рахунок`{:class="block3variables"}.

![Спрайт "Кіт"](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Додай код до свого спрайта, щоб збільшувати на `1` `рахунок`{:class="block3variables"} кожного разу, коли кіт досягне дверей. Також встанови `рахунок`{:class="block3variables"} рівним `0` `коли прапорець натиснуто`{:class="block3events"} на початку гри.

![Спрайт "Кіт"](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Якщо`{:class="block3control"} кіт `торкається дверей`{:class="block3sensing"}, то ` змінити рахунок на 1`{:class="block3variables"}.

\--- /hint \---

\--- hint \---

Ось нові блоки коду, які потрібно додати до твого скрипта `коли я починаю як клон`:

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
```

\--- /hint \---

\--- hint \---

Ось як має виглядати твій код:

```blocks3
when I start as a clone
show
repeat until <touching (edge v)?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    repeat until <not <touching color [#0000ff]?>>
        change y by (2)
    end
    next costume
    wait (0.1) seconds
+   if <touching (Door v)?> then
        change [score v] by (1)
    end
end
delete this clone

when flag clicked

+ set [score v] to (0)
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Додай код для того, щоб спрайт відтворював звук "meow" ("няв") і зникав після того, коли дістанеться дверей.

![Спрайт "Кіт"](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

\--- /task \---