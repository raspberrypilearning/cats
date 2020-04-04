## ネコを動かす

ネコがゆかに着くと、ゆっくりと右に歩きます。

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

ネコがステージの右がわにたどり着けるようにあなの上に橋をかくと、ネコは右のかべで行きづまってしまいます。

![はしで行きづまっているネコ](images/flailing-at-edge.png)

\--- task \---

`ずっと`{:class="block3control"}ループを削除 (さくじょ) し、代わりにちがうループを入れて、ネコが端 (はし) に着くまで歩くようにします。 ネコがステージの端に着くと、ネコは消えます。

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

緑の旗をおして、ネコがステージの端に着いたときに消えることをたしかめます。

\--- /task \---

ネコがあなに落ちた場合、消えるのではなくあなのそこで動けなくなることに気づいたと思います。 これは、ネコが下に落ちつづけようとしているためです。

このコードが、ネコに青に触れるまで落ちつづけるようにめいれいしています。

```blocks3
repeat until <touching color [#0000ff]?>
end
```

しかし、あなの中ではネコは青に触れることはないので、行きづまったままです。

\--- task \---

このループにさらにブロックを入れて、ネコのスプライトが青に触れるか、`または`{:class="block3operators"}`端に触れる`{:class="block3sensing"}まで繰り返すようにします。 こうすることで、スプライトがステージの端に着くと、スプライトは落ちるのをやめます。

![ネコのスプライト](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---