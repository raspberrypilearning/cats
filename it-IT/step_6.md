## Mettiti in salvo

Lo scopo del gioco è quello di portare i gatti al sicuro creando un percorso in modo che possano raggiungere la porta. Crea una variabile di punteggio per tenere traccia della quantità di gatti che raggiungono la porta.

\--- task \---

Crea una variabile denominata `punteggio`{:class="block3variables"}.

![Sprite gatto](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Aggiungi il codice al tuo sprite del gatto per aggiungere `1` al `punteggio`{:class="block3variables"} ogni volta che un gatto raggiunge la porta. Inoltre imposta il `punteggio`{:class="block3variables"} a `0``quando si clicca sulla bandiera`{:class="block3events"} all'inizio del gioco.

![Sprite gatto](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Se`{:class="block3control"} il gatto `tocca lo sprite della porta`{:class="block3sensing"}, `aggiungi 1 al punteggio`{:class="block3variables"}.

\--- /hint \---

\--- hint \---

Ecco i nuovi blocchi di codice che devi aggiungere al tuo script `quando vengo clonato`:

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
```

\--- /hint \---

\--- hint \---

Ecco come dovrebbe apparire il tuo codice:

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

Aggiungi altro codice affinché, quando uno sprite del gatto raggiunge la porta, il gatto fa il verso "miao" e poi scompare.

![Sprite gatto](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

\--- /task \---