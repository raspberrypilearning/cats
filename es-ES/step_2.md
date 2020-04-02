## Dibuja líneas

\--- task \---

Open the 'CATS!' Scratch starter project.

**Online:** open the starter project at [rpf.io/cats-on](http://rpf.io/cats-on){:target="_blank"}.

If you have a Scratch account you can make a copy by clicking **Remix**.

**Sin conexión**: abre el [proyecto de inicio](http://rpf.io/p/en/cats-go) en el editor sin conexión. Si necesitas descargar e instalar el editor sin conexión de Scratch, puedes encontrarlo en [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Añade la extensión Lápiz a tu proyecto.

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

Haz clic en el objeto llamado 'Lápiz' y agrega el código para establecer el color del lápiz en el mismo azul que los obstáculos en el Escenario.

![Pen sprite](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Para seleccionar un color, haz clic en el cuadrado de color en el bloque `fijar color de lápiz a`{: class = "block3extensions"} para hacer que el cursor del ratón se convierta en una pipeta, y luego haz clic en el color correcto en el Escenario.

\--- /task \---

\--- task \---

Agrega un poco más de código para que el objeto siga al puntero del ratón. Prueba tu programa para verificar que el código funcione.

![Pen sprite](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Agrega algo de código para indicarle al objeto que dibuje una línea en el escenario si se presiona el botón del ratón.

![Pen sprite](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`Si`{:class="block3control"} el `ratón está pulsado`{:class="block3sensing"}, pon el`lápiz abajo`{:class="block3extensions"}, y `sino`{:class="block3control"}, levanta el`lápiz hacia arriba`{:class="block3extensions"}.

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

Test your code. Deberías poder hacer clic y arrastrar con el ratón para dibujar una línea azul en el escenario.

![Draw a line](images/draw-a-line.png)

\--- /task \---

Probablemente veas que siempre aparece un punto azul en la esquina superior derecha del Escenario (está encerrado en un círculo en la imagen de arriba). Esto se debe a que, cuando haces clic en la bandera verde para iniciar el juego, presionas el ratón y el bolígrafo comienza a dibujar inmediatamente.

\--- task \---

Para evitar que esto suceda, agrega un bloque `subir lápiz`{: class = "block3extensions"} al comienzo del script, y un bloque `esperar (1) segundos`{: class = "block3control"} sobre el bloque `por siempre`{ : clase = "block3control"}.

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