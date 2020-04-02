## Blijf bij de lijnen

Het valt je misschien op dat, als je een lage brug tussen de twee platforms trekt, of een lijn die omhoog loopt, de katten uiteindelijk door het platform lopen in plaats van er bovenop!

![Katten lopen door het platform](images/cat-walk-through-platform.png)

--- task ---

Voeg in de code voor de kat sprite nog een lus toe vóór het `volgend uiterlijk`{:class="block3looks"} blok. Deze keer moet de lus de kat vertellen om met `2` omhoog te gaan totdat deze blauw niet raakt.

![Kat sprite](images/cat-sprite.png)

--- hints --- --- hint ---

De kat moet `2 stappen omhoog`{:class="block3motion"} `totdat`{:class="block3control"} hij `niet`{:class="block3operators"} `blauw raakt`{:class="block3sensing"}.

--- /hint ---

--- hint ---

Dit zijn de codeblokken die je nodig hebt:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

--- /hint ---

--- hint ---

Dit is hoe je code eruit zou moeten zien:

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

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Klik op de groene vlag en probeer een lijn te tekenen die omhoog loopt. Controleer dat de kat deze lijn volgt.

--- /task ---