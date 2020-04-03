## Alcançar a segurança

O objetivo do jogo é guiar os gatos para a segurança, criando um caminho para que eles possam alcançar a porta. Cria uma variável de pontuação para controlar quantos gatos chegam à porta.

--- task ---

Cria uma nova variável chamada `pontuação`{:class="block3variables"}.

![Ator gato](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Adiciona código ao teu ator de gato para adicionar `1` à `pontuação`{:class="block3variables"} de cada vez que um gato chega à porta. Define também a `pontuação`{:class="block3variables"} como `0` `quando alguém clicar a bandeira`{:class="block3events"} no início do jogo.

![Ator gato](images/cat-sprite.png)

--- hints ---
 --- hint ---

`Se`{:class="block3control"} o gato está `a tocar no ator porta`{:class="block3sensing"}, então, `adiciona a pontuação o valor 1`{:class="block3variables"}.

--- /hint ---

--- hint ---

Estes são os novos blocos de código que necessitas adicionar ao teu comando `quando fores criado como um clone`:

```blocks3
change [pontuação v] by (1)

if <> then
end

<touching (Porta v)?>

set [pontuação v] to (0)
```

--- /hint ---

--- hint ---

Este é o aspeto que o teu código deve ter:

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
+   if <touching (Porta v)?> then
        change [pontuação v] by (1)
    end
end
delete this clone

when flag clicked
+ set [pontuação v] to (0)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Acrescenta um pouco mais de código para que se oiça miar sempre que um ator gato chega à porta, e depois então desapareça.

![Ator gato](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

--- /task ---