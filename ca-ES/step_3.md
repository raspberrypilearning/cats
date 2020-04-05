## Clona gats

Volem un flux de gats que el jugador ha de guiar pel camí fins a la sortida.

\--- task \---

Fes clic al personatge anomenat 'Gat' i afegeix algun codi per `amagar`{:class="block3looks"} i per `clonar`{:class="block3control"} el personatge cada tres segons.

![Personatge del gat](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

Si executes el programa ara, no passa res a l’Escenari. Per comprovar que es crea un nou clon del personatge Gat cada tres segons, fes que cada clon aparegui i caigui del cel.

\--- task \---

Afegeix codi per dir-li al personatge que `quan s'inicia com a cloni`{:class = "block3control"} s'hauria de `mostrar`{:class="block3looks"} i caure fins que `toqui`{:class=" block3sensing"} el terra blau que està dibuixat a l'Escenari.

![Personatge del gat](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Quan el personatge comença com un clon`{:class="block3control"}, `mostra`{:class="block3looks"} el personatge. `Repetidament`{ class="block3control"} `Canviar`{:class="block3motion"} la coordenada `y` del personatge per `-2`, fins que el personatge `toqui`{:class="block3sensing"} el color blau de l'Escenari.

\--- /hint \---

\--- hint \---

Aquí tens els blocs que necessites:

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

Així és com s'hauria de veure el teu codi:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

Quan facis clic a la bandera verda, hauries de veure caure un gat nou des de la part superior de l'Escenari cada tres segons. Cada gat ha d’aterrar en una gran pila de gats amuntegats al terra blau de la part inferior.

![Gats que cauen](images/falling-cats.png)