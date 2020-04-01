## Kloon katten

Je wilt een eindeloze stroom katten die de speler langs het pad naar de uitgang moet leiden.

--- task ---

Klik op de sprite genaamd 'Cat' en voeg wat code toe om `verdwijn`{:class="block3looks"} de sprite te verbergen, en ook om elke drie seconden een `kloon`{:class="block3control"} van hem te maken.

![Kat sprite](images/cat-sprite.png)

```blocks3
wanneer op groene vlag wordt geklikt
verdwijn
herhaal
    maak een kloon van (mijzelf v)
    wacht (3) sec.
einde
```

--- /task ---

Als je het programma nu uitvoert, gebeurt er niets in het speelveld. Om te controleren of er om de drie seconden een nieuwe Kat sprite kloon wordt gemaakt, laat je elke kloon verschijnen en uit de lucht vallen.

--- task ---

Voeg code toe om de sprite te vertellen dat `wanneer ik als kloon start`{:class="block3control"}, hij moet `verschijnen`{:class="block3looks"} en vallen totdat hij de blauwe vloer `raakt`{:class="block3sensing"} die in het speelveld is getekend.

![Kat sprite](images/cat-sprite.png)

--- hints ---
 --- hint ---

`Wanneer ik als kloon start`{:class="block3control"}, `verschijnt`{:class="block3looks"} de sprite. `Herhaal`{:class="block3control"} `Verander`{:class="block3motion"} de `y` coördinaat van de sprite met `-2`, totdat de sprite de blauwe vloer `raakt`{:class="block3sensing"}.

--- /hint ---

--- hint ---

Dit zijn de codeblokken die je nodig hebt:

```blocks3
herhaal tot <>
einde

verschijn

<touching color [#0000ff]?>

verander y met (-2)

wanneer ik als kloon start
```

--- /hint ---

--- hint ---

Dit is hoe je code eruit zou moeten zien:

```blocks3
wanneer ik als kloon start
verschijn
herhaal tot <touching color [#0000ff]?>
verander y met (-2)
einde
```

--- /hint ------ /hints ---

--- /task ---

Als je op de groene vlag klikt, zou je elke drie seconden een nieuwe kat van de bovenkant van het speelveld moeten zien vallen. Elke kat moet in een grote stapel overlappende katten op de blauwe bodem onderaan landen.

![Vallende katten](images/falling-cats.png)