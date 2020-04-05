## 線にそわせる

2つの足場の間に低い橋または上向きの線をかくと、足場の上ではなく中を歩いてしまうことに気づいたと思います。

![足場の中を歩くネコ](images/cat-walk-through-platform.png)

--- task ---

ネコのスプライトのコードの`次のコスチュームにする`{:class="block3looks"}ブロックの前に別のループを追加します。 今度は、ループでネコが青色に触れなくなるまで`2`ずつ上がるようにしなければなりません。

![ネコのスプライト](images/cat-sprite.png)

--- hints ---
 --- hint ---

`青色に触れた`{:class="block3sensing"}じょうたい`ではなく`{:class="block3operators"}なるまで、ネコは`2つ上に動く`{:class="block3motion"}のを`繰り返す`{:class="block3control"}必要があります。

--- /hint ---

--- hint ---

必要なコードブロックは次のとおりです。

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

--- /hint ---

--- hint ---

コードは次のようになります。

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

--- /hint ---

--- /hints --- --- /task ---

--- task ---

緑の旗をクリックして、上向きの線をかいてみましょう。 ネコがこの線にそっていくことをたしかめましょう。

--- /task ---