## Aderir à linhas

Podes já ter notado que, se desenhares uma ponte baixa entre as duas plataformas, ou uma linha que inclina para cima, os gatos acabam por caminhar através da plataforma e não por cima dela!

![Gatos a andar na plataforma](images/cat-walk-through-platform.png)

\--- task \---

No código do ator gato, adiciona outro ciclo antes do bloco `passa para o teu próximo traje` {: class = "block3looks"}. Desta vez, o ciclo deve dizer ao gato para subir ` 2 ` até não estar a tocar na cor azul.

![Ator gato](images/cat-sprite.png)

\--- hints \--- \--- hint \---

O gato deve ` subir 2 ` {: class = "block3motion"} ` até ` {: class = "block3control"} ` não estar a ` {: class = "block3operators"} ` tocar na cor azul ` {: class = "block3sensing"}.

\--- /hint \---

\--- hint \---

Estes são os blocos de que necessitas:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

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
end
delete this clone
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Clica na bandeira verde e tenta desenhar uma linha inclinada para cima. Verifica se o teu gato segue a linha.

\--- /task \---