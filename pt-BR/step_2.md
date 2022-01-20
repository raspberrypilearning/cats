## Desenhar linhas

--- task ---

Abra o projeto inicial Scratch 'GATOS!'.

**Online:** Abra o projeto inicial em [scratch.mit.edu/projects/382879413](https://scratch.mit.edu/projects/382879413){:target="_blank"}.

Se você tiver uma conta Scratch, você pode fazer uma cópia clicando em **Remix**.

**Offline:** Abra o [projeto inicial](https://rpf.io/p/pt-BR/cats-go) no editor offline. Se você precisar baixar e instalar o editor offline do Scratch, você pode encontrá-lo em [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

Adicione a extensão Caneta ao seu projeto.

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

Clique no ator chamado 'Caneta' e adicione um código para definir a cor da caneta para o mesmo azul dos obstáculos no palco.

![ator Caneta](images/pen-sprite.png)

```blocks3
when flag clicked
mude a cor da caneta para [#0000ff]
apague tudo
adicione (5) ao tamanho da caneta
```

Para selecionar uma cor, clique no quadrado de cores no bloco `mude a cor da caneta para`{:class="block3extensions"} para transformar o cursor do mouse em uma pipeta e clique na cor correta no palco.

--- /task ---

--- task ---

Adicione um pouco mais de código para fazer o ator seguir o ponteiro do mouse. Teste seu programa para verificar se o código funciona.

![ator Caneta](images/pen-sprite.png)

```blocks3
sempre
vá para (ponteiro do mouse v)
fim
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

Adicione algum código para dizer ao ator para desenhar uma linha no palco se o botão do mouse for pressionado.

![ator Caneta](images/pen-sprite.png)

--- hints ---
 --- hint ---

`Se`{:class="block3control"} o `mouse está pressionado`{:class="block3sensing"}, `use a caneta`{:class="block3extensions"}, e `senão`{:class="block3control"}, `levante a caneta`{:class="block3extensions "}.

--- /hint ---

--- hint ---

Aqui estão os blocos de código que você precisa:

```blocks3
<mouse down?>

use a caneta

levante a caneta

se <> então
senão
fim
```

--- /hint ---

--- hint ---

É assim que seu código deve parecer:

```blocks3
when flag clicked
mude a cor da caneta para [#0000ff]
apague tudo
adicione (5) ao tamanho da caneta
sempre
vá para (ponteiro do mouse v)
+ se <mouse down?> então
use a caneta
senão
levante a caneta
fim
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Teste seu código. Você poderá clicar e arrastar com o mouse para desenhar uma linha azul no palco.

![Desenhe uma linha](images/draw-a-line.png)

--- /task ---

Você provavelmente vê que um ponto azul sempre aparece no canto superior direito do palco (está circulado na imagem acima). Isso ocorre porque, quando você clica na bandeira verde para iniciar o jogo, pressiona o mouse e a caneta começa a desenhar imediatamente.

--- task ---

Para impedir que isso aconteça, adicione um bloco `levante a caneta`{:class="block3extensions"} no início do script e um bloco `espere um segundo`{:class="block3control"} acima do bloco `sempre`{:class="block3control"}.

![ator Caneta](images/pen-sprite.png)

```blocks3
when flag clicked
+ levante a caneta
mude a cor da caneta para [#0000ff]
apague tudo
adicione (5) ao tamanho da caneta
+ espere(1) seg
sempre
vá para (ponteiro do mouse v)
se <mouse down?> então
use a caneta
senão
levante a caneta
fim
```

--- /task ---
