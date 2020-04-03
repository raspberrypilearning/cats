## Llegar a un lugar seguro

El objetivo del juego es guiar a los gatos a un lugar seguro creando un camino para que puedan llegar a la puerta. Crea una variable de puntuación para registrar cuántos gatos llegan a la puerta.

\--- task \---

Crea una nueva variable llamada `puntuación`{:class="block3variables"}.

![Objeto Gato](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Añade código a tu objeto Gato para añadir `1` a la `puntuación`{:class="block3variables"} cada vez que un gato llegue a la puerta. También establece `puntuación`{:class="block3variables"} a `0`` cuando se haga click en la bandera`{:class="block3events"} al inicio de la partida.

![Objeto Gato](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Si`{:class="block3control"} el gato está `tocando el objeto Puerta`{:class="block3sensing"}, entonces `suma 1 a la puntuación`{:class="block3variables"}.

\--- /hint \---

\--- hint \---

Aquí están los nuevos bloques de código que necesitas agregar a tu programa de `al comenzar como clon`:

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
```

\--- /hint \---

\--- hint \---

Así es como debería verse tu código:

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

Añade un poco más de código para que, cuando el objeto Gato llegue a la puerta, haga un sonido 'meow', es decir, maulle, y luego desaparezca.

![Objeto Gato](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

\--- /task \---