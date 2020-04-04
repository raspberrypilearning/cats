## Clona gatos

Tu quieres un flujo interminable de gatos que el jugador deba guiar a lo largo del camino hacia la salida.

--- task ---

Haz clic en el objeto llamado 'Gato' y agrega un código para `esconder`{:class="block3looks"} el objeto, y también para `clonar`{:class="block3control"} cada tres segundos.

![Objeto Gato](images/cat-sprite.png)

```blocks3
al presionar bandera verde
esconder
por siempre 
  crear clon de (mí mismo v)
  esperar (3) segundos
end
```

--- /task ---

Si ejecutas el programa ahora, no sucede nada en el Escenario. Para verificar que se crea un nuevo clon del objeto Gato cada tres segundos, haz que cada clon aparezca y caiga del cielo.

--- task ---

Añade código para decirle al objeto que `cuando se inicie como un clon`{:class="block3control"}, debe `mostrarse`{:class="block3looks"} a sí mismo y caer hasta que `toque`{:class="block3sensing"} el suelo azul que está dibujado en el Escenario.

![Objeto Gato](images/cat-sprite.png)

--- hints ---
 --- hint ---

`Cuando el objeto Gato comience como un clon`{:class="block3control"}, `muestra`{:class="block3looks"} el objeto. `Repetidamente`{:class="block3control"} `Cambia`{:class="block3motion"} la coordenada `y` del objeto a `-2`, hasta que el objeto `toque`{:class="block3sensing"} el Escenario azul.

--- /hint ---

--- hint ---

Aquí están los bloques de código que necesitas:

```blocks3
repetir hasta que <>
end

mostrar

<touching color [#0000ff]?>

change y by (-2)

al comenzar como clon
```

--- /hint ---

--- hint ---

Así es como debería verse tu código:

```blocks3
al comenzar como clon
mostrar
repetir hasta que <touching color [#0000ff]?> 
sumar a y (-2)
end
```

--- /hint ------ /hints ---

--- /task ---

Cuando hagas clic en la bandera verde, deberías ver un nuevo gato caer desde la parte superior del escenario cada tres segundos. Cada gato debe aterrizar en una gran pila de gatos superpuestos en el suelo azul de la parte inferior.

![Gatos que caen](images/falling-cats.png)