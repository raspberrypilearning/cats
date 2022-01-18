## Tracer des lignes

--- task ---

Ouvre le projet de démarrage Scratch « CHATS ! ».

**En ligne :** ouvre le projet de démarrage à [scratch.mit.edu/projects/382091816](https://scratch.mit.edu/projects/382091816){:target="_ blank"}.

Si tu as un compte Scratch, tu peux en créer une copie en cliquant sur **Remix**.

**Hors-ligne :** ouvre le [projet de démarrage](https://rpf.io/p/fr-FR/cats-go) dans l'éditeur hors-ligne. Si tu dois télécharger et installer l'éditeur hors-ligne Scratch, tu peux le trouver à [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

Ajoute l'extension Stylo à ton projet.

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

Clique sur le sprite appelé « Crayon » et ajoute du code pour définir la couleur du crayon sur le même bleu que les obstacles sur la scène.

![Sprite Crayon](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Pour sélectionner une couleur, clique sur le carré de couleur dans le bloc `mettre la couleur du stylo à`{:class="block3extensions"} pour que le curseur de ta souris se transforme en pipette, puis clique sur la bonne couleur sur la scène.

--- /task ---

--- task ---

Ajoute un peu plus de code pour que le sprite suive le pointeur de la souris. Teste ton programme pour vérifier que le code fonctionne.

![Sprite Crayon](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

Ajoute du code pour dire au sprite de tracer une ligne sur la scène si le bouton de la souris est enfoncé.

![Sprite Crayon](images/pen-sprite.png)

--- hints --- --- hint ---

`si`{:class="block3control"} `souris pressée ?`{:class="block3sensing"}, `stylo en position d'écriture`{:class="block3extensions"}, et `sinon`{:class=" block3control"}, `relever le stylo`{:class="block3extensions"}.

--- /hint ---

--- hint ---

Voici les blocs dont tu as besoin :

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

--- /hint ---

--- hint ---

Voici à quoi ton code devrait ressembler :

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
forever
go to (mouse pointer v)
+ if <mouse down?> then
pen down
else
pen up
end
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Teste ton code. Tu devrais pouvoir cliquer et faire glisser la souris pour tracer une ligne bleue sur la scène.

![Tracer une ligne](images/draw-a-line.png)

--- /task ---

Tu vois probablement qu'un point bleu apparaît toujours dans le coin supérieur droit de la scène (il est entouré dans l'image ci-dessus). C'est parce que lorsque tu cliques sur le drapeau vert pour démarrer le jeu, tu appuies sur la souris, et donc le stylo commence immédiatement à dessiner.

--- task ---

Pour éviter que cela ne se produise, ajoute un bloc `relever le stylo`{:class="block3extensions"} au début du script et un bloc `attendre une seconde`{:class="block3control"} au-dessus du bloc `répéter indéfiniment`{:class="block3control"}.

![Sprite Crayon](images/pen-sprite.png)

```blocks3
when flag clicked
+ pen up
set pen color to [#0000ff]
erase all
set pen size to (5)
+ wait (1) seconds
forever
go to (mouse pointer v)
if <mouse down?> then
pen down
else
pen up
end
```

--- /task ---
