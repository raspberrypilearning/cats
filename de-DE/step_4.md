## Lass die Katzen sich bewegen

Sobald eine Katze den Boden erreicht, sollte sie langsam nach rechts gehen.

\--- task \---

Füge dem `wenn ich als Klon entstehe`{:class="block3control"}-Teil Code hinzu, damit die Katzenfigur `zehn Schritte geht`{:class="block3motion"} und alle 0,1 Sekunden zwischen den beiden Kostümen der Figur wechselt damit die Katze so aussieht, als würde sie laufen.

![Katzen Figur](images/cat-sprite.png)

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

Wenn du eine Brücke über die Lücke zeichnest, damit die Katzen bis zur rechten Seite der Bühne gelangen können, wirst du sehen, dass sie beim Laufen in die rechte Wand stecken bleiben.

![Strampelnde Katzen am Rand](images/flailing-at-edge.png)

\--- task \---

Entferne die `fortlaufend`{:class="block3control"}- Schleife und füge stattdessen eine andere Schleife ein, damit die Katzen nur so lange laufen, bis sie eine Kante erreichen. Wenn eine Katze den Bühnenrand erreicht, sollte sie verschwinden.

![Katzen Figur](images/cat-sprite.png)

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

Drücke die grüne Flagge und überprüfe, ob die Katzen verschwinden, wenn sie den Bühnenrand erreichen.

\--- /task \---

Du hast vielleicht bemerkt, dass die Katzen, wenn sie in das Loch fallen, nicht verschwinden, sondern am Boden stecken bleiben. Dies liegt daran, dass sie immer wieder versuchen, nach unten zu fallen.

Das ist der Teil des Codes, der der Katze sagt, dass sie weiter fallen soll, bis sie blau berührt:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

In dem Loch kann die Katze jedoch niemals blau erreichen, so sitzt sie für immer fest.

\--- task \---

Füge dieser Schleife weitere Blöcke hinzu, sodass sie wiederholt wird, bis die Katzenfigur etwas blaues berührt `oder`{:class="block3operators"} sie den `Rand berührt`{:class="block3sensing"}. Auf diese Weise versucht die Figur nicht mehr zu fallen, wenn sie den Rand der Bühne erreicht.

![Katzen Figur](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---