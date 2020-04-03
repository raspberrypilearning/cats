## 線にそわせる

2つの足場の間に低い橋または上向きの線をかくと、足場の上ではなく中を歩いてしまうことに気づいたと思います。

![足場の中を歩くネコ](images/cat-walk-through-platform.png)

\--- task \---

ネコのスプライトのコードの`次のコスチュームにする`{:class="block3looks"}ブロックの前に別のループを追加します。 今度は、ループで猫が青色に触れなくなるまで`2`ずつ上がるようにしなければなりません。

![ネコのスプライト](images/cat-sprite.png)

\--- hints \--- \--- hint \---

The cat should `move up 2`{:class="block3motion"} `repeatedly until`{:class="block3control"} it is `not`{:class="block3operators"} `touching blue`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Here are the code blocks you need:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

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

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Click the green flag and try drawing a line that slopes upwards. Check that your cat follows this line.

\--- /task \---