## Dibuixa línies

\--- task \---

Obre el projecte inicial "CATS!" d’Scratch.

**En línia:** obre el projecte inicial a [rpf.io/cats-on ](http://rpf.io/cats-on) {:target = "_ blank"}.

Si tens un compte a Scratch pots fer una còpia fent clic a **Reinventa**.

**Fora de línia:** obriu el [projecte inicial](http://rpf.io/p/en/cats-go) a l’editor fora de línia. Si necessites descarregar i instal·lar l'editor fora de línia d'Scratch, el pots trobar a [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Afegeix l’extensió Llapis al teu projecte.

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

Fes clic al personatge anomenat "Llapis", i afegeix codi per configurar el color del llapis al mateix blau que el dels obstacles de l'escenari.

![Personatge del llapis](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Per seleccionar un color, fes clic al quadrat de color del bloc `fixa el color del llapis a`{:class="block3extensions"} per fer que el cursor del ratolí es converteixi en una pipeta i, a continuació, fes clic al color correcte de l'escenari.

\--- /task \---

\--- task \---

Afegeix més codi per tal que el personatge segueixi el punter del ratolí. Prova el programa per comprovar que el codi funciona.

![Pen sprite](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Add some code to tell the sprite to draw a line on the Stage if the mouse button is pressed down.

![Pen sprite](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`If`{:class="block3control"} the `mouse is down`{:class="block3sensing"}, put the `pen down`{:class="block3extensions"}, and `else`{:class="block3control"}, lift the `pen up`{:class="block3extensions"}.

\--- /hint \---

\--- hint \---

Aquí tens els blocs que necessites:

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

Així és com s'hauria de veure el teu codi:

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

Prova el codi nou. You should be able to click and drag with the mouse to draw a blue line on the Stage.

![Dibuixa una línia](images/draw-a-line.png)

\--- /task \---

You probably see that a blue dot always appears in the top right-hand corner of the Stage (it's circled in the image above). This is because, when you click the green flag to start the game, you press the mouse down, and so the pen immediately starts drawing.

\--- task \---

To stop this from happening, add a `pen up`{:class="block3extensions"} block at the start of the script, and a `wait one second`{:class="block3control"} block above the `forever`{:class="block3control"} block.

![Pen sprite](images/pen-sprite.png)

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