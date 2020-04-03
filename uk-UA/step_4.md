## Коти, що рухаються

Як тільки кіт досягає підлоги, він повинен повільно крокувати праворуч.

\--- task \---

Додай код до секції `коли я починаю як клон`{:class="block3control"}, щоб змусити спрайт кота `переміщатися на 10 кроків`{:class="block3motion"} і перемикатися між двома своїми образами кожні 0.1 секунди, щоб кіт виглядав так, ніби він йде.

![Cat sprite](images/cat-sprite.png)

\--- hints \--- \--- hint \---

Спрайт кота має `преміщатися на 10 кроків`{:class="block3motion"}, і показувати `наступний образ`{:class="block3looks"} кожні `0.1 секунди`{:class="block3control"}. Цей код має повторюватись `завжди`{:class="block3control"}, так як і код, який змушує кота падати.

\--- /hint \---

\--- hint \---

Ось необхідні тобі блоки коду:

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

\--- /hint \---

\--- hint \---

Ось як має виглядати твій код:

```blocks3
when I start as a clone
show
+ forever
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Натисни зелений прапорець і перевір, чи коти тепер переміщаються по синій платформі внизу.

\--- /task \---

Якщо намалювати міст через прірву, щоб коти могли дістатися до правої сторони сцени, ти можеш бачити, що вони в кінцевому підсумку застрягли біля правого краю сцени.

![Коти на краю](images/flailing-at-edge.png)

\--- task \---

Remove the `forever`{:class="block3control"} loop, and instead add a different loop to make the cats only walk until they reach an edge. Коли кіт досягає краю сцени, він повинен зникнути.

![Cat sprite](images/cat-sprite.png)

```blocks3
when I start as a clone
show
+ repeat until <touching (edge v)?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
+ delete this clone
```

\--- /task \---

\--- task \---

Press the green flag and check that the cats disappear when they reach the edge of the Stage.

\--- /task \---

You may notice that, if the cats fall into the hole, they don't disappear but instead get stuck at the bottom. This is because they keep trying to fall downwards.

Це частина коду, яка каже котові продовжувати падати доки не торкнеться синього кольору:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

Однак у прірві кіт не може досягти блакитного кольору, тому застрягає там назавжди.

\--- task \---

Add more blocks to this loop so that it repeats until the cat sprite is touching blue `or`{:class="block3operators"} `touching the edge`{:class="block3sensing"}. This way, the sprite stops trying to fall if it reaches the edge of the Stage.

![Cat sprite](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---