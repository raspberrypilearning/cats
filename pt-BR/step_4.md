## Faça os gatos se moverem

Uma vez que o gato chega ao chão, deve avançar lentamente para a direita.

--- task ---

Adicione código à seção `quando eu começar como um clone`{:class="block3control"} para fazer com que o ator Gato se `mova 10 passos`{:class="block3motion"}, e alterne entre as duas fantasias do ator a cada 0,1 segundos para fazer o gato parecer andar.

![ator Gato](images/cat-sprite.png)

--- hints ---
 --- hint ---

O ator Gato deve `mover 10 passos`{:class="block3motion"} e `mude para a fantasia ()`{:class="block3looks"} a cada `0.1 segundos`{:class="block3control"}. Este código deve repetir `sempre`{:class="block3control"}, assim como o código para fazer o gato cair.

--- /hint ---

--- hint ---

Aqui estão os blocos de código que você precisa:

```blocks3
mova (10) passos

wait (0.1) seconds

próxima fantasia

sempre
fim
```

--- /hint ---

--- hint ---

É assim que seu código deve parecer:

```blocks3
quando eu começar como um clone
mostre
+ sempre
    mova (10) passos
    repita até que <touching color [#0000ff]?>
        adicione (-2) a y
    fim
    próxima fantasia
    wait (0.1) seconds
fim
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Pressione a bandeira verde e verifique se os gatos agora se movem ao longo da plataforma azul na parte inferior.

--- /task ---

Se você desenhar uma ponte através da abertura para que os gatos possam chegar até o lado direito do Palco, poderá ver que eles acabam ficando presos andando para a parede direita.

![Gatos agitados na borda](images/flailing-at-edge.png)

--- task ---

Remova o laço `sempre`{:class="block3control"} e adicione um laço diferente para fazer com que os gatos andem apenas até atingirem uma borda. Quando um gato chega na borda do palco, ele deve desaparecer.

![ator Gato](images/cat-sprite.png)

```blocks3
quando eu começar como um clone
mostre
+ repita até que <touching (edge v)?>
    mova(10) passos
    repita até que <touching color [#0000ff]?>
        adicione (-2) a y
    fim
    próxima fantasia
    espere (0.1) seg
fim
+ apague este clone
```

--- /task ---

--- task ---

Pressione a bandeira verde e verifique se os gatos desaparecem quando chegam na borda do palco.

--- /task ---

Você pode perceber que, se os gatos caem no buraco, eles não desaparecem, mas ficam presos no fundo. Isso acontece porque eles continuam tentando cair mais fundo.

Esta é a parte do código que diz ao gato para continuar caindo até tocar no azul:

```blocks3
repita até que <touching color [#0000ff]?>
fim
```

Entretanto, no buraco, o gato nunca pode chegar no azul, por isso fica preso para sempre.

--- task ---

Adicione mais blocos a esse loop para que ele repita até o ator Gato tocar no azul `ou`{:class="block3operators"} `tocando em borda`{:class="block3sensing"}. Dessa forma, o ator para de tentar cair se atingir a borda do Palco.

![ator Gato](images/cat-sprite.png)

```blocks3
repita até que <<touching color [#0000ff]?> ou <touching (edge v)?>>
fim
```

--- /task ---