## الأسماك المتحكم بها عن بعد

حسنًا ، حان الوقت الآن لجعل السمكة تسبح من تلقاء نفسها. للقيام بذلك ، ستحتاج إلى نوع جديد من المقاطع: مقاطع **التحكم**.

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

هنا ، السمكة تفعل كل ما هو داخل مقطع ` كرر بإستمرار ` {: class="block3control"} مرارًا وتكرارًا، إلى الأبد. لذلك بمجرد الانتهاء من آخر شيء (المقطع) داخل مقطع ` كرر بإستمرار ` {: class="block3control"} ، تبدأ مجدداً من الأعلى وتفعل كل شيء مرة أخرى ، وهكذا.

\--- /collapse \---

\--- task \--- الآن انقر على العلم الأخضر ومشاهدة ما يحدث! \--- /task \---

حسنًا ، لقد اصطدمت السمكة للتو في جانب المنصة ، وكانت تتحرك بسرعة كبيرة جدًا بحيث لا يمكن ان يصطادها سمك القرش الخاص بك.

أولا ، تحتاج إلى إبطاء حركة السمكة. هذا في الواقع سهل للغاية ، تحتاج فقط إلى الانتظار لفترة قصيرة بعد أن تتحرك تلك الخطوات العشر. There’s a **Control** block that will help you here:

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

يمكنك اختبار قيم مختلفة لمعرفة ما هو الأفضل للعبة. وتذكر أنه يمكنك تغيير عدد الخطوات داخل مقطع `تحرك` {: class = "block3motion"} أيضًا!

\--- /collapse \---

السمكة تتحرك الآن، لكنك في حاجة إليها لترتد من على حافة المنصة أيضًا. مرة أخرى ، هناك مقطع في** الحركة ** لهذا!

أوجد مقطع `ارتد إذا كنت عند الحافة`{:class="block3motion"}، وأضفه بعد مقطع `انتظر` {:class="block3control"}. \--- /task \---

## \--- collapse \---

## title: ماذا تفعل المقاطع الجديدة؟

يقوم مقطع `ارتد إذا كنت عند الحافة`{:class="block3motion"} بالتحقق ما إذا كان الكائن يلامس حافة المنصة و ،إذا كان يلامس، يغير اتجاه إلى اليسار او اليمين او للأعلى او للأسفل على حسب الملائم.

\--- /collapse \---

بالطبع ، سيؤدي ذلك إلى سمكة مقلوبة ، لذا فأنت بحاجة إلى مقطع `اجعل نمط الدوران`{:class="block3motion"} مرة اخرى.

\--- task \--- حدث البرمجة الخاصة بك لجعل نمط الدوران للسمكة إلى `يمين - يسار`{:class="block3motion"} في بداية برمجة الكائن:

```blocks3
    عند نقر العلم الأخضر 
+    اجعل نمط الدوران  [يمين - يسار v]
    كرر باستمرار
        تحرك (10) خطوة
        انتظر (0.5) ثانية
        ارتد إذا كنت عند الحافة
    النهاية
```

\--- /task \---

تتحرك السمكة للخلف وللأمام الآن ، ولكن فقط في خط مستقيم - من السهل جدًا على اللاعب اللحاق بها باستخدام القرش! تحتاج إلى جعل السمكة أقل قابلية للتنبؤ.

انت تعرف مسبقاً من خطوة سابقة كيف تجعل الكائن يستدير، لذا ابدأ من هناك.

\--- task \--- أضف الإستدارة إلى تعليمات السباحة للسمكة ، وانقر على العلم الأخضر.

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