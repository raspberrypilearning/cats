## Mettons-nous à l'abri

Le but du jeu est de guider les chats en sécurité en créant un chemin pour qu'ils puissent atteindre la porte. Crée une variable score pour garder une trace du nombre de chats qui atteignent la porte.

\--- task \---

Crée une nouvelle variable appelée `score`{:class="block3variables"}.

![Sprite Chat](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Ajoute du code à ton sprite chat pour ajouter `1` au `score`{:class="block3variables"} à chaque fois qu'un chat atteint la porte. Mets également `score`{:class="block3variables"} à `0` `quand le drapeau est cliqué`{:class="block3events"} au début du jeu.

![Sprite Chat](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Si`{:class="block3control"} le chat `touche le sprite porte`{:class="block3sensing"}, alors `ajouter 1 au score`{:class="block3variables"}.

\--- /hint \---

\--- hint \---

Voici les nouveaux blocs de code que tu dois ajouter à ton script `quand je commence comme un clone` :

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
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

Ajoute plus de code pour que, lorsqu'un sprite chat atteint la porte, le chat fasse un son « miaou » et ensuite disparaisse.

![Sprite Chat](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

\--- /task \---