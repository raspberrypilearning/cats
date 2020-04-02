## Teken lijnen

--- task ---

Open het 'CATS!' Scratch startproject.

**Online:** open het startproject op [rpf.io/cats-on](http://rpf.io/cats-on){:target="_ blank"}.

Als je een Scratch account hebt, kun je een kopie maken door op **Remix** te klikken.

**Offline:** open het [startproject](http://rpf.io/p/nl-NL/cats-go) in de offline editor. Als je de Scratch offline editor wilt downloaden en installeren dan kan je die vinden op [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

Voeg de Pen uitbreiding toe aan je project.

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

Klik op de sprite genaamd 'Pen' en voeg code toe om de penkleur in te stellen op hetzelfde blauw als de obstakels in het speelveld.

![Pen sprite](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Om een kleur te selecteren, klik je op het kleurenvierkant in het blok `maak penkleur`{:class="block3extensions"} om je muiscursor in een pipet te veranderen en vervolgens klik je op de juiste kleur in het speelveld.

--- /task ---

--- task ---

Voeg nog wat code toe om de sprite de muisaanwijzer te laten volgen. Test je programma om te controleren of de code werkt.

![Pen sprite](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

Voeg wat code toe om de sprite te vertellen een lijn in het speelveld te tekenen als de muisknop ingedrukt wordt.

![Pen sprite](images/pen-sprite.png)

--- hints --- --- hint ---

`Als`{:class="block3control"} de `muis ingedrukt is`{:class="block3sensing"}, zet de `pen neer`{:class="block3extensions"} en `anders`{:class="block3control"}, til de `pen op`{:class="block3extensions"}.

--- /hint ---

--- hint ---

Dit zijn de codeblokken die je nodig hebt:

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

Dit is hoe je code eruit zou moeten zien:

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

Test je code. Je zou moeten kunnen klikken en slepen met de muis om een blauwe lijn in het speelveld te tekenen.

![Teken een lijn](images/draw-a-line.png)

--- /task ---

Je ziet waarschijnlijk dat er altijd een blauwe stip in de rechterbovenhoek van het speelveld verschijnt (deze is omcirkeld in de bovenstaande afbeelding). Dit komt omdat, wanneer je op de groene vlag klikt om het spel te starten, je de muis indrukt en de pen onmiddellijk begint te tekenen.

--- task ---

Om dit te voorkomen, voeg je een `pen op`{:class="block3extensions"} blok toe aan het begin van het script en een `wacht een seconde`{:class="block3control"} blok boven het `herhaal`{:class="block3control"} blok.

![Pen sprite](images/pen-sprite.png)

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