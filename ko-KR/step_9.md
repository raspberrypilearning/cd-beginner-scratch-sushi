## 점수 사용하기

플레이어가 잡은 물고기의 수를 점수로 저장하고, 게임을 다시 시작할 때 초기화되는 방법을 알아보도록 하겠습니다.

첫번째: 점수 저장!

\--- task \---

Go to the **Variables** blocks category and click on **Make a Variable**.

![](images/catch5.png)

Enter `score` as the name.

![](images/catch6.png)

Check out your new variable!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)

\--- /task \---

## \--- collapse \---

## title: 변수란 무엇인가요?

When you want to store information in a program, you use something called a **variable**. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. You’ll find variables in the **Variables** section, but you need to create them first for them to show up there!

\--- /collapse \---

Now you need to update the variable whenever the shark eats a fish, and to reset it when the game is restarted. Doing both is pretty easy:

\--- task \---

From the **Variables** section, take the `set [my variable v] to [0]`{:class="block3variables"} and `change [my variable v] by [1]`{:class="block3variables"} blocks. Click on the little arrows in the blocks, choose `score` from the list, and then put the blocks into your program:

### 상어에 대한 코드

```blocks3
    녹색 깃발을 클릭했을 때
+    [score v] 를 [0] 로 정하기
    회전 방식을 [왼쪽-오른쪽 v] 으로 정하기
    x: (0) y: (0) 으로 이동하기
```

### 물고기에 대한 코드

```blocks3
    만약 <touching [Sprite1 v] ?> 이라면
+        [score v] 를 [1] 만큼 바꾸기
        숨기기
        (1) 초 기다리기
        x: ((-240) 부터 (240) 사이의 난수) y: ((-180) 부터 (180) 사이의 난수) 로 이동하기
        보이기
    끝
```

\--- /task \---

Cool! Now you’ve got a score and everything.