## Faça os gatos se moverem

Uma vez que o gato chega ao chão, deve avançar lentamente para a direita.

\--- task \---

Adicione código à seção `quando eu começar como um clone`{:class="block3control"} para fazer com que o ator Gato se `mova 10 passos`{:class="block3motion"}, e alterne entre as duas fantasias do ator a cada 0,1 segundos para fazer o gato parecer andar.

![Cat sprite](images/cat-sprite.png)

\--- hints \--- \--- hint \---

O ator Gato deve `mover 10 passos`{:class="block3motion"} e `mude para a fantasia ()`{:class="block3looks"} a cada `0,1 segundos`{:class="block3control"}. Este código deve repetir `sempre`{:class="block3control"}, assim como o código para fazer o gato cair.

\--- /hint \---

\--- hint \---

Aqui estão os blocos de código que você precisa:

```blocks3
mova (10) passos

espere(0.1) seg

próxima fantasia

sempre
fim
```

\--- /hint \---

\--- hint \---

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
    espere(0.1) seg.
fim
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Pressione a bandeira verde e verifique se os gatos agora se movem ao longo da plataforma azul na parte inferior.

\--- /task \---

If you draw a bridge across the gap so that the cats can get all the way to the right side of the Stage, you can see that they end up getting stuck walking into the right wall.

![Flailing cats at the edge](images/flailing-at-edge.png)

\--- task \---

Remove the `forever`{:class="block3control"} loop, and instead add a different loop to make the cats only walk until they reach an edge. When a cat reaches the edge of the Stage, it should disappear.

![Cat sprite](images/cat-sprite.png)

```blocks3
when I start as a clone
show
+ repeat until <touching (edge v)?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
+ delete this clone
```

\--- /task \---

\--- task \---

Press the green flag and check that the cats disappear when they reach the edge of the Stage.

\--- /task \---

You may notice that, if the cats fall into the hole, they don't disappear but instead get stuck at the bottom. This is because they keep trying to fall downwards.

This is the part of the code that tells the cat to keep falling until it touches blue:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

However, in the hole, the cat can never reach blue, so it is stuck forever.

\--- task \---

Add more blocks to this loop so that it repeats until the cat sprite is touching blue `or`{:class="block3operators"} `touching the edge`{:class="block3sensing"}. This way, the sprite stops trying to fall if it reaches the edge of the Stage.

![Cat sprite](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---