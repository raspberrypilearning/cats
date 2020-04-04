## Dostań się w bezpieczne miejsce

Celem gry jest poprowadzenie kotów w bezpieczne miejsce, tworząc ścieżkę umożliwiającą im dotarcie do drzwi. Utwórz zmienną wyniku, aby śledzić ile kotów dociera do drzwi.

\--- task \---

Utwórz nową zmienną o nazwie `wynik`{:class="block3variables"}.

![Duszek kota](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Dodaj kod do duszka kota, aby dodać `1` do `wyniku`{:class="block3variables"} za każdym razem, gdy kot dociera do drzwi. Ustawia również `wynik`{:class="block3variables"} na `0` `po kliknięciu flagi`{:class="block3events"} na początku gry.

![Duszek kota](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`If`{:class="block3control"} kot ma `dotykając duszka drzwi`{:class="block3sensing"}, to `zmień wynik o 1`{:class="block3variables"}.

\--- /hint \---

\--- hint \---

Oto nowe bloki kodu, które musisz dodać do swojego skryptu `kiedy zaczynam jako klon`:

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
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

Dodaj jeszcze kilka bloków kody, aby duszek kota dotrze do drzwi, zamiauczał- wydał dźwięk "meow" i następnie znikł.

![Duszek kota](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

\--- /task \---