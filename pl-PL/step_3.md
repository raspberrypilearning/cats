## Klonowanie kotów

Chcesz niekończący się strumień kotów, które gracz musi prowadzić wzdłuż ścieżki do wyjścia.

\--- task \---

Kliknij duszka o nazwie „Duszek1” i dodaj kod `ukryj`{:class="block3looks"} do duszka, a także do `utwórz klona z siebie`{:class="block3control"} co trzy sekundy.

![Duszek1 - duszek kota](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

Jeśli teraz uruchamiasz program, nic się nie stanie na scenie. Aby sprawdzić, czy nowy klon Duszka1 jest tworzony co trzy sekundy, spraw, aby każdy klon pojawiał się i spadał z nieba.

\--- task \---

Dodaj kod, aby poinformować duszka, że `gdy zaczyna się jako klon`{:class="block3control"}, powinien się `pokazać`{:class="block3looks"} i spadać, aż będzie `dotykać`{:class=" block3sensing"} niebieską podłogę narysowaną na scenie.

![Duszek1 - duszek kota](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Kiedy duszek zaczyna jako klon`{:class="block3control"}, `pokazują`{:class="block3looks"} duszka. `Powtarzaj`{:class="block3control"} `Zmień`{:class="block3motion"} Współrzędną `y` duszka o `-2`, aż duszek będzie `dotykać`{:class="block3sensing"} niebieskiej sceny.

\--- /hint \---

\--- hint \---

Oto potrzebne bloki kodu:

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

Tak powinien wyglądać Twój kod:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

Kiedy klikniesz zieloną flagę, co trzy sekundy powinien wypaść nowy kot ze szczytu sceny. Każdy kot powinien wylądować na dużym stosie nachodzących na siebie kotów na niebieskiej podłodze u dołu.

![Spadające koty](images/falling-cats.png)