## Adhereix-los a les línies

És possible que notis que, si dibuixes un pont baix entre les dues plataformes, o bé una línia inclinada cap amunt, els gats acaben caminant a través de la plataforma en lloc de per sobre!

![Gats caminant a través de la plataforma](images/cat-walk-through-platform.png)

\--- task \---

En el codi del personatge del gat, afegeix un altre bucle abans del bloc `següent vestit`{:class="block3looks"}. Aquesta vegada, el bucle hauria de dir al gat que es mogui cap amunt per`2` fins que no toqui el blau.

![Personatge del gat](images/cat-sprite.png)

\--- hints \--- \--- hint \---

El gat hauria de `pujar 2`{:class="block3motion"} `repetidament fins que`{:class="block3control"} `no`{:class="block3operators"} `toqui el color blau`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Aquí tens els blocs que necessites:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

Així és com s'hauria de veure el teu codi:

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

Fes clic a la bandera verda i prova de dibuixar una línia inclinada cap amunt. Comprova que el teu gat segueixi aquesta línia.

\--- /task \---