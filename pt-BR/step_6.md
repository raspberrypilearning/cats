## Vá para o abrigo

O objetivo do jogo é guiar os gatos para o abrigo em segurança, criando um caminho para que eles possam chegar na porta. Crie uma variável de pontuação para registrar quantos gatos chegam na porta.

\--- task \---

Crie uma nova variável chamada `pontuação`{:class="block3variables"}.

![ator Gato](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Adicione código ao ator Gato para adicionar `1` à `pontuação`{:class="block3variables"} cada vez que um gato chega na porta. Defina também `pontos`{:class="block3variables"} como `0` `quando bandeira verde for clicado` {: class = "block3events"} no início do jogo.

![ator Gato](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`Se`{:class="block3control"} o gato está `tocando em Porta`{:class="block3sensing"}, então, `adiciona 1 a pontuação`{:class="block3variables"}.

\--- /hint \---

\--- hint \---

Estes são os novos blocos de código que você precisa adicionar ao seu script `quando eu começar como um clone`:

```blocks3
adicione (1) a [pontuação v]
se <> então
fim

<touching (Door v)?>

mude [pontuação v] para (0)
```

\--- /hint \---

\--- hint \---

É assim que seu código deve parecer:

```blocks3
quando eu começar comp um clone
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
+   se <touching (Door v)?> então
        adicione (1) a [pontuação v]
    fim
fim
apague este clone

quando bandeira verde for clicado

+ mude [pontuação v] para (0)
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Adicione um pouco mais de código para que, quando o gato chegar na porta, o gato faça o som 'miau' e depois então desapareça.

![ator Gato](images/cat-sprite.png)

```blocks3
toque o som (miau v)
apague este clone
```

\--- /task \---