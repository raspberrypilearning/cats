## 고양이가 움직이도록 만들기

고양이가 바닥에 닿으면 천천히 오른쪽으로 움직여야 합니다.

--- task ---

코드의 `복제되었을때`{:class="block3control"} 부분에 고양이 스프라이트가 0.1초 마다 `10만큼 움직이기`{:class="block3motion"}와 다음 모양으로 바꾸기를 하여 걸어가는 것처럼 보이도록 코드를 추가합니다.

![고양이 스프라이트](images/cat-sprite.png)

--- hints ---
 --- hint ---

고양이 스프라이트는 `0.1초`{:class="block3control"} 마다 `10만큼 움직이기`{:class="block3motion"}하고 `다음 모양으로 바꾸기`{:class="block3looks"}를 해야 합니다. 이 코드는 고양이를 떨어트리는 코드와 마찬가지로 `무한 반복하기`{:class="block3control"} 해야 합니다.

--- /hint ---

--- hint ---

필요한 코드 블록은 다음과 같습니다.

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

--- /hint ---

--- hint ---

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

--- /hint ---

--- /hints --- --- /task ---

--- task ---

녹색 깃발을 누르고 고양이가 바닥의 파란색 플랫폼을 따라 움직이는지 확인하십시오.

--- /task ---

고양이가 스테이지의 오른쪽까지 갈 수 있도록 간격 사이에 다리를 그리면 고양이가 오른쪽 벽에서 더이상 걷지 못하는 것을 볼 수 있습니다.

![가장자리에 버벅이는 고양이](images/flailing-at-edge.png)

--- task ---

`무한 반복하기`{:class="block3control"} 루프를 제거하고 대신 다른 루프를 추가하여 고양이가 가장자리에 도달할 때까지만 걸어가도록 합니다. 고양이가 스테이지 가장자리에 도달하면 사라져야 합니다.

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

--- /task ---

--- task ---

녹색 깃발을 누르고 고양이가 스테이지 가장자리에 닿으면 사라지는지 확인하십시오.

--- /task ---

고양이가 구멍에 빠지면 사라지지 않고 대신 바닥에 붙어있는 것을 알 수 있습니다. 이는 고양이가 계속 아래로 떨어지려고 하기 때문입니다.

이것은 고양이가 파란색에 닿을 때까지 계속 떨어지도록 지시하는 코드의 일부입니다.

```blocks3
repeat until <touching color [#0000ff]?>
end
```

그러나 구멍에서 고양이는 결코 파란색에 도달 할 수 없으므로 영원히 붙어 있습니다.

--- task ---

고양이 스프라이트가 파란색 `또는`{:class="block3operators"} `벽에 닿았는가`{:class="block3sensing"}까지 반복되도록 이 루프에 블록을 더 추가하십시오. 이렇게 하면 스프라이트가 벽에 도달하면 떨어지려고 하지 않습니다.

![고양이 스프라이트](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

--- /task ---