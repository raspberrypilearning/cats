## In veiligheid komen

Het doel van het spel is om de katten in veiligheid te brengen door een pad te maken zodat ze de deur kunnen bereiken. Maak een score variabele om bij te houden hoeveel katten de deur bereiken.

--- task ---

Maak een variabele met de naam `score`{:class="block3variables"}.

![Kat sprite](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Voeg code toe aan de kat sprite om `1` toe te voegen aan de `score`{:class="block3variables"} elke keer dat een kat de deur bereikt. Stel de `score`{:class="block3variables"} in op `0` `wanneer op de vlag wordt geklikt`{:class="block3events"} aan het begin van het spel.

![Kat sprite](images/cat-sprite.png)

--- hints ---
 --- hint ---

`Als`{:class="block3control"} de kat `de deur sprite raakt`{:class="block3sensing"}, verander dan de `score met 1`{:class="block3variables"}.

--- /hint ---

--- hint ---

Hier zijn de nieuwe codeblokken die je aan het `wanneer ik als kloon start` script toe moet voegen:

```blocks3
verander [score v] met (1)

als <> dan
einde

<touching (Door v)?>

maak [score v] (0)
```

--- /hint ---

--- hint ---

Dit is hoe je code eruit zou moeten zien:

```blocks3
wanneer ik als kloon start
verschijn
herhaal tot <touching (edge v)?>
    neem (10) stappen
    herhaal tot <touching color [#0000ff]?>
        verander y met (-2)
    einde
    herhaal tot <not <touching color [#0000ff]?>>
        verander y met (2)
    einde
    volgend uiterlijk
    wacht (0.1) sec.
+ als <touching (Door v)?> dan
        verander [score v] met (1)
    einde
einde
verwijder deze kloon

wanneer op de groene vlag wordt geklikt

+ maak [score v] (0)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Voeg nog wat code toe zodat, wanneer een kat sprite de deur bereikt, de kat een 'miauw' geluid maakt en dan verdwijnt.

![Cat sprite](images/cat-sprite.png)

```blocks3
start geluid (meow v)
verwijder deze kloon
```

--- /task ---