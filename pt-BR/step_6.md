## Vá para o abrigo

O objetivo do jogo é guiar os gatos para o abrigo em segurança, criando um caminho para que eles possam chegar na porta. Crie uma variável de pontuação para registrar quantos gatos chegam na porta.

\--- task \---

Crie uma nova variável chamada `pontuação`{:class="block3variables"}.

![Cat sprite](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Adicione código ao ator Gato para adicionar `1` à `pontuação`{:class="block3variables"} cada vez que um gato chega na porta. Defina também `pontos`{:class="block3variables"} como `0` `quando bandeira verde for clicado` {: class = "block3events"} no início do jogo.

![Cat sprite](images/cat-sprite.png)

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
+   if <touching (Door v)?> then
        change [score v] by (1)
    end
end
delete this clone

when flag clicked

+ set [score v] to (0)
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Add some more code so that, when a cat sprite reaches the door, the cat makes a 'meow' sound and then disappears.

![Cat sprite](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

\--- /task \---