## Katzen klonen

Du möchtest einen endlosen Strom von Katzen, die der Spieler auf den Weg zum Ausgang führen muss.

\--- task \---

Klicke auf die Figur namens 'Katze' und füge einen Code hinzu, um sie zu `verstecken`{:class="block3looks"} und um sie alle drei Sekunden zu `klonen`{:class="block3control"}.

![Katzen Figur](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

Wenn du das Programm jetzt ausführst, passiert auf der Bühne nichts. Um zu überprüfen, ob alle drei Sekunden ein neuer Katzen-Figur-Klon erstellt wird, lasse jeden Klon erscheinen und vom Himmel fallen.

\--- task \---

Füge einen Code hinzu, um der Figur mitzuteilen, dass sie `wenn sie als Klon entsteht`{:class="block3control"}, sich selbst `zeigen`{:class="block3looks"} und fallen soll, bis sie den blauen Boden `berührt`{:class="block3sensing"}, der auf der Bühne gezeichnet wird.

![Katzen Figur](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Wenn die Figur als Klon entsteht`{:class="block3control"}, `zeige`{:"block3looks"} die Figur. `Ändere`{:class="block3motion"} die `y`-Koordinate der Figur `wiederholt`{:class="block3control"} um `-2`, bis die Figur die blaue Bühne `berührt`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Hier sind die Codeblöcke die du brauchst:

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

So sollte dein Code aussehen:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

Wenn du auf die grüne Flagge klickst, sollte alle drei Sekunden eine neue Katze vom oberen Rand der Bühne fallen. Jede Katze sollte in einem großen Haufen überlappender Katzen auf dem blauen Boden unten landen.

![Fallende Katzen](images/falling-cats.png)