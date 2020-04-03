## 고양이가 움직이도록 만들기

고양이가 바닥에 닿으면 천천히 오른쪽으로 움직여야 합니다.

\--- task \---

Add code to the `when I start as a clone`{:class="block3control"} section to make the cat sprite `move ten steps`{:class="block3motion"}, and switch between the sprite's two costumes every 0.1 seconds to make the cat look like it's walking.

![고양이 스프라이트](images/cat-sprite.png)

\--- hints \--- \--- hint \---

The cat sprite should `move 10 steps`{:class="block3motion"}, and `switch costume`{:class="block3looks"} every `0.1 seconds`{:class="block3control"}. This code should repeat `forever`{:class="block3control"}, just like the code to make the cat fall.

\--- /hint \---

\--- hint \---

필요한 코드 블록은 다음과 같습니다.

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

\--- /hint \---

\--- hint \---

다음과 같은 코드를 추가해야 합니다:

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

Press the green flag and check that the cats now move along the blue platform at the bottom.

\--- /task \---

고양이가 스테이지의 오른쪽까지 갈 수 있도록 간격 사이에 다리를 그리면 고양이가 오른쪽 벽에서 더이상 걷지 못하는 것을 볼 수 있습니다.

![가장자리에 버벅이는 고양이](images/flailing-at-edge.png)

\--- task \---

Remove the `forever`{:class="block3control"} loop, and instead add a different loop to make the cats only walk until they reach an edge. When a cat reaches the edge of the Stage, it should disappear.

![고양이 스프라이트](images/cat-sprite.png)

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

고양이가 구멍에 빠지면 사라지지 않고 대신 바닥에 붙어있는 것을 알 수 있습니다. This is because they keep trying to fall downwards.

This is the part of the code that tells the cat to keep falling until it touches blue:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

However, in the hole, the cat can never reach blue, so it is stuck forever.

\--- task \---

Add more blocks to this loop so that it repeats until the cat sprite is touching blue `or`{:class="block3operators"} `touching the edge`{:class="block3sensing"}. This way, the sprite stops trying to fall if it reaches the edge of the Stage.

![고양이 스프라이트](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

\--- /task \---