## 스스로 움직이는 물고기

이제 물고기를 스스로 수영하게 만들 시간입니다. 이렇게 하려면 새로운 종류의 **제어** 블록이 필요합니다.

\--- task \---

Select your fish sprite.

Drag a `when green flag clicked`{:class="block3events"} **Event** block, a `forever`{:class="block3control"} **Control** block, and a `move 10 steps`{:class="block3motion"} **Motion** block into the **sprite panel**, like this:

```blocks3
    녹색 깃발을 클릭했을 때
    무한 반복
        (10) 만큼 움직이기
    끝
```

\--- /task \---

## \--- collapse \---

## title: 새로운 블록은 무엇을 하는 블록인가요?

**Control** blocks make your program do things a certain number of times, or under certain conditions.

Here, the fish does whatever is inside the `forever`{:class="block3control"} block over and over again on a loop, forever. So once it has done the last thing (block) inside the `forever`{:class="block3control"} block, it starts over at the top and does everything again, and so on.

\--- /collapse \---

\--- task \---

Now click the green flag and watch what happens!

\--- /task \---

Well, that fish just crashed into the side of the Stage, and it was moving far too fast for your shark to catch.

First, you need to slow the fish down. That’s actually pretty easy, you just need it to wait for a little while after it moves those 10 steps. There’s a **Control** block that will help you here:

```blocks3
    (1) 초 기다리기
```

\--- task \---

Add the `wait`{:class="block3control"} block into your code inside the `forever`{:class="block3control"} block, and change the number to `0.5`, like this:

```blocks3
    녹색 깃발을 클릭했을 때
    무한 반복
        (10) 만큼 움직이기
+      (0.5) 초 기다리기
    끝
```

\--- /task \---

## \--- collapse \---

## 제목: 기다리기 초 조정

The number you set in the `wait`{:class="block3control"} block says how many **seconds** you want the fish to wait. `0.5` is half a second.

You can test out different values to see which is the best for the game. And remember that you can change the number of steps inside the `move`{:class="block3motion"} block too!

\--- /collapse \---

The fish moves now, but you need it to bounce off the edge of the Stage too. Yet again, there’s a **Motion** block for this!

\--- task \---

Find the `if on edge bounce`{:class="block3motion"} block, and add it in after the `wait`{:class="block3control"} block.

\--- /task \---

## \--- collapse \---

## title: 새로운 코드는 무엇을 합니까?

The `if on edge bounce`{:class="block3motion"} block checks if the sprite is touching the edge of the Stage and, if it is, it turns left, right, up, or down as appropriate.

\--- /collapse \---

Of course, this will lead to an upside-down fish, so you need a `set rotation style`{:class="block3motion"} block again.

\--- task \---

Update your code to set the rotation style of the fish to `left-right`{:class="block3motion"} at the beginning of the sprite's script:

```blocks3
    녹색 깃발을 클릭했을 때
+    회전 방식을 [왼쪽-오른쪽 v] 으로 정하기
    무한 반복
        (10) 만큼 움직이기
        (0.5) 초 기다리기
        벽에 닿으면 튕기기
    끝
```

\--- /task \---

The fish moves backwards and forwards now, but only in a straight line — a bit too easy for the player to catch with the shark! You need to make the fish less predictable.

You already know from a previous step how to make a sprite turn, so start there.

\--- task \---

Add a turn into the fish's swimming instructions, and click the green flag.

```blocks3
    녹색 깃발을 클릭했을 때
    회전 방식을 [왼쪽-오른쪽 v] 으로 정하기
    무한 반복
        (10) 만큼 움직이기
+        cw 방향으로 (10) 도 회전하기
        (0.5) 초 기다리기
        벽에 닿으면 튕기기
    끝
```

\--- /task \---

It’s better, but there’s still too much of a pattern. It needs to be more random. Luckily, Scratch can do random for you! You’ll just need a new kind of block, called an **operator** block.

## \--- collapse \---

## 제목: 연산자란 무엇입니까?

**Operators** take in one or more values (like numbers, text, or `True/False` values) and give back a single value. You can tell the kind of value it will give back by the shape of the block: round ends give numbers or text, pointy ends give `True/False`.

```blocks3
    (() + ())

    ([헬로우 ] 와 [월드] 결합하기)

    <[] = []>
```

\--- /collapse \---

\--- task \---

Find the `pick random`{:class="block3operators"} **operator** block, and plug it into the `turn degrees`{:class="block3motion"} **Motion** block by clicking it and dragging it into the field where you set the number of degrees.

```blocks3
    녹색 깃발을 클릭했을 때
    회전 방식을 [왼쪽-오른쪽 v] 으로 정하기
    무한 반복
        (10) 만큼 움직이기
+        cw 방향으로 ((1) 부터 (10) 까지의 난수) 도 회전하기
        (0.5) 초 기다리기
        벽에 닿으면 튕기기
    끝
```

\--- /task \---

**Note**: you can change the minimum and maximum numbers it will pick, but the default values (`1` and `10`) are pretty good for this game, so you can just leave them.

\--- task \---

Click the green flag to run the code!

\--- /task \---

## \--- collapse \---

## 제목: 자 이제 무한 반복 블록은 무엇을 합니까?

The forever block now makes the fish sprite do four things in order:

1. 앞으로 이동
2. 방향 조금 돌리기
3. 잠깐 기다리기
4. 벽에 닿으면 튕기기

Once the sprite has done the check, it will start at the beginning of the loop again and move, turn, wait, check, for as long as you let your Scratch program run.

\--- /collapse \---

Cool! Next up: catching that fish!