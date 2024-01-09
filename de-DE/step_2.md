## Linien zeichnen

\--- task \---

Öffne das "KATZEN!" Scratch Starter Projekt.

**Online:** open the starter project at [rpf.io/cats-on](https://rpf.io/cats-on){:target="_blank"}.

Wenn du bereits einen Scratch-Account besitzt, kannst du dir durch klicken auf **Remix** eine Kopie anlegen.

**Offline:** open the [starter project](https://rpf.io/p/en/cats-go) in the offline editor. If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Füge die Malstift Erweiterung zu deinem Projekt hinzu.

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

Klicke auf die Figur mit dem Namen "Stift" und füge einen Code hinzu, um die Stiftfarbe auf das gleiche Blau wie die Hindernisse auf der Bühne einzustellen.

![Stift Figur](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Um eine Farbe auszuwählen, klicke auf das Farbquadrat im Block `setze Stiftfarbe auf`{:class="block3extensions"}, damit sich dein Mauszeiger in eine Pipette verwandelt, und klicke dann auf der Bühne auf die richtige Farbe.

\--- /task \---

\--- task \---

Füge weiteren Code hinzu, damit die Figur dem Mauszeiger folgt. Teste dein Programm, um zu überprüfen, ob der Code funktioniert.

![Stift Figur](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Füge einen Code hinzu, um die Figur anzuweisen, eine Linie auf der Bühne zu zeichnen, wenn die Maustaste gedrückt wird.

![Stift Figur](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`Falls`{:class="block3control"} die `Maustaste gedrückt`{:class="block3sensing"} ist, `schalte Stift ein`{:class="block3extensions"} und `sonst`{:class="block3control"}, `schalte Stift aus`{:class="block3extensions"}.

\--- /hint \---

\--- hint \---

Hier sind die Codeblöcke, die du brauchst:

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

\--- /hint \---

\--- hint \---

So sollte dein Code aussehen:

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

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Teste deinen Code. Du solltest in der Lage sein, mit der Maus zu klicken und zu ziehen, um eine blaue Linie auf der Bühne zu zeichnen.

![Zeichne eine Linie](images/draw-a-line.png)

\--- /task \---

Du siehst wahrscheinlich, dass immer ein blauer Punkt in der oberen rechten Ecke der Bühne erscheint (er ist im Bild oben eingekreist). Das liegt daran, dass du beim Klicken auf die grüne Flagge, um das Spiel zu starten, die Maustaste drückst und der Stift sofort mit dem Zeichnen beginnt.

\--- task \---

Um dies zu verhindern, füge am Anfang des Skripts einen `schalte Stift aus`{:class="block3extensions"}-Block und einen `warte 1 Sekunde`{:class="block3control"}-Block über den `wiederhole fortlaufend`{:class="block3control"} block hinzu.

![Stift Figur](images/pen-sprite.png)

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

\--- /task \---