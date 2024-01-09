## Dibuja líneas

\--- task \---

Abre el proyecto de inicio de Scratch '¡GATOS!'.

**Online:** open the starter project at [rpf.io/cats-on](https://rpf.io/cats-on){:target="_blank"}.

Si tienes una cuenta de Scratch, puedes hacer una copia haciendo clic en ** Remix **.

**Offline:** open the [starter project](https://rpf.io/p/en/cats-go) in the offline editor. If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Añade la extensión Lápiz a tu proyecto.

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

Haz clic en el objeto llamado 'Lápiz' y agrega el código para establecer el color del lápiz en el mismo azul que los obstáculos en el Escenario.

![Objeto lápiz](images/pen-sprite.png)

```blocks3
al presionar la bandera
fijar el color del lápiz a [#0000ff]
borrar todo
fijar tamaño del lápiz a (5)
```

Para seleccionar un color, haz clic en el cuadro de color del bloque `fijar color del lápiz`{:class="block3extensions"} para hacer que el cursor del ratón se convierta en una pipeta, y luego haz clic en el color correcto en el escenario.

\--- /task \---

\--- task \---

Añade un poco más de código para hacer que el objeto siga el puntero del ratón. Prueba tu programa para verificar que el código funcione.

![Objeto lápiz](images/pen-sprite.png)

```blocks3
por siempre 
ir a (puntero del ratón v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Agrega algo de código para indicarle al objeto que dibuje una línea en el escenario si se presiona el botón del ratón.

![Objeto lápiz](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`Si`{:class="block3control"} el `ratón está pulsado`{:class="block3sensing"}, pon el `lápiz abajo`{:class="block3extensions"}, y `si no`{:class="block3control"}, levanta el `lápiz`{:class="block3extensions"}.

\--- /hint \---

\--- hint \---

Aquí están los bloques de código que necesitas:

```blocks3
<mouse down?>

bajar lápiz

subir lápiz

si <> entonces
si no
end
```

\--- /hint \---

\--- hint \---

Así es como debería verse tu código:

```blocks3
al presionar bandera
fijar color de lápiz a [#0000ff]
borrar todo
fijar tamaño de lápiz a (5)
por siempre 
ir a (puntero del ratón v)
si <mouse down?> entonces 
bajar lápiz
si no 
subir lápiz
end
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Prueba tu código. Deberías poder hacer clic y arrastrar con el ratón para dibujar una línea azul en el escenario.

![Dibuja una línea](images/draw-a-line.png)

\--- /task \---

Probablemente veas que siempre aparece un punto azul en la esquina superior derecha del Escenario (está encerrado en un círculo en la imagen de arriba). Esto se debe a que, cuando haces clic en la bandera verde para iniciar el juego, presionas el ratón y el bolígrafo comienza a dibujar inmediatamente.

\--- task \---

Para evitar que esto suceda, agrega un bloque `subir lápiz`{:class = "block3extensions"} al comienzo del script, y un bloque `esperar un segundo`{: class = "block3control"} sobre el bloque `por siempre`{: clase = "block3control"}.

![Objeto lápiz](images/pen-sprite.png)

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