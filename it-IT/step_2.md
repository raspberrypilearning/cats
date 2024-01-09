## Traccia delle linee

\--- task \---

Apri il progetto Scratch per principianti "GATTI!".

**Online:** open the starter project at [rpf.io/cats-on](https://rpf.io/cats-on){:target="_blank"}.

Se hai un account Scratch puoi fare una copia facendo clic su **Remix**.

**Offline:** open the [starter project](https://rpf.io/p/en/cats-go) in the offline editor. If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Aggiungi l'estensione Penna al tuo progetto.

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

Fai clic sullo sprite chiamato "Penna" e aggiungi il codice per impostare il colore della penna sullo stesso blu degli ostacoli sulla stage.

![Sprite penna](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Per selezionare un colore, fai clic sul riquadro dei colori nel blocco `porta colore penna a`{:class="block3extensions"} per trasformare il cursore del mouse in una pipetta, quindi fai clic sul colore corretto sullo Stage.

\--- /task \---

\--- task \---

Aggiungi altro codice per fare in modo che lo sprite segua il puntatore del mouse. Prova il tuo programma per verificare che il codice funzioni.

![Sprite penna](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Aggiungi del codice per dire allo sprite di tracciare una linea sullo Stage se il pulsante del mouse è premuto.

![Sprite penna](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`Se`{:class="block3control"} il `mouse è premuto`{:class="block3sensing"}, `aziona la penna`{:class="block3extensions"} e `altrimenti`{:class="block3control"}, `solleva la penna`{:class="block3extensions"}.

\--- /hint \---

\--- hint \---

Ecco i blocchi di codice che ti servono:

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

\--- /hint \---

\--- hint \---

Ecco come dovrebbe apparire il tuo codice:

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
forever
go to (mouse pointer v)
+ if <mouse down?> then
pen down
else
pen up
end
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Prova il tuo codice. Dovresti essere in grado di fare clic e trascinare il mouse per disegnare una linea blu sullo Stage.

![Traccia una linea](images/draw-a-line.png)

\--- /task \---

Probabilmente vedrai che un punto blu appare sempre nell'angolo in alto a destra dello Stage (è cerchiato nell'immagine sopra). Questo perché, quando si fa clic sulla bandiera verde per iniziare il gioco, si preme il mouse e quindi la penna inizia immediatamente a disegnare.

\--- task \---

Per evitare che ciò accada, aggiungi un blocco `penna su`{:class="block3extensions"} all'inizio dello script e un blocco `attendi un secondo`{:class="block3control"} sopra il blocco `per sempre`{:class="block3control"}.

![Sprite penna](images/pen-sprite.png)

```blocks3
when flag clicked
+ pen up
set pen color to [#0000ff]
erase all
set pen size to (5)
+ wait (1) seconds
forever
go to (mouse pointer v)
if <mouse down?> then
pen down
else
pen up
end
```

\--- /task \---