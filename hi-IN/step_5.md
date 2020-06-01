## Moving things around

Right now your shark moves in a circle, and it would be much more fun to control it with the arrow keys. On this card, you’re going learn how to do that!

\--- task \---

Start by deleting all code that you have for the shark.

\--- /task \---

जैसा कि आपने शायद अनुमान लगाया है, आपको ** ईवेंट की आवश्यकता है ** और ** गति ** फिर से ब्लॉक!

\--- task \---

This time, look for this block and drag it into the current sprite panel:

```blocks3
    when [space v] key pressed
```

` स्थान के पास स्थित छोटे तीर (▼) पर क्लिक करें ` । You will see a list of all your keyboard keys that you can pick from.

\--- /task \---

कुंजी दबाने पर आपको चार ` की आवश्यकता होगी ` {"class =" block3events "} ब्लॉक - आपके प्रत्येक तीर कुंजी के लिए।

\--- task \---

अपने शार्क को स्थानांतरित करने के लिए, इन ब्लॉकों को ** गति से कनेक्ट करें ** इस तरह से ब्लॉक:

```blocks3
    when [left arrow v] key pressed
    move (-10) steps
```

```blocks3
    when [right arrow v] key pressed
    move (10) steps
```

```blocks3
    when [up arrow v] key pressed
```

```blocks3
    when [down arrow v] key pressed
```

\--- /task \---

** ध्यान दें ** : ` -10 ` '10 कदम पीछे हटो' का मतलब है।

\--- task \---

Now click the green flag to test out your code.

\--- /task \---

Now your shark moves back and forwards, which is pretty cool, but it doesn’t move up or down. Also, if you look through the **Motion** blocks, you’ll see there are no blocks for 'up' or 'down'. उनमें से एक पूरा गुच्छा ** x से संबंधित है ** और ** y ** हालांकि निर्देशांक - चलो उन की कोशिश करो!

\--- task \---

दो ` परिवर्तन y द्वारा पकड़ो ` {= class = "block3motion"} ब्लॉक करता है, और अपना कोड इस तरह से अपडेट करें:

```blocks3
    when [up arrow v] key pressed
+     change y by (10)
```

```blocks3
    when [down arrow v] key pressed
+     change y by (-10)
```

\--- /task \---

Now when you press the arrows keys, the shark moves all around the stage!

## \--- collapse \---

## title: How do x- and y-coordinates work?

To talk about the positions of objects, such as sprites, we often use x- and y-coordinates. ** x- अक्ष ** स्टेज समन्वय प्रणाली ** बाएं से दाएं चलती है ** , और ** y- अक्ष ** ** नीचे से ऊपर तक चलता है ** ।

![](images/moving3.png)

एक स्प्राइट इसके केंद्र के निर्देशांक द्वारा स्थित हो सकता है, उदाहरण के लिए `(15, -27)` , जहां `15` एक्स-अक्ष के साथ इसकी स्थिति है, और `-27` y-अक्ष के साथ इसकी स्थिति।

+ यह वास्तव में कैसे काम करता है, इसके बारे में महसूस करने के लिए, स्प्राइट का चयन करें और **x** और **y** का उपयोग करें निर्देशांक के लिए अलग-अलग मान सेट करके इसे चरण के चारों ओर ले जाने के लिए नियंत्रण।

![](images/xycoords.png)

+ मूल्यों के विभिन्न युग्मों को देखने की कोशिश करें कि स्प्राइट कहां जाता है! स्क्रैच में x- अक्ष `-240` से जाता है `240`, और y- अक्ष `-180` से `180` जाता है ।

\--- /collapse \---

### खेल को फिर से शुरू करना

शार्क अब पूरे स्क्रीन पर घूमती है, लेकिन कल्पना करें कि यह एक गेम है: आप इसे कैसे पुनः आरंभ करते हैं, और प्रत्येक गेम की शुरुआत में क्या होता है?

खिलाड़ी को खेल शुरू करने पर आपको शार्क को उसके मूल स्थान पर लाने की आवश्यकता होती है। वे हरे झंडे पर क्लिक करके इस खेल को शुरू करेंगे, इसलिए जब आप ऐसा करते हैं तो शार्क स्प्राइट के x- और y- निर्देशांक को बदलना होगा।

यह वास्तव में बहुत आसान है! मंच का केंद्र `(0, 0)` में <0 >(x, y)</code> निर्देशांक।

तो आप सभी की जरूरत है एक **Events** उस हरे झंडे के लिए ब्लॉक करें, और **go to ** से ब्लॉक करें **Motion** ।

\--- task \---

हरी झंडी क्लिक करने पर `when green flag clicked`{:class="block3events"} **Event** वर्तमान स्प्राइट पैनल पर ब्लॉक करें।

```blocks3
    when green flag clicked
```

फिर `go to`{:class="block3motion"} **Motion** ब्लॉक करें, और इसे अपने ध्वज से संलग्न करें **Events** खंड मैथा।

```blocks3
    when green flag clicked
+     go to x: (0) y: (0)
```

दोनों को सेट करें `x` और `y` `0` से समन्वयित करें में जाएं `go to`{:class="block3motion"} ब्लॉक करें यदि वे पहले से ही नहीं हैं `0` ।

\--- /task \---

\--- task \---

अब हरे झंडे पर क्लिक करें: आपको शार्क को मंच के केंद्र में वापस जाना चाहिए!

\--- /task \---