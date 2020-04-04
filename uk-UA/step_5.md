## Переміщення по поверхні

Ти можеш помітити, що якщо намалювати низький міст між двома платформами або висхідну лінію, то коти будуть йти крізь платформу, а не по ній!

![Коти, які проходять крізь платформу](images/cat-walk-through-platform.png)

\--- task \---

У код для спрайта кота, додай ще один цикл перед блоком `наступний образ`{:class="block3looks"}. На цей раз, цикл повинен сказати котові рухатися вгору на `2` доки він не торкнеться синього.

![Спрайт "Кіт"](images/cat-sprite.png)

\--- hints \--- \--- hint \---

Кіт повинен `повторити`{:class="block3control"} `зміну у на 2`{:class="block3motion"} поки `не`{:class="block3operators"} `торкнеться синього кольору`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Тобі будуть потрібні наступні блоки коду:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
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
end
delete this clone
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Натисни на зелений прапорець і спробуй намалювати висхідну лінію. Перевір чи твій кіт іде по цій лінії.

\--- /task \---