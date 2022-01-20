## 선 그리기

--- task ---

스크래치 스타터 프로젝트 '고양이들!'를 여십시오.

**온라인:** [scratch.mit.edu/projects/382683246](https://scratch.mit.edu/projects/382683246){:target="_blank"}에서 새로운 스타터 프로젝트 열기.

스크래치 계정이 있는 경우 **Remix**을 클릭하여 사본을 만들 수 있습니다.

**오프라인:** 오프라인 편집기에서 [스타터 프로젝트](https://rpf.io/p/ko-KR/cats-go)를 엽니다. 스크래치 오프라인 에디터를 다운로드 받아야 하는 경우, [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}에서 다운 받을 수 있습니다.

--- /task ---

--- task ---

프로젝트에 펜 확장 프로그램을 추가합니다.

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

'펜'이라는 스프라이트를 클릭하고 코드를 추가하여 펜 색상을 스테이지의 장애물과 같은 파란색으로 설정합니다.

![펜 스프라이트](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

색상을 선택하려면 `펜 색깔을 ~로 정하기`{:class="block3extensions"} 블록에서 색깔 사각형을 클릭하여 마우스 커서를 스포이트로 만든 다음 스테이지에서 적절한 색상을 클릭하십시오.

--- /task ---

--- task ---

스프라이트가 마우스 포인터를 따라가도록 코드를 더 추가하십시오. 코드가 잘 작동하는지 확인하기 위해 프로그램을 테스트해 보십시오.

![펜 스프라이트](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

마우스 버튼을 눌렀을 때 스프라이트가 스테이지에 선을 그리도록 하는 코드를 추가하십시오.

![펜 스프라이트](images/pen-sprite.png)

--- hints ---
 --- hint ---

`만약`{:class="block3control"} `마우스를 클릭했는가`{:class="block3sensing"}라면 `펜 내리기`{:class="block3extensions"}, `아니면`{:class="block3control"}, `펜 올리기`{:class="block3extensions"} 를 수행합니다.

--- /hint ---

--- hint ---

필요할 코드 블록은 다음과 같습니다.

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

--- /hint ---

--- hint ---

코드는 다음과 같이 설계되어야 합니다:

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
forever
go to (mouse pointer v)
+ if <mouse down?> then
pen down
else
pen up
end
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

코드를 테스트 해 보십시오. 마우스로 드래그하여 스테이지에 파란색 선을 그릴 수 있어야합니다.

![선 그리기](images/draw-a-line.png)

--- /task ---

스테이지의 오른쪽 상단에 파란색 점이 항상 나타나는 것을 볼 수 있습니다 (위 이미지에서 동그라미 쳐져 있습니다). 녹색 깃발을 클릭하여 게임을 시작할 때 마우스를 누르면 펜이 바로 그리기 시작하기 때문입니다.

--- task ---

이 문제를 해결하기 위해서는 `펜 올리기`{:class="block3extensions"} 블록과 `1초 기다리기`{:class="block3control"} 블록을 `무한 반복하기`{:class="block3control"} 블록 위의 스크립트 시작 부분에 추가합니다.

![펜 스프라이트](images/pen-sprite.png)

```blocks3
when flag clicked
+ pen up
set pen color to [#0000ff]
erase all
set pen size to (5)
+ wait (1) seconds
forever
go to (mouse pointer v)
if <mouse down?> then
pen down
else
pen up
end
```

--- /task ---
