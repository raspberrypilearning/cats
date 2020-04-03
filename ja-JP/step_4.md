## ネコを動かす

ネコが床に着くと、ゆっくりと右に歩きます。

\--- task \---

`クローンされたとき`{:class="block3control"}のセクションに、ネコのスプライトを`10歩動かし`{:class="block3motion"}、0.1秒ごとに2つのコスチュームを切りかえるようにコードを入れます。

![ネコのスプライト](images/cat-sprite.png)

\--- hints \--- \--- hint \---

ネコは`10歩動き`{:class="block3motion"}、`0.1秒`{:class="block3control"}ごとに`コスチュームを切りかえます`{:class="block3looks"}。 このコードは、ネコを落とすコードと同じように、 `ずっと`{:class="block3control"}くり返す必要があります。

\--- /hint \---

\--- hint \---

必要なコードブロックは次のとおりです。

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

\--- /hint \---

\--- hint \---

コードは次のようになります。

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

緑の旗をおして、ネコが青いゆかにそって動くことをたしかめます。

\--- /task \---

ネコがステージの右がわにちゃんとたどり着けるようにあなの上に橋をかくと、ネコが右のかべで行きづまってしまいます。

![端で行き詰っているネコ](images/flailing-at-edge.png)

\--- task \---

`ずっと`{:class="block3control"}ループを削除 (さくじょ) し、代わりにちがうループを入れて、ネコがはしに着くまで歩くようにします。 When a cat reaches the edge of the Stage, it should disappear.

![ネコのスプライト](images/cat-sprite.png)

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

![ネコのスプライト](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---