## 코드 블록 추가 및 제거

잘하셨어요! 첫 번째 스크래치 프로그램을 작성하셨습니다. 이번에는 스크래치 블록들에 대해 조금 더 배워보도록 하겠습니다. 스크래치 코드는 다음과 같이 **블록** 로 구성됩니다.

![](images/code1.png)

**코드 블록 팔레트** 에있는 모든 블록은, 해당 블록이 하는 일에 따라 다른 카테고리로 정렬됩니다.

## \--- collapse \---

## 제목: 다른 카테고리의 블록 사용

해당 카테고리의 블록을 보려면 카테고리 이름을 클릭하세요. 여기에서는 **동작** 카테고리가 선택됩니다.

![](images/code2a.png)

클릭 한 카테고리의 모든 블록이 목록에 표시됩니다.

![](images/code2b.png)

원하는 블록을 클릭 한 다음 현재 스크립트 영역으로 드래그하여 놓으십시오. 일단 블록이 스크립트 영역에 있으면, 당신은 블록을 옮기고 그것을 다른 블록에 연결할 수 있습니다.

-- /collapse \---

블록이 무엇을하는지 보려면 블록을 두 번 클릭하여 실행할 수 있습니다.

\--- task \---

Try double-clicking on some of the blocks to see what they do.

\--- /task \---

## \--- collapse \---

## title : 코드 실행

Usually, you want your code to run automatically whenever something specific happens. This is why many of your programs will start with a block from the **Events** category, most often this one:

```blocks3
    녹색 깃발이 클릭되었을 때
```

The code blocks connected to this block will run after the **green flag** is clicked.

Code blocks run from top to bottom, so the order in which you snap your blocks together matters. In this example, the sprite will `say`{:class="block3looks"} `Hello!` before it will `play`{:class="block3sound"} the `meow` sound.

```blocks3
    녹색 깃발이 클릭되었을 때
    [안녕!] 말하기
    [야옹 v] 재생하기
```

\--- /collapse \---

Removing or deleting code blocks you don’t want in your program is easy! Just drag them back into the code blocks palette.

**Be careful:** dragging them into the code blocks pallette will delete all the blocks connected to the block you drag, so make sure to separate code blocks you want to keep from those you want to remove. If you delete some code blocks by accident and want to get them back, right-click and then click on the **undo** option to get everything back.

![](images/code6.png)

\--- task \---

Try adding, deleting, and undeleting some code blocks!

\--- /task \---

### 모두 합쳐서 코드 만들기

Now you know how to move code around and make things happen, it's time for you to create a program to make the Scratch Cat walk in a circle!

\--- task \---

Make sure you have the cat sprite selected in the sprite list, and then drag the following blocks into the sprite panel and connect them. You’ll find them in the **Events** and **Motion** lists.

```blocks3
    녹색 깃발이 클릭되었을 때
    [10] 만큼 움직이기
```

\--- /task \---

\--- task \---

Now, click on the green flag above the Stage.

![](images/code7.png)

\--- /task \---

You should see the cat walking in a straight line...not exactly what you want, right?

Note: If you click th flag too many times and the cat walks away, you can drag it back!

\--- task \---

Snap the turn block to the end to make the cat sprite walk in a circle. It’s in the **Motion** list too.

```blocks3
    녹색 깃발이 클릭되었을 때
    [10] 만큼 움직이기
+    cw 방향으로 (15) 도 회전하기
```

\--- /task \---

## \--- collapse \---

## 제목 : 회전은 어떻게 작동합니까?

This block makes the sprite turn 15 degrees of the full 360 degrees that make up a circle. You can change that number, and the number of steps, by clicking on the number and typing in a new value.

![](images/code9.png)

\--- /collapse \---

\--- task \---

Now save your work!

\--- /task \---