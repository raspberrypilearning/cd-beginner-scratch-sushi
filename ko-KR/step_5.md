## 사물 이동

지금 상어가 원을 그리며 움직이는 것보다, 화살표 키로 상어를 제어하는 것이 훨씬 더 재미있을 것입니다. 이 과정에서 이렇게 하는 방법을 배우게됩니다!

--- task --- 상어에 대한 모든 코드를 삭제한 이후 시작하십시오. --- /task ---

짐작하셨듯이, **이벤트** 와 **동작** 카테고리에 있는 블록이 필요합니다!

--- task --- 이번에는 이 블록을 찾아서 현재 스크립트 영역으로 드래그하십시오.

```blocks3
    [스페이스 v] 키를 눌렀을 때
```

`스페이스` 옆 화살표 (▼) 를 클릭하세요. 선택할 수 있는 모든 키보드 키 목록이 표시됩니다. --- /task ---

방향키가 4개 있기 때문에 `키를 눌렀을 때`{:class="block3events"} 블록이 총 4개 필요합니다.

--- task --- 상어가 움직이게 하려면 이 블록들을 **동작** 블록에 아래와 같이 연결합니다:

```blocks3
    [왼쪽 화살표 v] 키를 눌렀을 때
    (-10) 만큼 움직이기
```

```blocks3
    [오른쪽 화살표 v] 키를 눌렀을 때
    (10) 만큼 움직이기
```

```blocks3
    [위쪽 화살표 v] 키를 눌렀을 때
```

```blocks3
    [아래쪽 화살표 v] 키를 눌렀을 때
```

--- /task ---

**참고**: `-10` 은 '10 만큼 뒤로 가는 것을 의미합니다'.

--- task --- 이제 녹색 깃발을 클릭하여 코드를 테스트하십시오. --- /task ---

이제 상어가 앞뒤로는 움직이지만 위나 아래로는 움직이지 않습니다. 또한 **동작** 카테고리의 블록을 살펴보면 '위' 또는 '아래' 로 이동하는 블록이 없다는 것을 알 수 있습니다. 그러나 이 문제는 **x** 와 **y** 좌표를 변경하는 것으로 쉽게 해결할 수 있습니다. — 도전해 봅시다!

--- task --- 2개의 `y 좌표를 만큼 바꾸기`{:class="block3motion"} 블록을 가져와, 아래와 같이 바꾸세요:

```blocks3
    [위쪽 화살표 v] 키를 눌렀을 때
+     y 좌표를 (10) 만큼 바꾸기
```

```blocks3
    [아래쪽 화살표 v] 키를 눌렀을 때
+     y 좌표를 (-10) 만큼 바꾸기
```

--- /task ---

이제 화살표 키를 누르면 상어가 무대 주위로 움직이는 것을 볼 수 있습니다!

--- collapse ---
---
title: x 및 y 좌표는 어떻게 동작합니까?
---

스프라이트와 같은 객체의 위치에 대해 이야기하기 위해 종종 x, y 좌표를 사용합니다. **x-축** 좌표는 무대에서 **왼쪽에서 오른쪽으로 이동**하는 것을 말하며, **y-축** 좌표는 **가운데에서 위로 향하는** 것을 말합니다.

![](images/moving3.png)

스프라이트는 다음과 같이 좌표로 위치가 지정됩니다, 예를 들어 `(15, -27)` 좌표에서 `15`는 x축 좌표를 의미하며, `-27` 은 y축 좌표를 의미합니다.

+ 이것이 실제로 어떻게 작동하는지 관찰하려면 스프라이트를 선택하고 **x** 그리고 **y** 좌표에 다른 값을 설정하여 스테이지 주위로 이동하도록 제어합니다.

![](images/xycoords.png)

+ 스프라이트의 위치를 확인하려면 다른 값으로 시도해 보세요! 스크래치에서, x축은 `-240` 부터 `240` 까지, y축은 `-180` 부터 `180` 까지 입니다.

--- /collapse ---

### 게임 다시 시작

상어는 이제 화면을 가로 질러 움직입니다. 그러나 이것이 게임이라고 상상해보십시오. 다시 시작할 때에는 어떻게 해야 하나요?

플레이어가 게임을 시작할 때 상어를 원래 위치로 배치해야 합니다. 플레이어는 녹색 깃발을 클릭하여 이 게임을 시작할 것이므로, 게임이 시작될 때 상어 스프라이트의 x와 y 좌표를 변경해야합니다.

실제로 매우 쉽습니다! 무대의 중심은 `(x, y)` 좌표에서 `(0, 0)`입니다.

여러분은 **이벤트** 카테고리에서 '깃발을 클릭했을 때' 블록을 찾고, **동작**카테고리에서 **이동하기** 블록을 배치하면 됩니다.

--- task --- `녹색 깃발을 클릭했을 때`{:class="block3events"} 블록을 **이벤트** 카테고리에서 찾아 스프라이트에 추가합니다.

```blocks3
    ⚑ 클릭했을 때
```

그런 다음 `이동하기`{:class="block3motion"} 블록을, **동작**카테고리 에서 찾아, **이벤트** 블록에 아래에 다음과 같이 추가합니다.

```blocks3
    ⚑ 클릭했을 때
+     x: (0) y: (0) \(으\)로 이동하기
```

`이동하기`{:class="block3motion"} 블록에서 `x` 와 `y` 좌표를 전부 `0` 으로 설정하세요.

--- /task ---

--- task --- 이제 녹색 깃발을 클릭하십시오: 상어가 무대 중앙으로 돌아 오는 것을 볼 수 있습니다! --- /task ---