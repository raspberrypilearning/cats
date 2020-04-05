## Pegarse a las líneas

Te habrás dado cuenta que, si dibujas un puente más bajo entre las dos plataformas, o una línea que se inclina hacia arriba, ¡los gatos terminan caminando a través de la plataforma en lugar de por encima!

![Gatos caminando por la plataforma](images/cat-walk-through-platform.png)

--- task ---

En el código para el objeto "Gato", añade otro bucle antes del bloque `siguiente disfraz`{:class="block3looks"}. Esta vez, el bucle debería indicarle al gato que se mueva hacia arriba por `2` hasta que no esté tocando el color azul.

![Objeto Gato](images/cat-sprite.png)

--- hints ---
 --- hint ---

El gato debería `moverse 2 hacia arriba`{:class="block3motion"} `repetir hasta que`{:class="block3control"} `no`{:class="block3operators"} `toque el color azul`{:class="block3sensing"}.

--- /hint ---

--- hint ---

Aquí están los bloques de código que necesitas:

```blocks3
<touching color [#0000ff]?>

change y by (-2)

repetir hasta que <>
end

no <>
```

--- /hint ---

--- hint ---

Así es como debería verse tu código:

```blocks3
al comenzar como clon
mostrar
repetir hasta que <touching (edge v)?> 
mover (10) pasos
repetir hasta que <touching color [#0000ff]?> 
change y by (-2)
end
repetir hasta que <not <touching color [#0000ff]?>> 
change y by (-2)
end
siguiente disfraz
esperar (0.1) segundos
end
eliminar este clon
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Haz clic en la bandera verde e intenta dibujar una línea que se incline hacia arriba. Comprueba que tu gato sigue esta línea.

--- /task ---