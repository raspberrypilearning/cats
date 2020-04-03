## 선 따라가기

You might notice that, if you draw a low bridge between the two platforms, or a line that slopes upwards, the cats end up walking through the platform rather than on top of it!

![플랫폼을 통과해 걷는 고양이](images/cat-walk-through-platform.png)

\--- task \---

In the code for the cat sprite, add another loop before the `next costume`{:class="block3looks"} block. 이번에는 루프가 고양이에게 파란색에 닿지 않을 때까지 `2`만큼 위쪽으로 이동하라고 지시해야 합니다.

![고양이 스프라이트](images/cat-sprite.png)

\--- hints \--- \--- hint \---

The cat should `move up 2`{:class="block3motion"} `repeatedly until`{:class="block3control"} it is `not`{:class="block3operators"} `touching blue`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

필요한 코드 블록은 다음과 같습니다.

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

다음과 같은 코드를 추가해야 합니다:

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

초록색 깃발을 클릭하고 위쪽으로 기울어진 선을 그려보십시오. 고양이가 이 선을 따라가는지 확인하십시오.

\--- /task \---