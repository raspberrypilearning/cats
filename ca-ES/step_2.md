## Dibuixa línies

\--- task \---

Obre el projecte inicial "CATS!" d’Scratch.

**Online:** open the starter project at [rpf.io/cats-on](https://rpf.io/cats-on){:target="_blank"}.

Si tens un compte a Scratch pots fer una còpia fent clic a **Reinventa**.

**Offline:** open the [starter project](https://rpf.io/p/en/cats-go) in the offline editor. If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

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

![Personatge del llapis](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Afegeix codi per dir-li al personatge que dibuixi una línia a l’Escenari si es manté premut el botó del ratolí.

![Personatge del llapis](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`Si`{:class="block3control"} el `ratolí clicat`{:class="block3sensing"}, `baixa el llapis`{:class="block3extensions"} i `si no`{:class="block3control"}, `puja el llapis`{:class="block3extensions "}.

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

Prova el codi nou. Hauries de fer clic i arrossegar amb el ratolí per dibuixar una línia blava a l'Escenari.

![Dibuixa una línia](images/draw-a-line.png)

\--- /task \---

Probablement veuràs que sempre apareix un punt blau a la part superior dreta de l'Escenari (està encerclat a la imatge de dalt). Això es deu al fet que, quan fas clic a la bandera verda per iniciar el joc, prems el ratolí cap avall i així el llapis comença a dibuixar immediatament.

\--- task \---

Per evitar que això passi, afegeix un bloc `puja el llapis`:{:class="block3extensions"} al començament del codi i un bloc `espera un segon`{:class="block3control"} per sobre del bloc `per sempre`{:class="block3control"}.

![Personatge del llapis](images/pen-sprite.png)

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