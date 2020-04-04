## Respecter les lignes

Tu pourras remarquer que, si tu traces un pont plus bas entre les deux plateformes, ou une ligne qui est inclinée vers le haut, les chats finissent par se promener à travers la plate-forme plutôt que par dessus !

![Chats qui traversent la plate-forme](images/cat-walk-through-platform.png)

\--- task \---

Dans le code du sprite chat, ajoute une autre boucle avant le bloc `costume suivant`{:class="block3looks"}. Cette fois, la boucle devrait dire au chat de se déplacer vers le haut par `2` jusqu'à ce qu'il ne touche pas le bleu.

![Sprite Chat](images/cat-sprite.png)

\--- hints \--- \--- hint \---

Le chat devrait `monter de 2`{:class="block3motion"} `de manière répétée jusqu'à ce qu'il`{:class="block3control"} `ne`` touche pas le bleu` {:class="block3operators"}{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Voici les blocs dont tu as besoin :

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

Voici à quoi ton code devrait ressembler :

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
end
delete this clone
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Clique sur le drapeau vert et essaie de dessiner une ligne qui est inclinée vers le haut. Vérifie que ton chat suit cette ligne.

\--- /task \---