## ネコのクローンを作る

ゲームには、プレイヤーが出口までの道にそってあんないする、つぎつぎと出てくるネコが必要です。

\--- task \---

「ネコ」というスプライトをクリックします。`隠す`{:class="block3looks"} (かくす) ブロックをスプライトに追加し、さらに3秒ごとにスプライトの`クローンを作る`{:class="block3looks"}。

![ネコのスプライト](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

ここでプログラムを実行しても、ステージでは何も起こりません。 3秒ごとに新しいネコのスプライトのクローンが作られているのをたしかめるには、クローンをそれぞれ表示 (ひょうじ) して空から落ちるようにします。

\--- task \---

スプライトが`クローンされたとき`{:class="block3control"}、 `表示`{:class="block3looks"}します。スプライトがステージにかかれた青いゆかに`触れる`{:class="block3sensing"} (ふれる) まで落ちるようにコードを入れます。

![ネコのスプライト](images/cat-sprite.png)

\--- hints \--- \--- hint \---

スプライトが`クローンされたとき`{:class="block3control"}、 `表示`{:class="block3looks"}します。 ステージの青い部分に`触れる`{:class="block3sensing"}まで、スプライトの`y`座標 (ざひょう) を`-2`ずつ`繰り返し`{:class="block3control"} (くりかえし) `変え`{:class="block3motion"} (かえ) ます。

\--- /hint \---

\--- hint \---

必要なコードブロックは次のとおりです。

```blocks3
repeat until <>
end

show

<touching color [#0000ff]?>

change y by (-2)

when I start as a clone
```

\--- /hint \---

\--- hint \---

コードは次のようになります。

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

緑の旗をクリックすると、3秒ごとに新しいネコがステージの上部から落ちてきます。 Every cat should land in a big pile of overlapping cats on the blue floor at the bottom.

![落ちるネコ](images/falling-cats.png)