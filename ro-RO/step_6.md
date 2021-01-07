## Toate personajele

Acum ai un rechin pe care îl poți mișca folosind tastele săgeți. Frumos! E timpul să adaugi niște pești pe care să îi prindă.

\--- task \---

Apasă pe butonul **Alege un personaj** și alege un pește în ecranul care se deschide.

![Butonul Alege un Personaj](images/spritesNewFromLibrary.png)

Dacă peștele e prea mare față de rechin poți să folosești căsuța pentru dimensiune pentru a îi face să aibă dimensiunile potrivite!

![Căsuța pentru dimensiune](images/sprites2.png)

Change the number in the size control to make the sprite bigger or smaller.

\--- /task \---

Grozav! Mai târziu, vei adăuga niște cod pentru a face peștele să se miște singur, fără ajutor din partea jucătorului. Jucătorul tău va mișca rechinul și va încerca să prindă peștele.

## \--- collapse \---

## title: Ce se întâmplă cu rechinul când se mișcă cu spatele?

Arată cam puțin ciudat ca rechinul să înoate înapoi. Așa cum în mod normal te întorci înapoi in loc să mergi cu spatele, rechinul ar trebui să se întoarcă în loc să înoate cu spatele. Din fericire pentru tine, Scratch are un bloc pentru asta!

Blocul `orientează-te în direcția`{:class="block3motion"} îți permite să alegi direcția în care să fie îndreptat personajul. Îl poți găsi în secțiunea de blocuri **Mișcare**. Poți introduce orice număr de grade, pentru a orienta personajul în orice direcție vrei.

\--- /collapse \---

\--- task \---

Ia câteva blocuri `orientează-te în direcția`{:class="block3motion"} de la **Mișcare** și conectează-le la codul rechinului tău, astfel:

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

Modifică numărul de pași din blocul `mergi`{:class="block3motion"} de la `-10` la `10`.

Dacă miști rechinul acum după ce ai adăugat blocul `orientează-te în direcția`{:class="block3motion"}, vei observa că se întâmpla ceva puțin ciudat. Rechinul nu se rotește cum trebuie!

![Rechin cu capul în jos](images/spritesUpsideDown.png)

\--- /task \---

## \--- collapse \---

## title: De ce se întoarce cu capul în jos?

Problema este că personajul rechin a început, ca toate personajele, cu **stilul de rotație** „de jur împrejur“, iar ție îți trebuie să aibă stilul „stânga-dreapta“.

Ca de obicei, există un bloc pentru asta, și este în **Mișcare**!

\--- /collapse \---

\--- task \---

Caută în categoria **Mișcare** blocul `setează stilul de rotație`{:class="block3motion"}.

Adaugă blocul la codul de resetare a rechinului și setează stilul de rotație la `stânga-dreapta`{:class="block3motion"}, astfel:

```blocks3
    when green flag clicked
+     set rotation style [left-right v]
    go to x: (0) y: (0)
```

\--- /task \---