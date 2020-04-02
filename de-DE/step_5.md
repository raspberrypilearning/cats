## Auf der Linie bleiben

Du wirst vielleicht bemerken, dass wenn du eine niedrige Brücke zwischen den beiden Plattformen zeichnest oder eine Linie, die nach oben läuft, die Katzen eher durch die Plattform laufen als auf ihr!

![Katzen, die durch die Plattform laufen](images/cat-walk-through-platform.png)

\--- task \---

Füge im Code für die Katzenfigur eine weitere Schleife vor dem `nächsten Kostüm`{:class="block3looks"}-Block hinzu. Dieses Mal sollte die Schleife die Katze anweisen, sich um `2` nach oben zu bewegen, bis sie kein blau mehr berührt.

![Katzen Figur](images/cat-sprite.png)

\--- hints \--- \--- hint \---

Die Katze sollte sich `wiederholt`{:class="block3control"} `um 2 Schritte nach oben`{:class="block3motion"} bewegen `bis`{:class="block3control"} sie `nicht`{:class="block3operators"} `Blau berührt`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Hier sind die Codeblöcke die du brauchst:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

So sollte dein Code aussehen:

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

Klicke auf die grüne Fahne und versuche eine Linie zu zeichnen, die nach oben ansteigt. Überprüfe, ob deine Katze dieser Linie folgt.

\--- /task \---