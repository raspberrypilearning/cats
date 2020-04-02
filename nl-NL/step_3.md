## Kloon katten

Je wilt een eindeloze stroom katten die de speler langs het pad naar de uitgang moet leiden.

--- task ---

Klik op de sprite genaamd 'Kat' en voeg wat code toe om de sprite te laten `verdwijnen`{:class="block3looks"}, en ook om er elke drie seconden een `kloon`{:class="block3control"} van te maken.

![Kat sprite](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

--- /task ---

Als je het programma nu uitvoert, gebeurt er niets in het speelveld. Om te controleren of er om de drie seconden een nieuwe Kat sprite kloon wordt gemaakt, laat je elke kloon verschijnen en uit de lucht vallen.

--- task ---

Voeg code toe om de sprite te vertellen dat `wanneer ik als kloon start`{:class="block3control"}, hij moet `verschijnen`{:class="block3looks"} en vallen totdat hij de blauwe vloer `raakt`{:class="block3sensing"} die in het speelveld is getekend.

![Kat sprite](images/cat-sprite.png)

--- hints --- --- hint ---

`Wanneer ik als kloon start`{:class="block3control"}, `verschijnt`{:class="block3looks"} de sprite. `Herhaal`{:class="block3control"} `Verander`{:class="block3motion"} de `y` coördinaat van de sprite met `-2`, totdat de sprite de blauwe vloer `raakt`{:class="block3sensing"}.

--- /hint ---

--- hint ---

Dit zijn de codeblokken die je nodig hebt:

```blocks3
repeat until <>
end

show

<touching color [#0000ff]?>

change y by (-2)

when I start as a clone
```

--- /hint ---

--- hint ---

Dit is hoe je code eruit zou moeten zien:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

--- /hint --- --- /hints ---

--- /task ---

Als je op de groene vlag klikt, zou je elke drie seconden een nieuwe kat van de bovenkant van het speelveld moeten zien vallen. Elke kat moet in een grote stapel overlappende katten op de blauwe bodem onderaan landen.

![Vallende katten](images/falling-cats.png)