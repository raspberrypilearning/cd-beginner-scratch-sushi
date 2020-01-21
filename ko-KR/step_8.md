## 물고기 잡기

상어가 움직이고 물고기는 수영하지만 둘이 서로 상호 작용하지 않습니다. 물고기가 상어의 입으로 바로 수영해도 아무 일도 일어나지 않습니다. 그것을 바꿀 시간입니다!

먼저 물고기가 상어에 닿았는지 알아야합니다. 이를 제작하기 위해서는 **제어** 블록 및 **감지** 블록이 필요합니다.

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Drag the `touching...`{:class="block3sensing"} block into the space at the top of the `if...then`{:class="block3control"} block, and click the little triangle to select the shark sprite's name. If you haven’t changed it, it'll be 'Sprite1'.

```blocks3
    녹색 깃발을 클릭했을 때
    회전 방식을 [왼쪽-오른쪽 v] 으로 정하기
    무한 반복
        (10) 만큼 움직이기
        cw 방향으로 ((1) 부터 (10) 까지의 난수) 도 회전하기
        (0.5) 초 기다리기
        벽에 닿으면 튕기기
+        만약 <touching [Sprite1 v] ?> 이라면
    끝
```

\--- /task \---

## \--- collapse \---

## title: 어떻게 동작하나요?

The `if...then`{:class="block3control"} **Control** block needs to be given a `True/False` value.

**Sensing** blocks collect information, like where the sprite is, what it’s touching, etc. You're using this block:

```blocks3
    <touching [Sprite1 v] ?>
```

From this block's pointy ends, you can tell it’s going to give you the `True/False` value that the `if...then`{:class="block3control"} block needs.

\--- /collapse \---

Of course, you’ve just added an `if...then`{:class="block3control"} block without adding anything for the 'then' part. So at the moment your script is checking whether the fish sprite is touching the shark sprite, but it's not making anything happen in response.

You can make the fish disappear, as if the shark ate it, by using the `hide`{:class="block3looks"} block.

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    만약 <touching [Sprite1 v] ?> 이라면
+        숨기기
    끝
```

\--- /task \---

Now once the shark catches the fish, the fish disappears for good. That’s not great.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    녹색 깃발을 클릭했을 때
+    보이기
    회전 방식을 [왼쪽-오른쪽 v] 으로 정하기
    무한 반복
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    벽에 닿으면 튕기기
    만약 <touching [Sprite1 v] ?> 이라면
        숨기기
+        (1) 초 기다리기
+        x: ((-240) 부터 (240) 사이의 난수) y: ((-180) 부터 (180) 사이의 난수) 로 이동하기
+        보이기
    끝
```

\--- /task \---

## \--- collapse \---

## title: 어떻게 동작하나요?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!