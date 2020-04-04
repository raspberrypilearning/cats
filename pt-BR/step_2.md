## Desenhar linhas

\--- task \---

Abra o projeto inicial Scratch 'GATOS!'.

**Online:** Abra o projeto inicial em [ rpf.io/cats-on ](http://rpf.io/cats-on){: target="_ blank"}.

Se você tiver uma conta Scratch, você pode fazer uma cópia clicando em **Remix**.

**Offline:** Abra o [projeto inicial](http://rpf.io/p/en/cats-go) no editor offline. Se você precisar baixar e instalar o editor offline do Scratch, você pode encontrá-lo em [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Adicione a extensão Caneta ao seu projeto.

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

Clique no ator chamado 'Caneta' e adicione um código para definir a cor da caneta para o mesmo azul dos obstáculos no palco.

![Pen sprite](images/pen-sprite.png)

```blocks3
quando bandeira verde for clicado
mude a cor da caneta para [#0000ff]
apague tudo
adicione (5) ao tamanho da caneta
```

To select a colour, click on the colour square in the `set pen color`{:class="block3extensions"} block to make your mouse cursor turn into a pipette, and then click on the correct colour on the Stage.

\--- /task \---

\--- task \---

Add some more code to make the sprite follow the mouse pointer. Test your program to check that the code works.

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

Here are the code blocks you need:

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

This is what your code should look like:

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

Test your code. You should be able to click and drag with the mouse to draw a blue line on the Stage.

![Draw a line](images/draw-a-line.png)

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