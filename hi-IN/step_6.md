## All the sprites

Now you have a shark that you can move around using the arrow keys. Nice! Time to add some fish for it to catch.

\--- task \---

Click the **New sprite** button, and on the screen that opens, choose a fish.

![The New sprite button](छवियों / spritesNewFromLibrary.png)

यदि आपकी मछली आपके शार्क की तुलना में थोड़ी बड़ी है, तो आप दोनों को सही आकार में बनाने के लिए आकार नियंत्रण का उपयोग कर सकते हैं!

![Sprite size control](images/sprites2.png)

सर्पिल को बड़ा या छोटा करने के लिए आकार नियंत्रण में संख्या बदलें।

\--- /task \---

Great! Later, you're going to add some code to make the fish move around on its own, without help from the player. Your player will move the shark and try to catch the fish.

## \--- collapse \---

## शीर्षक: पीछे की शार्क के बारे में क्या?

It does look a little funny to have that shark swimming backwards. Just like you’d usually turn around rather than walking backwards, the shark would turn around rather than swimming backwards. Luckily for you, Scratch has a block for this!

The `point in direction`{:class="block3motion"} block lets you pick the direction your sprite is pointing in. आप इसे ** गति में पाएंगे ** खंड खंड। You can type in any number of degrees, to point the sprite wherever you want.

\--- /collapse \---

\--- task \---

Grab a couple of copies of the `point in direction`{:class="block3motion"} block from the **Motion** list and connect them to your shark's code, like this:

```blocks3
    when [left arrow v] key pressed
+     point in direction (-90)
    move (10) steps
```

```blocks3
    when [right arrow v] key pressed
+     point in direction (90)
    move (10) steps
```

\--- /task \---

\--- task \---

` चाल में चरणों की संख्या बदलें ` {<class = "block3motion"} ब्लॉक ` -10 से ` को ` 10 ` ।

यदि आपने दिशा में ` बिंदु को जोड़ने के बाद शार्क को अब चारों ओर ले जाने का प्रयास किया है ` {"class =" block3motion "} ब्लॉक, आपको कुछ अजीब सा हो रहा है। The shark may not be turning quite right!

![Upside down shark](images/spritesUpsideDown.png)

\--- /task \---

## \--- collapse \---

## title: Why does it go upside down?

The problem here is that the shark sprite started, as all sprites do, with the 'all around' **rotation style**, and what you need it to have is the 'left-right' style.

As usual, there’s a block for that, and it’s in **Motion**!

\--- /collapse \---

\--- task \---

** गति में देखें ** श्रेणी के लिए श्रेणी ` रोटेशन शैली सेट करें ` {: वर्ग = "block3motion"}।

ब्लॉक को पहले से अपने शार्क रीसेट कोड में जोड़ें, और रोटेशन शैली को ` बाएं-दाएं पर सेट करें ` {, class = "block3motion"}, इस तरह:

```blocks3
    when green flag clicked
+     set rotation style [left-right v]
    go to x: (0) y: (0)
```

\--- /task \---