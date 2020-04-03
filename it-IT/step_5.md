## Aderisci alle linee

Potresti notare che, se disegni un ponte basso tra le due piattaforme, o una linea che va verso l'alto, i gatti finiscono per camminare attraverso la piattaforma anziché su di essa!

![Gatti che camminano attraverso la piattaforma](images/cat-walk-through-platform.png)

--- task ---

Nel codice per lo sprite del gatto, aggiungi un altro ciclo prima del blocco `passa la costume seguente`{:class="block3looks"}. Stavolta, il ciclo dovrebbe dire al gatto di muoversi verso l'alto di `2` fino a quando non tocca il blu.

![Sprite gatto](images/cat-sprite.png)

--- hints ---
 --- hint ---

Il gatto dovrebbe `spostarsi verso l'alto di 2`{:class="block3motion"} `ripetutamente fino a che`{:class="block3control"} `non`{:class="block3operators"} `tocca il blu`{:class="block3sensing"}.

--- /hint ---

--- hint ---

Ecco i blocchi di codice che ti servono:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

--- /hint ---

--- hint ---

Ecco come dovrebbe apparire il tuo codice:

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

Fai clic sulla bandiera verde e prova a tracciare una linea che si inclina verso l'alto. Controlla che il tuo gatto segua questa linea.

--- /task ---