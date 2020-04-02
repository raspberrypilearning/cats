## Clona i gatti

Vuoi un flusso infinito di gatti che il giocatore deve guidare lungo il percorso verso l'uscita.

\--- task \---

Fai clic sullo sprite chiamato 'Gatto' e aggiungi del codice per `nascondere`{:class="block3looks"} lo sprite, e anche per `clonare`{:class="block3control"} lo sprite ogni tre secondi.

![Sprite gatto](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

Se esegui il programma ora, non accade nulla sullo Stage. Per verificare che ogni tre secondi venga creato un nuovo clone dello sprite del Gatto, fai apparire e cadere tutti i cloni dal cielo.

\--- task \---

Aggiungi del codice per dire allo sprite che `quando viene clonato`{:class="block3control"}, dovrebbe `mostrare`{:class="block3looks"} lo sprite e cadere finché non `tocca`{:class=block3sensing"} il pavimento blu disegnato sullo Stage.

![Sprite gatto](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Quando lo sprite inizia come clone`{:class="block3control"}, `mostra`{:class="block3looks"} lo sprite. `Ripetutamente`{:class="block3control"} `Cambia`{:class="block3motion"} la coordinata `y` dello sprite a `-2`, fino a quando lo sprite `tocca`{:class="block3sensing"} lo Stage di colore blu.

\--- /hint \---

\--- hint \---

Ecco i blocchi di codice che ti servono:

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

Ecco come dovrebbe apparire il tuo codice:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

Quando fai clic sulla bandiera verde, dovresti vedere un nuovo gatto cadere dalla parte alta dello Stage ogni tre secondi. Ogni gatto dovrebbe atterrare in un grande mucchio di gatti posti uno sopra l'altro sul pavimento blu nella parte inferiore.

![Gatti che cadono](images/falling-cats.png)