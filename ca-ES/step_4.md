## Fes moure els gats

Una vegada que un gat arriba al terra, hauria de passar lentament cap a la dreta.

\--- task \---

Afegeix codi a la secció `quan començo com a clon`{:class="block3control"} per fer que el gat es `mogui deu passos`{:class="block3motion"} i canvia entre els dos vestits del personatge cada 0,1 segons fer que el gat sembli que camini.

![Personatge del gat](images/cat-sprite.png)

\--- hints \--- \--- hint \---

El personatge del gat s'hauria de `moure 10 passos`{:class="block3motion"} i `canviar de vestit`{:class="block3looks"} cada `0,1 segons`{:class="block3control"}. Aquest codi s'hauria de repetir `per sempre`{:class="block3control"}, de la mateixa manera que el codi per fer caure el gat.

\--- /hint \---

\--- hint \---

Aquí tens els blocs que necessites:

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

\--- /hint \---

\--- hint \---

Així és com s'hauria de veure el teu codi:

```blocks3
when I start as a clone
show
+ forever
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Press the green flag and check that the cats now move along the blue platform at the bottom.

\--- /task \---

Si dibuixes un pont que tapi la bretxa perquè els gats puguin anar fins al costat dret de l’Escenari, pots veure que s’acaben enganxant caminant per la paret dreta.

![Flailing cats at the edge](images/flailing-at-edge.png)

\--- task \---

Remove the `forever`{:class="block3control"} loop, and instead add a different loop to make the cats only walk until they reach an edge. When a cat reaches the edge of the Stage, it should disappear.

![Cat sprite](images/cat-sprite.png)

```blocks3
when I start as a clone
show
+ repeat until <touching (edge v)?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
+ delete this clone
```

\--- /task \---

\--- task \---

Press the green flag and check that the cats disappear when they reach the edge of the Stage.

\--- /task \---

You may notice that, if the cats fall into the hole, they don't disappear but instead get stuck at the bottom. Això és perquè continuen intentant caure cap avall.

This is the part of the code that tells the cat to keep falling until it touches blue:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

Tot i això, al forat, el gat no pot arribar mai al blau, de manera que queda enganxat per sempre.

\--- task \---

Add more blocks to this loop so that it repeats until the cat sprite is touching blue `or`{:class="block3operators"} `touching the edge`{:class="block3sensing"}. This way, the sprite stops trying to fall if it reaches the edge of the Stage.

![Cat sprite](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---