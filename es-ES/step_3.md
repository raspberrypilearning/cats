## Clona gatos

Tu quieres un flujo interminable de gatos que el jugador deba guiar a lo largo del camino hacia la salida.

\--- task \---

Click on the sprite called 'Cat', and add some code to `hide`{:class="block3looks"} the sprite, and also to `clone`{:class="block3control"} it every three seconds.

![Objeto Gato](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

Si ejecutas el programa ahora, no sucede nada en el Escenario. Para verificar que se crea un nuevo clon del objeto Gato cada tres segundos, haz que cada clon aparezca y caiga del cielo.

\--- task \---

Añade código para decirle al objeto que `cuando se inicie como un clon`{:class = "block3control"}, debe `mostrarse`{:class ="block3looks"} a sí mismo y caer hasta que `toque`{:class =" block3sensing "} el suelo azul que está dibujado en el Escenario.

![Objeto Gato](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Cuando el objeto Gato comience como un clon`{:class="block3control"}, `muestra`{:class="block3looks"} el objeto. `Repetidamente`{:class="block3control"} `Cambia`{:class="block3motion"} la coordenada `y` del objeto a `-2`, hasta que el objeto `toque`{:class="block3sensing"} el Escenario azul.

\--- /hint \---

\--- hint \---

Aquí están los bloques de código que necesitas:

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

Así es como debería verse tu código:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

When you click the green flag, you should see a new cat fall from the top of the Stage every three seconds. Every cat should land in a big pile of overlapping cats on the blue floor at the bottom.

![Falling cats](images/falling-cats.png)