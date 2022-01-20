## Desenhar linhas

--- task ---

Abre o 'GATOS!' Projeto Scratch inicial.

**Online:** abre o projeto inicial em [scratch.mit.edu/projects/382446321](https://scratch.mit.edu/projects/382446321){:target="_blank"}.

Se tiveres uma 'conta Scratch' podes fazer uma cópia ao clicares **Remisturar**.

**Off-line:** abre o [projeto inicial](https://rpf.io/p/pt-PT/cats-go) no editor off-line. Se necessitares de descarregar e instalar o editor offline do Scratch, podes encontrá-lo em [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

Adiciona a extensão "caneta" ao teu projeto.

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

Clica no ator chamado 'Lápis' e adiciona-lhe código para definir a cor do lápis para o mesmo azul dos obstáculos no palco.

![Caneta sprite](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

Para selecionar uma cor, clica no quadrado de cores no bloco `set pen color`{:class="block3extensions"} para transformar o cursor do rato numa pipeta e clica na cor correta no palco.

--- /task ---

--- task ---

Adiciona um pouco mais de código para obrigar o ator a seguir o ponteiro do rato. Testa o teu programa para verificar se o código está a funcionar.

![Caneta sprite](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

Adiciona mais algum código para que o ator desenhe uma linha no palco quando o botão do rato for pressionado.

![Caneta sprite](images/pen-sprite.png)

--- hints ---
 --- hint ---

`Se`{:class="block3control"} o mouse `estiver pressionado`{:class="block3sensing"}, coloque a caneta `pressionada`{:class="block3extensions"} e mais `outras`{:class="block3control"}, levante a caneta `cima`{:class="block3extensions"}.

--- /hint ---

--- hint ---

Estes são os blocos de que necessitas:

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

--- /hint ---

--- hint ---

Este é o aspeto que o teu código deve ter:

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
forever
go to (mouse pointer v)
+ if <mouse down?> then
pen down
else
pen up
end
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

Testa o teu código. Você poderá clicar e arrastar com o mouse para desenhar uma linha azul no palco.

![Desenhe uma linha](images/draw-a-line.png)

--- /task ---

Você provavelmente vê que um ponto azul sempre aparece no canto superior direito do palco (está circulado na imagem acima). Isso ocorre porque, quando você clica na bandeira verde para iniciar o jogo, pressiona o mouse e a caneta começa a desenhar imediatamente.

--- task ---

Para impedir que isso aconteça, adicione um bloco `caneta`{:class="block3extensions"} no início do script e `espere um segundo`{:class="block3control"} acima dos `para sempre`{:class="block3control"} bloco.

![Caneta sprite](images/pen-sprite.png)

```blocks3
when flag clicked
+ pen up
set pen color to [#0000ff]
erase all
set pen size to (5)
+ wait (1) seconds
forever
go to (mouse pointer v)
if <mouse down?> then
pen down
else
pen up
end
```

--- /task ---
