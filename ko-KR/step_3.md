## 고양이 복제하기

You want a never-ending stream of cats that the player has to guide along the path to the exit.

\--- task \---

Click on the sprite called 'Cat', and add some code to `hide`{:class="block3looks"} the sprite, and also to `clone`{:class="block3control"} it every three seconds.

![고양이 스프라이트](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

지금 프로그램을 실행하면 스테이지에서 아무 일도 일어나지 않습니다. To check that a new Cat sprite clone is created every three seconds, make each clone appear and fall out of the sky.

\--- task \---

Add code to tell the sprite that `when it starts as a clone`{:class="block3control"}, it should `show`{:class="block3looks"} itself and fall until it `touches`{:class="block3sensing"} the blue floor that is drawn on the Stage.

![Cat sprite](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`When the sprite starts as a clone`{:class="block3control"}, `show`{:class="block3looks"} the sprite. `Repeatedly`{:class="block3control"} `Change`{:class="block3motion"} the sprite's `y` coordinate by `-2`, until the sprite `touches`{:class="block3sensing"} the blue Stage.

\--- /hint \---

\--- hint \---

필요한 코드 블록은 다음과 같습니다.

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

다음과 같은 코드를 추가해야 합니다:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

초록색 깃발을 클릭하면 3 초마다 새 고양이가 스테이지 상단에서 떨어집니다. 모든 고양이는 바닥에있는 파란색 바닥에 겹치는 고양이의 큰 더미에 착륙해야합니다.

![떨어지는 고양이](images/falling-cats.png)