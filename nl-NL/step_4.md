## Laat de katten bewegen

Zodra een kat de vloer bereikt, moet hij langzaam naar rechts stappen.

--- task ---

Voeg code toe aan de `wanneer ik als kloon start`{:class="block3control"} sectie om de kat sprite `neem tien stappen`{:class="block3motion"} te laten bewegen, en schakel elke 0,1 seconden tussen de twee uiterlijken van de sprite om de kat eruit te laten zien alsof hij loopt.

![Kat sprite](images/cat-sprite.png)

--- hints ---
 --- hint ---

De sprite van de kat moet `neem 10 stappen`{:class="block3motion"} en `volgend uiterlijk`{:class="block3looks"} elke `0.1 seconden`{:class="block3control"}. Deze code moet altijd `herhalen`{:class="block3control"}, net als de code om de kat te laten vallen.

--- /hint ---

--- hint ---

Dit zijn de codeblokken die je nodig hebt:

```blocks3
neem (10) stappen

wacht (0.1) sec.

volgend uiterlijk

herhaal
einde
```

--- /hint ---

--- hint ---

Dit is hoe je code eruit zou moeten zien:

```blocks3
wanneer ik als kloon start
verschijn
+ herhaal
    neem (10) stappen
    herhaal tot <touching color [#0000ff]?>
        verander y met (-2)
    einde
    volgend uiterlijk
    wacht (0.1) sec.
einde
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Druk op de groene vlag en controleer of de katten nu langs het blauwe platform onderaan bewegen.

--- /task ---

Als je een brug over de opening tekent, zodat de katten helemaal naar de rechterkant van het speelveld kunnen komen, kun je zien dat ze vast komen te zitten in de rechtermuur.

![Zwervende katten aan de rand](images/flailing-at-edge.png)

--- task ---

Verwijder de `herhaal`{:class="block3control"} lus en voeg in plaats daarvan een andere lus toe om de katten alleen te laten lopen totdat ze een rand bereiken. Wanneer een kat de rand van het speelveld bereikt, moet hij verdwijnen.

![Kat sprite](images/cat-sprite.png)

```blocks3
wanneer ik als kloon start
verschijn
+ herhaal tot <touching (rand v)?>
    neem (10) stappen
    herhaal tot <touching color [#0000ff]?>
        verander y met (-2)
    einde
    volgend uiterlijk
    wacht (0.1) sec.
einde
+ verwijder deze kloon
```

--- /task ---

--- task ---

Druk op de groene vlag en controleer dat de katten verdwijnen wanneer ze de rand van het speelveld bereiken.

--- /task ---

Je merkt misschien dat, als de katten in het gat vallen, ze niet verdwijnen maar in plaats daarvan vast komen te zitten aan de onderkant. Dit komt omdat ze blijven proberen naar beneden te vallen.

Dit is het deel van de code dat de kat vertelt dat hij moet blijven vallen totdat hij blauw raakt:

```blocks3
herhaal tot <touching color [#0000ff]?>
einde
```

In het gat kan de kat echter nooit blauw bereiken, dus zit hij voor altijd vast.

--- task ---

Voeg meer blokken toe aan deze lus zodat deze wordt herhaald totdat de kat sprite blauw raakt `of`{:class="block3operators"} `de rand raakt`{:class="block3sensing"}. Op deze manier stopt de sprite met vallen als het de rand van het speelveld bereikt.

![Kat sprite](images/cat-sprite.png)

```blocks3
herhaal tot <<touching color [#0000ff]?> of <touching (rand v)?>>
einde
```

--- /task ---