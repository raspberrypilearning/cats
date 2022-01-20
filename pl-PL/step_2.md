## Narysuj linie

--- task ---

Otwórz startowy projekt Scratch "KOTY!".

**Online:** otwórz projekt początkowy Scratch na stronie [scratch.mit.edu/projects/382683951](https://scratch.mit.edu/projects/382683951){:target="_blank"}.

Jeśli posiadasz konto Scratch, możesz utworzyć kopie poprzez kliknięcie **Remiks**.

**Offline:** otwórz [projekt startowy](https://rpf.io/p/pl-PL/cats-go) w edytorze offline. Jeśli musisz pobrać i zainstalować edytor Scratcha, znajdziesz go na stronie [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

Dodaj rozszerzenie pióra do swojego projektu.

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

Kliknij na duszka o nazwie 'ołówek' i dodaj kod, aby ustawić kolor pióra na ten sam niebieski co przeszkody na scenie.

![Duszek ołówka](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Aby wybrać kolor, kliknij kwadrat koloru w bloku `ustaw kolor pióra`{:class="block3extensions"}, aby kursor myszy zmienił się w pipetę, a następnie kliknij odpowiedni kolor na stole montażowym.

--- /task ---

--- task ---

Dodaj trochę kodu, aby duszek podążał za wskaźnikiem myszy. Przetestuj swój program, aby sprawdzić, czy kod działa.

![Duszek ołówka](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

Dodaj kod, aby powiedzieć duszkowi, aby narysował linię na scenie, jeśli przycisk myszy jest wciśnięty.

![Duszek ołówka](images/pen-sprite.png)

--- hints ---
 --- hint ---

`Jeśli`{:class="block3control"} `kliknięto myszką?`{:class="block3sensing"}, to`przyłóż pisak`{:class="block3extensions"}, `w przeciwnym razie`{:class="block3control"}, `podnieś pisak`{:class="block3extensions"}.

--- /hint ---

--- hint ---

Oto potrzebne bloki kodu:

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

Tak powinien wyglądać Twój kod:

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

Przetestuj swój kod. Powinieneś być w stanie kliknąć i przeciągnąć myszką, aby narysować niebieską linię na scenie.

![Narysuj linię](images/draw-a-line.png)

--- /task ---

Prawdopodobnie widzisz, że niebieska kropka zawsze pojawia się w prawym górnym rogu sceny (jest zakreślona na obrazku powyżej). Dzieje się tak, ponieważ gdy klikniesz zieloną flagę, aby rozpocząć grę, naciskasz myszkę w dół, a więc długopis natychmiast zaczyna rysować.

--- task ---

Aby temu zapobiec zdarzeniom, dodać bloczek `podnieś pisak`{:class="block3extensions"} bloku na początku skryptu i bloczek `czekaj 1 sekund`{:class="block3control"} powyżej bloczka `zawsze`{:class="block3control"}.

![Duszek ołówka](images/pen-sprite.png)

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
