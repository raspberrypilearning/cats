## 안전 확보

이 게임의 목표는 고양이가 문에 도달 할 수 있도록 경로를 만들어 고양이를 안전하게 안내하는 것입니다. 문에 도달하는 고양이 수를 세는 점수 변수를 만듭니다.

\--- task \---

Create a variable called `score`{:class="block3variables"}.

![고양이 스프라이트](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Add code to your cat sprite to add `1` to the `score`{:class="block3variables"} each time a cat reaches the door. Also set `score`{:class="block3variables"} to `0` `when the flag is clicked`{:class="block3events"} at the start of the game.

![고양이 스프라이트](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`If`{:class="block3control"} the cat is `touching the door sprite`{:class="block3sensing"}, then `add 1 to the score`{:class="block3variables"}.

\--- /hint \---

\--- hint \---

Here are the new code blocks you need to add to your `when I start as a clone` script:

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
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
+   if <touching (Door v)?> then
        change [score v] by (1)
    end
end
delete this clone

when flag clicked

+ set [score v] to (0)
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

고양이 스프라이트가 문에 도달하면 고양이가 'meow'소리를 내고 사라지도록 코드를 더 추가하십시오.

![고양이 스프라이트](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

\--- /task \---