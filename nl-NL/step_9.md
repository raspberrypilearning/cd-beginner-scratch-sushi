## Score bijhouden

Om bij te houden hoeveel vissen de speler vangt, moet je iets hebben om de score in op te slaan, een manier om erbij op te tellen, en een manier om opnieuw te beginnen als het spel herstart wordt.

Ten eerste: de scoren opslaan!

--- task --- 

Ga naar de **Variabelen** blokken categorie en klik op **Maak een variabele**.

![](images/catch5.png)

Type `score` als de naam.

![](images/catch6.png)

Bekijk je nieuwe variabele!

![De Score variabele wordt weergegeven in het speelveld](images/scoreVariableStage.png) 

--- /task ---

--- collapse ---
---
title: Wat zijn variabelen?
---

Als je informatie wilt opslaan in een programma, dan gebruik je iets dat **variabele** heet. Zie het als een doos met een label erop: je kunt er iets instoppen, controleren wat er in zit, en veranderen wat er in zit. Je vindt de variabelen in de **Variabelen** categorie, maar je moet ze eerst zelf maken zodat ze te zien zijn!

--- /collapse ---

Nu moet de variabele elke keer bijgewerkt worden als de haai een vis pakt, en opnieuw beginnen als het spel wordt herstart. Beide zijn vrij simpel om te doen:

--- task --- 

Pak uit de **Variabelen** categorie de `maak [mijn variabele v] [0]`{:class="block3variables"} en `verander [mijn variabele v] met [1]`{:class="block3variables"} blokken. Klik op de kleine pijltjes in de blokken, kies `score` uit de lijst, en zet de blokken in je programma:

### Code voor de haai

```blocks3
    when green flag clicked
+    set [score v] to [0]
    set rotation style [left-right v]
    go to x: (0) y: (0)
```

### Code voor de vis

```blocks3
   if <touching [Sprite1 v] ?> then
+        change [score v] by [1]
        hide
        wait (1) secs
        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
        show
    end
```

--- /task ---

Gaaf! Nu heb je zelfs een score.
