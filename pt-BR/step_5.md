## Fiquem nas linhas

Você pode ter notado que, se você desenhar uma ponte baixa entre as duas plataformas, ou uma linha que inclina para cima, os gatos acabam por caminhar através da plataforma e não por cima dela!

![Gatos andando através da plataforma](images/cat-walk-through-platform.png)

--- task ---

No código do ator Gato, adicione outro laço antes do bloco `próxima fantasia`{:class="block3looks"}. Desta vez, o laço deve dizer ao gato para subir `2` até não tocar na cor azul.

![ator Gato](images/cat-sprite.png)

--- hints ---
 --- hint ---

O gato deve `subir 2`{:class="block3motion"} de maneira `repetida até que`{:class="block3control"} esteja `não`{:class="block3operators"} `tocando na cor azul`{:class="block3sensing"}.

--- /hint ---

--- hint ---

Aqui estão os blocos de código que você precisa:

```blocks3
<touching color [#0000ff]?>

adicione (2) a y

repita até que <>
fim

não <>
```

--- /hint ---

--- hint ---

É assim que seu código deve parecer:

```blocks3
quando eu começar como um clone
mostre
repita até que <touching (edge v)?>
    mova(10) passos
    repita até que <touching color [#0000ff]?>
        adicione (-2) a y
    fim
    repita até que <not <touching color [#0000ff]?>>
        adicione (2) a y
    fim
    próxima fantasia
    espere (0.1) seg
fim
apague este clone
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Clique na bandeira verde e tente desenhar uma linha inclinada para cima. Verifique se o gato segue a linha.

--- /task ---