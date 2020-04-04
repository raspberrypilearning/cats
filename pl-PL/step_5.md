## Trzymaj się linii

Możesz zauważyć, że jeśli narysujesz nisko zawieszony most między dwiema platformami lub stromą linię w górę, koty ostatecznie przechodzą przez platformę, zamiast po niej!

![Koty przechodzą przez platformę](images/cat-walk-through-platform.png)

\--- task \---

W kodzie duszka kota dodaj kolejną pętlę przed blokiem `następny kostium`{:class="block3looks"}. Tym razem pętla powinna poinformować kota o przesunięciu się w górę o `2` dopóki nie dotknie niebieskiego.

![Duszek kota](images/cat-sprite.png)

\--- hints \--- \--- hint \---

Kot powinien `przesuwać się w górę o 2`{:class="block3motion"} i `powtarzać aż`{:class="block3control"} `nie`{:class="block3operators"} `dotyka niebieskiego`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Oto potrzebne bloki kodu:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

Tak powinien wyglądać Twój kod:

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

Kliknij zieloną flagę i spróbuj rysować linię nachylenia w górę. Sprawdź, czy twój kot podąża za tą linią.

\--- /task \---