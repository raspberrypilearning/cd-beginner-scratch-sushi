## إضافة وإزالة المقاطع البرمجية

عظيم! لقد كتبت أول برنامج Scratch لك. حان الوقت لمعرفة المزيد حول إدخال و إزالة الكود من Scratch! تتكون برمجة Scratch من **مقاطع** كهذه:

![](images/code1.png)

سوف تجد جميع المقاطع في **لوحة المقاطع البرمجية **، ويتم تصنيفها إلى فئات مختلفة وفقا لعملهم.

## \--- collapse \---

## title: استخدام مقاطع من مختلف الفئات

انقر على اسم الفئة لرؤية المقاطع التي تحتويها. هنا ، تم تحديد فئة **الحركة**:

![](images/code2a.png)

جميع المقاطع في الفئة التي نقرت عليها معروضة في قائمة:

![](images/code2b.png)

يمكنك النقر فوق المقطع الذي تريده ، ثم قم بسحبه إلى لوحة الكائن الحالي واتركه. بمجرد وجوده في اللوحة ، يمكنك تحريكه وتوصيله بالمقاطع الأخرى.

\--- /collapse \---

إذا كنت تريد أن ترى ما يقوم به مقطع ما ، فيمكنك النقر مرتين عليه لتشغيله!

\--- task \---

Try double-clicking on some of the blocks to see what they do.

\--- /task \---

## \--- collapse \---

## title: تشغيل الكود

Usually, you want your code to run automatically whenever something specific happens. This is why many of your programs will start with a block from the **Events** category, most often this one:

```blocks3
    عند نقر العلم الأخضر
```

The code blocks connected to this block will run after the **green flag** is clicked.

Code blocks run from top to bottom, so the order in which you snap your blocks together matters. In this example, the sprite will `say`{:class="block3looks"} `Hello!` before it will `play`{:class="block3sound"} the `meow` sound.

```blocks3
    عندما نقر العلم الأخضر
    قل [Hello]
    شغل صوت [meow v]
```

\--- /collapse \---

Removing or deleting code blocks you don’t want in your program is easy! Just drag them back into the code blocks palette.

**Be careful:** dragging them into the code blocks pallette will delete all the blocks connected to the block you drag, so make sure to separate code blocks you want to keep from those you want to remove. If you delete some code blocks by accident and want to get them back, right-click and then click on the **undo** option to get everything back.

![](images/code6.png)

\--- task \---

Try adding, deleting, and undeleting some code blocks!

\--- /task \---

### ضع كل شيء معا

Now you know how to move code around and make things happen, it's time for you to create a program to make the Scratch Cat walk in a circle!

\--- task \---

Make sure you have the cat sprite selected in the sprite list, and then drag the following blocks into the sprite panel and connect them. You’ll find them in the **Events** and **Motion** lists.

```blocks3
    عند نقر العلم الأخضر
    تحرك [10] خطوة
```

\--- /task \---

\--- task \---

Now, click on the green flag above the Stage.

![](images/code7.png)

\--- /task \---

You should see the cat walking in a straight line...not exactly what you want, right?

Note: If you click the flag too many times and the cat walks away, you can drag it back!

\--- task \---

Snap the turn block to the end to make the cat sprite walk in a circle. It’s in the **Motion** list too.

```blocks3
    عند نقر العلم الأخضر
    تحرك [10] خطوة
+ أستدر مع عقارب الساعة (15) درجة
```

\--- /task \---

## \--- collapse \---

## title: كيف يعمل الدوران؟

This block makes the sprite turn 15 degrees of the full 360 degrees that make up a circle. You can change that number, and the number of steps, by clicking on the number and typing in a new value.

![](images/code9.png)

\--- /collapse \---

\--- task \---

Now save your work!

\--- /task \---