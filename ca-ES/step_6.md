## Fes que vagin segurs

L’objectiu del joc és guiar els gats de manera segura creant un camí perquè puguin arribar fins a la porta. Crea una variable de puntuació per fer un seguiment de quants gats arriben fins la porta.

\--- task \---

Crea una variable anomenada `puntuació`{:class="block3variables"}.

![Personatge del gat](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Afegeix codi al teu personatge de gat per afegir `1` a la `puntuació`{:class="block3variables"} cada vegada que un gat arribi a la porta. També assigna a `puntuació`{:class="block3variables"} el valor `0` `quan es faci clic a la bandera`{:class="block3events"} al començament del joc.

![Personatge del gat](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Si`{:class="block3control"} el gat està `tocant a la porta`{:class="block3sensing"}, aleshores `afegir 1 a la puntuació`{:class="block3variables"}.

\--- /hint \---

\--- hint \---

Aquests són els nou blocs de codi que necessites afegir al que ja tens `quan començo com a clon`:

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
```

\--- /hint \---

\--- hint \---

Així és com s'hauria de veure el teu codi:

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

Afegeix més codi per tal que, quan un personatge de gat arriba a la porta, aquest faci el so 'mèu' i després desaparegui.

![Personatge del gat](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

\--- /task \---