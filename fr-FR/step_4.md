## Faire bouger les chats

Une fois qu'un chat atteint le sol, il devrait avancer lentement vers la droite.

--- task ---

Ajoute du code à la section `quand je commence comme un clone`{:class="block3control"} pour que le sprite chat se `déplace de dix pas`{:class="block3motion"}, et bascule entre les deux costumes du sprite toutes les 0,1 secondes pour que le chat ait l'air de marcher.

![Sprite Chat](images/cat-sprite.png)

--- hints --- --- hint ---

Le sprite chat doit se `déplacer de 10 pas`{:class="block3motion"}, et `changer de costume`{:class="block3looks"} toutes les `0,1 secondes`{:class="block3control"}. Ce code devrait répéter le bloc `répéter indéfiniment`{:class="block3control"}, tout comme le code pour faire tomber le chat.

--- /hint ---

--- hint ---

Voici les blocs dont tu as besoin :

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

--- /hint ---

--- hint ---

Voici à quoi ton code devrait ressembler :

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

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Appuies sur le drapeau vert et vérifie que les chats se déplacent maintenant le long de la plate-forme bleue en bas.

--- /task ---

Si tu traces un pont à travers le vide pour que les chats puissent se rendre jusqu'au côté droit de la scène, tu peux voir qu'ils finissent par se coincer en marchant dans le mur de droite.

![Chats agités au bord](images/flailing-at-edge.png)

--- task ---

Supprime la boucle `répéter indéfiniment`{:class="block3control"} et ajoute une boucle différente pour que les chats ne marchent que jusqu'à ce qu'ils atteignent un bord. Lorsqu'un chat atteint le bord de la scène, il devrait disparaître.

![Sprite Chat](images/cat-sprite.png)

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

--- /task ---

--- task ---

Appuies sur le drapeau vert et vérifie que les chats disparaissent lorsqu'ils atteignent le bord de la scène.

--- /task ---

Tu remarques peut-être que si les chats tombent dans le trou, ils ne disparaissent pas mais restent coincés au fond. C'est parce qu'ils continuent d'essayer de tomber vers le bas.

C'est la partie du code qui dit au chat de continuer à tomber jusqu'à ce qu'il touche le bleu :

```blocks3
repeat until <touching color [#0000ff]?>
end
```

Cependant, dans le trou, le chat ne peut jamais atteindre le bleu, il est donc coincé pour toujours.

--- task ---

Ajoute plus de blocs à cette boucle afin qu'elle se répète jusqu'à ce que le sprite Chat touche le bleu `ou`{:class="block3operators"} `touche le bord`{:class="block3sensing"}. De cette façon, le sprite cesse d'essayer de tomber s'il atteint le bord de la scène.

![Sprite Chat](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

--- /task ---