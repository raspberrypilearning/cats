## Clonar gatos

Você quer um fluxo interminável de gatos que o jogador precisa orientar ao longo do caminho até a saída.

--- task ---

Clique no sprite chamado 'Cat' e adicione algum código ao `esconde-te`{:class="block3looks"} do sprite, e também ao `clone`{:class="block3control"} a cada três segundos.

![Sprite de gato](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

--- /task ---

Se você executar o programa agora, nada acontece no palco. Para verificar se um novo clone de sprite Cat é criado a cada três segundos, faça com que cada clone apareça e caia do céu.

--- task ---

Adicione código para dizer ao sprite que `quando ele começa como um clone`{:class="block3control"}, deve- `show de`{:class="block3looks"}-se e cair até que ele `toques`{:class="block3sensing"} o piso azul desenhado no palco.

![Sprite de gato](images/cat-sprite.png)

--- hints ---
 --- hint ---

`Quando o sprite começa como um clone`{:class="block3control"}, `mostra`{:class="block3looks"} o sprite. `Repetidamente`{:class="block3control"} `Altere`{:class="block3motion"} as coordenadas `e` do sprite por `-2`, até o sprite `tocar`{:class="block3sensing"} no azul Palco.

--- /hint ---

--- hint ---

Estes são os blocos de que necessitas:

```blocks3
repeat until <>
end

show

<touching color [#0000ff]?>

change y by (-2)

when I start as a clone
```

--- /hint ---

--- hint ---

Este é o aspeto que o teu código deve ter:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

--- /hint ------ /hints ---

--- /task ---

Ao clicar na bandeira verde, você verá um novo gato cair do topo do palco a cada três segundos. Todo gato deve pousar em uma grande pilha de gatos sobrepostos no chão azul na parte inferior.

![Gatos caindo](images/falling-cats.png)