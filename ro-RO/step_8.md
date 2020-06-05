## La pescuit!

Rechinul se mișcă, peștele înoată, dar nu interacționează: dacă peștele înoată în gura rechinului, nu se întâmplă nimic. E timpul să schimbăm asta!

În primul rând, trebuie să verifici dacă peștele atinge rechinul. Pentru aceasta, vei avea nevoie de un bloc **Control** și un bloc **Detectare**.

--- task ---

Adaugă blocul `dacă... atunci`{:class="block3control"} de tip **Control** în interiorul buclei `la infinit`{:class="block3control"} dedesubtul blocului `dacă atinge marginea, ricoșează`{:class="block3motion"} în codul peștelui.

Trage blocul `atinge...`{:class="block3sensing"} în spațiul din partea de sus a blocului `dacă...atunci`{:class="block3control"} și apasă pe triunghiul mic pentru a selecta numele personajului rechin. Dacă nu l-ai schimbat, va fi „Personaj1”.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
+        if <touching [Sprite1 v] ?> then
    end
```

--- /task ---

--- collapse ---
---
title: Cum funcționează?
---

Blocul `dacă...atunci`{:class="block3control"} de tip **Control** trebuie să primească o valoare `Adevărat/Fals`.

Blocurile **Detectare** colectează informații, cum ar fi în unde se află un personaj, ce lucruri atinge etc. Tu folosești acest bloc:

```blocks3
    <touching [Sprite1 v] ?>
```

Dacă te uiți la capetele ascuțite ale acestui bloc, îți poți da seama că va returna valoarea `Adevărat/Fals` de care are nevoie blocul `dacă...atunci`{:class="block3control"}.

--- /collapse ---

Desigur, tocmai ai adăugat un bloc `dacă...atunci`{:class="block3control"} fără a adăuga nimic la partea „atunci”. Deci, în acest moment, scriptul tău verifică dacă personajul pește atinge personajul rechin, dar nu se va întâmpla nimic dacă acesta este cazul.

Poți face peștele să dispară, ca ca și cum rechinul l-ar fi mâncat, folosind blocul `ascunde`{:class="block3looks"}.

--- task ---

Caută blocul `ascunde`{:class="block3looks"} în lista **Aspect** și pune-l în interiorul blocului `dacă...atunci`{:class="block3control"}, astfel:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

--- /task ---

Acum, după ce rechinul prinde peștele, peștele dispare pentru totdeauna. Asta nu e prea grozav.

--- task ---

Pune blocul `arată`{:class="block3looks"} de la **Aspect** chiar la începutul codului peștelui, pentru a putea reseta jocul.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

--- /task ---

Arată deja mai bine, dar nu vrei ca jucătorul să fie nevoit să repornească jocul de fiecare dată când prinde un singur pește!

--- task ---

Modifică codul din blocul `dacă...atunci`{:class="block3control"} să arate astfel:

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

--- /task ---

--- collapse ---
---
title: Cum funcționează?
---

Faci un lucru inteligent: când peștele este ascuns, așteaptă, se mișcă și apoi apare din nou.

Se pare că o mulțime de pești continuă să apară, dar este un singur personaj care se tot mișcă!

--- /collapse ---

Ai făcut un joc! Dar încă nu se ține scorul și nici nu se poate câștiga. Poți rezolva și asta — pe următorul card!