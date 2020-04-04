## 선 따라가기

두 플랫폼 사이에 낮은 다리나 위로 경사져 있는 선을 그리면 고양이들은 선 위에 올라가기 보다는 플랫폼을 통과해 걷게 된다는 것을 볼 수도 있을 것입니다!

![플랫폼을 통과해 걷는 고양이](images/cat-walk-through-platform.png)

--- task ---

고양이 스프라이트의 코드에 `다음 모양으로 바꾸기`{:class="block3looks"} 블록 앞에 루프를 하나 추가합니다. 이번에는 루프가 고양이에게 파란색에 닿지 않을 때까지 `2`만큼 위쪽으로 이동하라고 지시해야 합니다.

![고양이 스프라이트](images/cat-sprite.png)

--- hints ---
 --- hint ---

고양이 스프라이트는 `파란색에 닿았는가`{:class="block3sensing"} `가 아니다`{:class="block3operators"} 일때까지 `y 좌표를 2만큼 바꾸기`{:class="block3motion"}를 `반복합니다`{:class="block3control"}.

--- /hint ---

--- hint ---

필요한 코드 블록은 다음과 같습니다.

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
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
end
delete this clone
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

초록색 깃발을 클릭하고 위쪽으로 기울어진 선을 그려보십시오. 고양이가 이 선을 따라가는지 확인하십시오.

--- /task ---