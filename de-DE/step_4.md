## Lass die Katzen sich bewegen

Sobald eine Katze den Boden erreicht, sollte sie langsam nach rechts gehen.

\--- task \---

Füge dem `wenn ich als Klon entstehe`{:class="block3control"}-Teil Code hinzu, damit die Katzenfigur `zehn Schritte geht`{:class="block3motion"} und alle 0,1 Sekunden zwischen den beiden Kostümen der Figur wechselt damit die Katze so aussieht, als würde sie laufen.

![Cat sprite](images/cat-sprite.png)

\--- hints \--- \--- hint \---

Die Katzenfigur sollte `10 Schritte gehen`{:class="block3motion"} und alle `0,1 Sekunden`{:class="block3control"} `das Kostüm wechseln`{:class="block3looks"}. Dieser Code sollte `fortlaufend wiederholt`{:class="block3control"} werden, genau wie der Code, der die Katze fallen lässt.

\--- /hint \---

\--- hint \---

Hier sind die Codeblöcke die du brauchst:

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

\--- /hint \---

\--- hint \---

So sollte dein Code aussehen:

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

Drücke die grüne Flagge und überprüfe, ob sich die Katzen jetzt entlang der blauen Plattform am unteren Rand bewegen.

\--- /task \---

If you draw a bridge across the gap so that the cats can get all the way to the right side of the Stage, you can see that they end up getting stuck walking into the right wall.

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

You may notice that, if the cats fall into the hole, they don't disappear but instead get stuck at the bottom. This is because they keep trying to fall downwards.

This is the part of the code that tells the cat to keep falling until it touches blue:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

However, in the hole, the cat can never reach blue, so it is stuck forever.

\--- task \---

Add more blocks to this loop so that it repeats until the cat sprite is touching blue `or`{:class="block3operators"} `touching the edge`{:class="block3sensing"}. This way, the sprite stops trying to fall if it reaches the edge of the Stage.

![Cat sprite](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---