## 고양이 복제하기

당신은 출구로 안내해야 하는 끝없는 고양이들의 흐름을 원합니다.

--- task ---

'고양이'이라는 스프라이트를 클릭하고 스프라이트를 `숨기기`{:class="block3looks"}하고 스프라이트를 `복제하기`{:class="block3control"} 위해 코드를 추가합니다.

![고양이 스프라이트](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

--- /task ---

지금 프로그램을 실행하면 스테이지에서 아무 일도 일어나지 않습니다. 3 초마다 새로운 고양이 스프라이트 복사본이 생성되는지 확인하려면 각 고양이의 클론이 나타나고 하늘에서 떨어지도록 하십시오.

--- task ---

스프라이트가 `복제되었을 때`{:class="block3control"} 자기 자신을 `보이기`{:class="block3looks"} 하고, 파란색 바닥에 `~에 닿았는가`{:class="block3sensing"}까지 떨어지도록 코드를 추가합니다.

![고양이 스프라이트](images/cat-sprite.png)

--- hints ---
 --- hint ---

`복제되었을 때`{:class="block3control"} 스프라이트를 `보이기`{:class="block3looks"} 하십시오. 스프라이트의 `y` 좌표를 `-2` `만큼 바꾸기 `{:class="block3motion"} 를 스프라이트가 파란색 스테이지에`~에 닿았는가`{:class="block3sensing"}`까지 반복하기`{:class="block3control"} 하세요.

--- /hint ---

--- hint ---

필요한 코드 블록은 다음과 같습니다.

```blocks3
repeat until <>
end

show

<touching color [#0000ff]?>

change y by (-2)

when I start as a clone
```

--- /hint ---

--- hint ---

다음과 같은 코드를 추가해야 합니다:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

--- /hint ------ /hints ---

--- /task ---

초록색 깃발을 클릭하면 3 초마다 새 고양이가 스테이지 상단에서 떨어집니다. 모든 고양이는 바닥에있는 파란색 바닥에 겹치는 고양이의 큰 더미에 착륙해야합니다.

![떨어지는 고양이](images/falling-cats.png)