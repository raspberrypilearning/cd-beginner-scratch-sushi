## نقل الأشياء في جميع الأنحاء

الآن يتحرك القرش في دائرة ، وسيكون من الممتع اكثر ان نتحكم به باستخدام مفاتيح الأسهم. على هذه البطاقة ، سوف تتعلم كيفية القيام بذلك!

\--- task \--- ابدأ بحذف جميع المقاطع البرمجية التي لديك للقرش. \--- /task \---

كما قد تكون خمنت على الأرجح ، ستحتاج إلى مقاطع **الأحداث** و **الحركة** مرة أخرى!

\--- task \--- هذه المرة ، ابحث عن هذه الكتلة و اسحبها إلى لوحة الكائن الحالي:

```blocks3
    عند الضغط على مفتاح [المسافة v]
```

انقر على السهم الصغير (▼) بجانب `المسافة `. سترى قائمة بجميع مفاتيح لوحة المفاتيح التي يمكنك الاختيار منها. \--- /task \---

ستحتاج إلى أربعة من مقاطع ` عند الضغط على المفتاح ` {: class = "block3events"} - واحدة لكل مفتاح من مفاتيح الأسهم الخاصة بك.

\--- task \--- لتحريك سمك القرش ، قم بتوصيل هذه المقاطع بمقاطع ** الحركة ** هكذا:

```blocks3
    عندما ضغط مفتاح [السهم الأيسر v] 
    تحرك (-10) خطوة
```

```blocks3
    عندما ضغط مفتاح [السهم الأيمن v]
    التحريك (10) خطوة
```

```blocks3
    عند ضغط مفتاح [السهم العلوي v]
```

```blocks3
    عند ضغط مفتاح [السهم السفلي v]
```

\--- /task \---

** ملاحظة **: ` -10 ` يعني "العودة 10 خطوات".

\--- task \--- الآن انقر على العلم الأخضر لاختبار التعليمات البرمجية الخاصة بك. \--- /task \---

يتحرك سمك القرش الآن للخلف وللأمام ، وهو أمر رائع ، لكنه لا يتحرك للأعلى أو للأسفل. أيضًا ، إذا نظرت إلى مقاطع ** الحركة ** ، سترى أنه لا توجد مقاطع لـ "أعلى" أو "لأسفل". هناك مجموعة كاملة منها مرتبطة بـاحداثيات ** س ** و ** ص ** رغم ذلك - دعنا نجرب هؤلاء!

\--- task \--- اسحب اثنين `غير الموضع ص بمقدار` {: class = "block3motion"} ، وحدث البرمجة الخاص بك هكذا:

```blocks3
    عند الضغط على مفتاح [السهم العلوي v]
+ غير الموضع ص بمقدار (10)
```

```blocks3
    عند الضغط على مفتاح [السهم السفلي v]
+ غير الموضع ص بمقدار (10-)
```

\--- /task \---

الآن عند الضغط على مفاتيح الأسهم ، يتحرك القرش في جميع أنحاء المنصة!

## \--- collapse \---

## title: How do x- and y-coordinates work?

To talk about the positions of objects, such as sprites, we often use x- and y-coordinates. The **x-axis** of the Stage coordinate system runs from **left to right**, and the **y-axis** runs from **bottom to top**.

![](images/moving3.png)

A sprite can be located by the coordinates of its centre, for example `(15, -27)`, where `15` is its position along the x-axis , and `-27` its position along the y-axis.

+ To get a feel for how this actually works, select a sprite and use the **x** and **y** controls to move it around the stage by setting different values for the coordinates.

![](images/xycoords.png)

+ Try different pairs of values to see where the sprite goes! In Scratch, the x-axis goes from `-240` to `240`, and the y-axis goes from `-180` to `180`.

\--- /collapse \---

### Restarting the game

The shark moves all over the screen now, but imagine this is a game: how do you restart it, and what happens at the start of each game?

You need to get the shark to its original location when the player starts the game. They'll start this game by clicking on the green flag, so you need to change the shark sprite's x- and y-coordinates when that happens.

That’s actually pretty easy! The centre of the stage is `(0, 0)` in `(x, y)` coordinates.

So all you need is an **Event** block for that green flag, and the **go to** block from **Motion**.

\--- task \--- Drag a `when green flag clicked`{:class="block3events"} **Event** block onto the current sprite panel.

```blocks3
    when green flag clicked
```

Then find the `go to`{:class="block3motion"} **Motion** block, and attach it to your flag **Event** block.

```blocks3
    when green flag clicked
+     go to x: (0) y: (0)
```

Set the both the `x` and the `y` coordinate to `0` in the `go to`{:class="block3motion"} block if they are not already `0`.

\--- /task \---

\--- task \--- Now click the green flag: you should see the shark return to the centre of the stage! \--- /task \---