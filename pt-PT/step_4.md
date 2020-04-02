## Faça os gatos se mexerem

Quando um gato atinge o chão, deve pisar lentamente para a direita.

\--- task \---

Adicione código ao `quando eu começar como um clone`{: class = "block3control"} para fazer o sprite de gato `mover dez etapas`{: class = "block3motion"} e alterne entre os dois figurinos do sprite a cada 0,1 segundos para fazer o gato parecer andar.

![Sprite de gato](images/cat-sprite.png)

\--- hints \--- \--- hint \---

O sprite de gato deve `mover 10 etapas`{: class = "block3motion"} e `alternar o traje`{: class = "block3looks"} a cada `0,1 segundos`{: class = "block3control"}. Este código deve repetir `para sempre`{: class = "block3control"}, assim como o código para fazer o gato cair.

\--- /hint \---

\--- hint \---

Estes são os blocos de que necessitas:

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

\--- /hint \---

\--- hint \---

Este é o aspeto que o teu código deve ter:

```blocks3
when I start as a clone
show
+ forever
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Pressione a bandeira verde e verifique se os gatos agora se movem ao longo da plataforma azul na parte inferior.

\--- /task \---

Se você desenhar uma ponte através da abertura para que os gatos possam chegar até o lado direito do Palco, poderá ver que eles acabam ficando presos andando na parede direita.

![Gatos agitados na borda](images/flailing-at-edge.png)

\--- task \---

Remova o loop `para sempre`{: class = "block3control"} e adicione um loop diferente para fazer com que os gatos andem apenas até atingirem uma borda. Quando um gato atinge a borda do palco, ele deve desaparecer.

![Sprite de gato](images/cat-sprite.png)

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

Pressione a bandeira verde e verifique se os gatos desaparecem quando atingem a borda do palco.

\--- /task \---

Você pode perceber que, se os gatos caem no buraco, eles não desaparecem, mas ficam presos no fundo. Isso ocorre porque eles continuam tentando cair para baixo.

Esta é a parte do código que diz ao gato para continuar caindo até tocar em azul:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

No entanto, no buraco, o gato nunca pode chegar ao azul, por isso fica preso para sempre.

\--- task \---

Adicione mais blocos a esse loop para que ele repita até o sprite de gato tocar em azul `ou`{: class = "block3operators"} `tocando na borda`{: class = "block3sensing"}. Dessa forma, o sprite para de tentar cair se atingir a borda do Palco.

![Sprite de gato](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---