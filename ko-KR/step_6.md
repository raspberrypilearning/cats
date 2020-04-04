## 안전 확보

이 게임의 목표는 고양이가 문에 도달 할 수 있도록 경로를 만들어 고양이를 안전하게 안내하는 것입니다. 문에 도달하는 고양이 수를 세는 점수 변수를 만듭니다.

--- task ---

먼저, `점수`{:class="block3variables"}라는 이름의 변수를 추가 해 보세요.

![고양이 스프라이트](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

고양이가 문에 닿을 때마다 `1`을 `점수`{:class="block3variables"}에 더하는 코드를 고양이 스프라이트에 추가합니다. 또 `점수`{:class="block3variables"}를 `깃발을 클릭했을 때`{:class="block3events"} `0`으로 바꾸게 합니다.

![고양이 스프라이트](images/cat-sprite.png)

--- hints ---
 --- hint ---

`만약`{:class="block3control"} 고양이가 `문에 닿았는가?`{:class="block3sensing"}라면 `점수에 1을 더한다`{:class="block3variables"}.

--- /hint ---

--- hint ---

이것은 `복제되었을 때` 스크립트에 추가할 코드 블럭들 입니다.

```blocks3
change [score v] by (1)

if <> then
end

<touching (문 v)?>

set [score v] to (0)
```

--- /hint ---

--- hint ---

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
+   if <touching (문 v)?> then
        change [score v] by (1)
    end
end
delete this clone

when flag clicked
+ set [score v] to (0)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

고양이 스프라이트가 문에 도달하면 고양이가 'meow'소리를 내고 사라지도록 코드를 더 추가하십시오.

![고양이 스프라이트](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

--- /task ---