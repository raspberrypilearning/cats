## Доберись до безопасного места

Цель игры состоит в том, чтобы направить котов в безопасное место, создав для них путь, чтобы они могли добраться до двери. Создай переменную для счёта, чтобы отслеживать, сколько котов достигает двери.

--- task ---

Создай новую переменную с именем `счёт`{:class="block3variables"}.

![Спрайт кота](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Добавь код к спрайту кота, чтобы увеличивать `счёт`{:class="block3variables"} на `1` каждый раз, когда кот достигает двери. Также установи `счёт`{:class="block3variables"} равным `0` `когда зелёный флаг нажат`{:class="block3events"} в начале игры.

![Спрайт кота](images/cat-sprite.png)

--- hints ---
 --- hint ---

`Если`{:class="block3control"} кот `касается спрайта двери`{:class="block3sensing"}, тогда `добавить 1 к счёту`{:class="block3variables"}.

--- /hint ---

--- hint ---

Вот новые блоки кода, которые нужно добавить в блок `когда я начинаю как клон`:

```blocks3
изменить [счёт v] на (1)

если <>, то
end

<touching (Дверь v)?>

задать [счёт v] значение (0)
```

--- /hint ---

--- hint ---

Вот как должен выглядеть твой код:

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
+   if <touching (Дверь v)?> then
        change [счёт v] by (1)
    end
end
delete this clone

когда щёлкнут по зелёному флагу
+задать [счёт v] значение (0)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Добавь ещё немного кода, чтобы, когда спрайт кота достигает двери, он издавала «мяу», а затем исчезал.

![Спрайт кота](images/cat-sprite.png)

```blocks3
включить звук (мяу v)
удалить клон
```

--- /task ---