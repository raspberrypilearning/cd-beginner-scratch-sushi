## الأسماك المتحكم بها عن بعد

حسنًا ، حان الوقت الآن لجعل السمك يسبح من تلقاء نفسه. للقيام بذلك ، ستحتاج إلى نوع جديد من المقاطع: مقاطع **التحكم**.

\--- task \--- حدد كائن السمكة.

اسحب مقطع **الأحداث** `عند نقر العلم الاخضر`{:class="block3events"}، و مقطع **التحكم** `كرر باستمرار`{:class="block3control"}، ومقطع **الحركة** `تحرك 10 خطوة`{:class="block3motion"} إلى **لوحة الكائن**، هكذا:

```blocks3
    عند نقر العلم الأخضر
    كرر باستمرار
        تحرك (10) خطوة
    النهاية
```

\---/task--

## \--- collapse \---

## title: ماذا تفعل المقاطع الجديدة؟

مقاطع **التحكم** تجعل برنامجك يقوم بالأشياء عدة مرات أو تحت ظروف معينة.

هنا ، الأسماك تفعل كل ما هو داخل مقطع ` كرر بإستمرار ` {: class="block3control"} مرارًا وتكرارًا، إلى الأبد. لذلك بمجرد الانتهاء من آخر شيء (المقطع) داخل مقطع ` كرر بإستمرار ` {: class="block3control"} ، تبدأ مجدداً من الأعلى وتفعل كل شيء مرة أخرى ، وهكذا.

\--- /collapse \---

\--- task \--- الآن انقر على العلم الأخضر ومشاهدة ما يحدث! \--- /task \---

حسنًا ، لقد اصطدمت السمكة للتو في جانب المنصة ، وكانت تتحرك بسرعة كبيرة جدًا بحيث لا يمكن ان يصطادها سمك القرش الخاص بك.

أولا ، تحتاج إلى إبطاء حركة الأسماك. هذا في الواقع سهل للغاية ، تحتاج فقط إلى الانتظار لفترة قصيرة بعد أن تتحرك تلك الخطوات العشر. There’s a **Control** block that will help you here:

```blocks3
    انتظر (1) ثانية
```

\--- task \--- أضف مقطع ` انتظر` {: class="block3control"} في التعليمات البرمجية الخاصة بك داخل مقطع `
كرر باستمرار` {: class="block3control"} ، وقم بتغيير الرقم إلى ` 0.5 ` ، هكذا:

```blocks3
    عند نقر العلم الأخضر
    كرر باستمرار
        تحرك (10) خطوة
+      انتظر (0.5) ثانية
    النهاية
```

\--- /task \---

## \--- collapse \---

## title: إجراء التعديلات

الرقم الذي حددته في مقطع `انتظر` يوضح {: class="block3control"} كم عدد ** الثواني ** التي تريد من السمكة أن تنتظر. ` 0.5 ` هو نصف ثانية.

يمكنك اختبار قيم مختلفة لمعرفة ما هو الأفضل للعبة. And remember that you can change the number of steps inside the `move`{:class="block3motion"} block too!

\--- /collapse \---

The fish moves now, but you need it to bounce off the edge of the Stage too. Yet again, there’s a **Motion** block for this!

\--- task \--- Find the `if on edge bounce`{:class="block3motion"} block, and add it in after the `wait`{:class="block3control"} block. \--- /task \---

## \--- collapse \---

## title: ماذا تفعل المقاطع الجديدة؟

The `if on edge bounce`{:class="block3motion"} block checks if the sprite is touching the edge of the Stage and, if it is, it turns left, right, up, or down as appropriate.

\--- /collapse \---

Of course, this will lead to an upside-down fish, so you need a `set rotation style`{:class="block3motion"} block again.

\--- task \--- Update your code to set the rotation style of the fish to `left-right`{:class="block3motion"} at the beginning of the sprite's script:

```blocks3
    when green flag clicked
+    set rotation style [left-right v]
    forever
        move (10) steps
        wait (0.5) secs
        if on edge, bounce
    end
```

\--- /task \---

The fish moves backwards and forwards now, but only in a straight line — a bit too easy for the player to catch with the shark! You need to make the fish less predictable.

You already know from a previous step how to make a sprite turn, so start there.

\--- task \--- Add a turn into the fish's swimming instructions, and click the green flag.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever
        move (10) steps
+        turn cw (10) degrees
        wait (0.5) secs
        if on edge, bounce
    end
```

\--- /task \---

It’s better, but there’s still too much of a pattern. It needs to be more random. Luckily, Scratch can do random for you! You’ll just need a new kind of block, called an **operator** block.

## \--- /collapse \---

## title: What's an operator?

**Operators** take in one or more values (like numbers, text, or `True/False` values) and give back a single value. You can tell the kind of value it will give back by the shape of the block: round ends give numbers or text, pointy ends give `True/False`.

```blocks3
    (() + ())

    (join [hello ] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \--- Find the `pick random`{:class="block3operators"} **operator** block, and plug it into the `turn degrees`{:class="block3motion"} **Motion** block by clicking it and dragging it into the field where you set the number of degrees.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
+        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
    end
```

\--- /task \---

**Note**: you can change the minimum and maximum numbers it will pick, but the default values (`1` and `10`) are pretty good for this game, so you can just leave them.

\--- task \--- انقر على العلم الأخضر لتشغيل البرنامج! \--- /task \---

## \--- collapse \---

## title: So what does the forever block do now?

The forever block now makes the fish sprite do four things in order:

1. Move forward
2. Turn a little bit
3. Wait briefly
4. Check whether it's at the edge of the Stage

Once the sprite has done the check, it will start at the beginning of the loop again and move, turn, wait, check, for as long as you let your Scratch program run.

\--- /collapse \---

Cool! Next up: catching that fish!