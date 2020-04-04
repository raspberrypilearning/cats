## Haz que los gatos se muevan

Una vez que un gato llega al suelo, debe avanzar lentamente hacia la derecha.

\--- task \---

Agrega código a la sección `al comenzar como clon`{:class="block3control"} para hacer que el objeto Gato se `mueva diez pasos`{:class="block3motion"}, y cambie entre los dos disfraces del objeto cada 0.1 segundos para que parezca que el gato que está caminando.

![Objeto Gato](images/cat-sprite.png)

\--- hints \--- \--- hint \---

El objeto Gato debe `moverse 10 pasos`{:class="block3motion"}, y `cambiar el disfraz `{:class="block3looks"} cada `0.1 segundos`{:class="block3control"}. Este código debe repetirse `por siempre`{:class="block3control"}, al igual que el código que hace que el gato caiga.

\--- /hint \---

\--- hint \---

Aquí están los bloques de código que necesitas:

```blocks3
mover (10) pasos

esperar (0.1) segundos

siguiente disfraz

por siempre
end
```

\--- /hint \---

\--- hint \---

Así es como debería verse tu código:

```blocks3
al comenzar como clon
mostrar
+ por siempre 
mover (10) pasos
repetir hasta que <touching color [#0000ff]?> 
cambiar y a (-2)
end
siguiente disfraz
esperar (0.1) segundos
end
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Presiona la bandera verde y verifica que los gatos ahora se muevan a lo largo de la plataforma azul en la parte inferior.

\--- /task \---

Si dibujas un puente a través del hueco para que los gatos puedan llegar hasta el lado derecho del Escenario, puedes ver que terminan clavados caminando a través de la pared derecha.

![Gatos agitándose en el borde](images/flailing-at-edge.png)

\--- task \---

Elimina el bucle `por siempre`{:class="block3control"} y, en su lugar, añade un bucle diferente para que los gatos sólo caminen hasta que lleguen al borde. Cuando un gato llega al borde del Escenario, debe desaparecer.

![Objeto Gato](images/cat-sprite.png)

```blocks3
al comenzar como clon
mostrar
+ repetir hasta que <touching (edge v)?> 
mover (10) pasos
repetir hasta que <touching color [#0000ff]?> 
cambiar y a (-2)
end
siguiente disfraz
esperar (0.1) segundos
end
+ eliminar este clon
```

\--- /task \---

\--- task \---

Presiona la bandera verde y verifica que los gatos desaparezcan cuando lleguen al borde del escenario.

\--- /task \---

Date cuenta de que, si los gatos caen en el agujero, no desaparecen, sino que se quedan clavados en la parte inferior. Esto se debe a que siguen tratando de caerse.

Esta es la parte del código que le dice al gato que siga cayendo hasta que toque el color azul:

```blocks3
repetir hasta que <touching color [#0000ff]?>
end
```

Sin embargo, en el agujero, el gato nunca puede alcanzar el azul, por lo que está atrapado para siempre.

\--- task \---

Agrega más bloques a este bucle para que se repita hasta que el objeto Gato toque el color azul `o`{:class="block3operators"} `toque el borde`{:class="block3sensing"}. De esta manera, el objeto deja de intentar caerse si llega al borde del Escenario.

![Objeto Gato](images/cat-sprite.png)

```blocks3
repetir hasta que <<touching color [#0000ff]?> o <touching (edge v)?>>
end
```

\--- /task \---