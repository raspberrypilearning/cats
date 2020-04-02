## Cloner les chats

Tu veux un flot incessant de chats que le joueur doit guider le long du chemin vers la sortie.

\--- task \---

Clique sur le sprite appelé « Chat », et ajoute du code pour `cacher`{:class="block3looks"} le sprite, et aussi le `cloner`{:class="block3control"} toutes les trois secondes.

![Sprite Chat](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

Si tu exécutes le programme maintenant, rien ne se passe sur la scène. Pour vérifier qu'un nouveau clone de sprite Chat est créé toutes les trois secondes, fais en sorte que chaque clone apparaisse et tombe du ciel.

\--- task \---

Ajoute du code pour indiquer au sprite que `lorsqu'il commence comme un clone`{:class="block3control"}, il doit se `montrer`{:class="block3looks"} et tomber jusqu'à ce qu'il `touche`{:class="block3sensing"} le sol bleu dessiné sur la scène.

![Sprite Chat](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`quand je commence comme un clone`{:class="block3control"}, `montrer`{:class="block3looks"} le sprite. `de manière répétée`{:class="block3control"} `Ajouter`{:class="block3motion"} `-2` à la coordonnée `y` du sprite, jusqu'à ce que le sprite `touche`{:class="block3sensing"} la scène bleue.

\--- /hint \---

\--- hint \---

Voici les blocs dont tu as besoin :

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

Voici à quoi ton code devrait ressembler :

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

Lorsque tu cliques sur le drapeau vert, tu devrais voir un nouveau chat tomber du haut de la scène toutes les trois secondes. Chaque chat devrait atterrir dans un gros tas de chats qui se chevauchent sur le sol bleu en bas.

![Chats qui tombent](images/falling-cats.png)