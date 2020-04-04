## Spraw, aby koty poruszały się

Gdy kot dotrze do podłogi, powinien powoli posuwać się w prawo.

\--- task \---

Dodaj następujący kod do sekcji `gdy zaczynam jako klon`{:class="block3control"} duszka kota aby `przesuń o 10 kroków`{:class="block3motion"}, i przełączaj dwoma kostiumami duszka co 0,1 sekundy żeby kot wyglądał, jakby szedł.

![Duszek kota](images/cat-sprite.png)

\--- hints \--- \--- hint \---

Duszek kota powinien się `przesunąć o10 kroków`{:class="block3motion"} i następnie zmienić kostium `następny kostium`{:class="block3looks"}co `0,1 sekundy`{:class="block3control"}. Ten kod powinien powtarzać się `zawsze`{:class="block3control"}, podobnie jak kod powodujący upadek kota.

\--- /hint \---

\--- hint \---

Oto potrzebne bloki kodu:

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

\--- /hint \---

\--- hint \---

Tak powinien wyglądać Twój kod:

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

Naciśnij zieloną flagę i sprawdź, czy koty poruszają się teraz wzdłuż niebieskiej platformy na dole.

\--- /task \---

Jeśli narysujesz most nad dziurą, aby koty mogły dotrzeć do końca prawej strony sceny, zobaczysz, że w końcu utknęły w prawej ścianie.

![Spadające koty na krawędzi](images/flailing-at-edge.png)

\--- task \---

Usuń pętlę `zawsze`{:class="block3control"} i zamiast niej dodaj inną pętlę, aby koty chodziły tylko do krawędzi. Kiedy kot dotrze do krawędzi sceny, powinien zniknąć.

![Duszek kota](images/cat-sprite.png)

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

Naciśnij zieloną flagę i sprawdź, czy koty znikają, gdy dotrą do krawędzi sceny.

\--- /task \---

Możesz zauważyć, że jeśli koty wpadną do dziury, nie znikną, ale utkną na dole. To dlatego, że wciąż próbują spadać w dół.

To jest część kodu, która mówi kotowi, aby spadał, dopóki nie dotknie niebieskiego:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

Jednak w dziurze kot nigdy nie osiągnie niebieskiego, więc utknie na zawsze.

\--- task \---

Dodaj więcej bloków do tej pętli, aby powtarzała się, aż duszek kota dotknie niebieskiego `lub`{:class="block3operators"} `dotknie krawędzi`{:class="block3sensing"}. W ten sposób duszek przestaje próbować spadać, jeśli dojdzie do krawędzi sceny.

![Duszek kota](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---