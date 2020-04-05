## Clonar gatos

Você quer um fluxo interminável de gatos que o jogador precisa guiar ao longo do caminho até a saída.

--- task ---

Clique no ator chamado 'Gato' e adicione algum código para que se `esconda`{:class="block3looks"} o ator, e também para `crie clone de ()`{:class="block3control"} a cada três segundos.

![ator Gato](images/cat-sprite.png)

```blocks3
when flag clicked
esconda
sempre
    crie clone de (este ator v)
    espere (3) seg
fim
```

--- /task ---

Se você executar o programa agora, nada acontece no palco. Para verificar se um novo clone do ator Gato é criado a cada três segundos, faça com que cada clone apareça e caia do céu.

--- task ---

Adicione código para dizer ao ator que `quando eu começar como um clone`{:class="block3control"}, ele se `mostre`{:class="block3looks"} e caia até que ele `toque`{:class="block3sensing"} o chão azul desenhado no palco.

![ator Gato](images/cat-sprite.png)

--- hints ---
 --- hint ---

`quando eu começar como um clone`{:class="block3control"}, `mostre`{:class="block3looks"} o ator. `Repetidamente`{:class="block3control"} `Adicione`{:class="block3motion"} a coordenada `y` do ator por `-2`, até o ator `tocar`{:class="block3sensing"} no palco azul.

--- /hint ---

--- hint ---

Aqui estão os blocos de código que você precisa:

```blocks3
repita até que <>
fim

mostre

<touching color [#0000ff]?>

adicione (-2) a y

quando eu começar como um clone
```

--- /hint ---

--- hint ---

É assim que seu código deve parecer:

```blocks3
quando eu começar como um clone
mostre
repita até que <touching color [#0000ff]?>
adicione (-2) a y
fim
```

--- /hint ------ /hints ---

--- /task ---

Ao clicar na bandeira verde, você verá um novo gato cair do topo do palco a cada três segundos. Todo gato deve pousar em uma grande pilha de gatos sobrepostos no chão azul na parte inferior.

![Gatos caindo](images/falling-cats.png)