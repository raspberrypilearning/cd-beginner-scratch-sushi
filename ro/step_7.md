## Pește controlat de program
Ok, acum hai să facem peștele să înoate de unul singur. Ca să facem asta, ne trebuie un nou tip de bloc: un bloc de **Control**. 

+ Pentru început selectează personajul pește!

+ Trage un **Eveniment** `când steagul verde este apăsat`{:class="block3events"}, un **Control** `la nesfarșit`{:class="block3control"}, și o **Mișcare** `mergi 10 pași`{:class="block3motion"} în **panoul personajului**, așa: 
![blocks_1546569177_729224](images/blocks_1546569177_729224.png)

--- collapse ---
---
title: Ce face noul bloc?
---

Blocurile de **Control** fac acţiuni în mod repetat de un anumit număr de ori, sau cât timp se respectă anumite condiţi.

Aici, peștele face orice este înăuntrul blocului `la nesfarșit`{:class="block3control"} într-una, fara să se opreasca. Deci odată ce a făcut ultima acţiune din blocul `la nesfarșit`{:class="block3control"}, o ia de la capăt și reface toate acţiunile, iar și iar.

--- /collapse ---

+ Acum apasă pe steagul verde și urmărește ce se întâmplă!

Ei bine, primul tău pește s-a lovit de marginea Scenei, și se mișcă prea repede pentru că un Rechin să îl poată prinde.

Pentru început, trebuie să încetinești peștele. Asta e destul de ușor, trebuie doar să îl pui să aștepte puţin după fiecare 10 pași făcuţi.
![blocks_1546569178_800881](images/blocks_1546569178_800881.png)


+ Adaugă blocul `așteaptă`{:class="block3control"} în codul tău înăuntrul blocului `la nesfarșit`{:class="block3control"}, și schimbă numărul în `0.5`, astfel:


![blocks_1546569179_881654](images/blocks_1546569179_881654.png)


--- collapse ---
---
title: Ajustari
---

Numărul pe care l-ai setat la `așteptare`{:class="block3control"} zice cate **secunde** vrei să aștepte peștele. `0.5` este jumătate de secundă.

Poţi încerca cu mai multe valori și vezi care se potrivește mai bine pentru jocul tău. Și reţine că poţi schimbă și numărul de pași din blocul `mergi`{:class="block3motion"}!
--- /collapse ---

Peștele se mișcă acum, dar vrei să se și întoarcă când atinge marginea Scenei. Ce noroc că ai un bloc de **Mișcare** pentru asta!

+ Găsește blocul `dacă atingi marginea întoarce-te`{:class="block3motion"} și adauga-l după blocul `așteaptă`{:class="block3control"}.

--- collapse ---
---
title: Ce face noul bloc?
---

Blocul `dacă atingi marginea întoarce-te`{:class="block3motion"} verifica dacă personajul atinge merginea Scenei și, dacă atinge, se întoarce în direcţia opusă.
--- /collapse ---

Însă asta ar rezultă într-un pește cu sus-ul în jos, așa că îţi trebuie un bloc `setează stilul răsuciri`{:class="block3motion"}.

+ Schimba codul și setează stilul de răsucire în `stânga-dreapta`{:class="block3motion"} la începutul programului pentru acest personaj:

![blocks_1546569180_992167](images/blocks_1546569180_992167.png)

Peștele se mișcă în faţă și în spate acum, dar numai în linie dreaptă — umpic prea ușor pentru jucătorul cu Rechinul! Trebuie să faci peștele mai imprevizibil.

Ști deja din pașii anteriori cum să faci un personaj să se răsucească, începe de acolo!

+ Adaugă o răsucire în mișcarea peștelui, după care apasă steagul verde.

![blocks_1546569182_10717](images/blocks_1546569182_10717.png)

E mai bine, dar încă este prea multă predictibilitate în mișcările peștelui. Trebuie să fie mai întâmplătoare. Din fericire, Scratch poate să ia decizi întâmplătoare pentru tine! Pentru asta o să ai nevoie de un nou bloc, de **Operaţie**.

--- collapse ---
---
title: Ce este o operaţie?
---

**Operaţile** primesc una sau mai multe valori (că numere, text, `Adevărat/Fals`) și dau înapoi o singură valoare. Vei ști ce fel de valoare vor rezultă din forma blocului: cele rotunjite rezultă număr sau text, iar cele ascuţite `Adevărat/Fals`.

![blocks_1546569183_229207](images/blocks_1546569183_229207.png)

--- /collapse ---

+ Gasește **operaţia** `alege la întâmplăre`{:class="block3operators"} , și trage-o în campul unde setezi numărul de grade din blocul de **Mișcare** `grade de rotaţie`{:class="block3motion"}.

![blocks_1546569184_331149](images/blocks_1546569184_331149.png)

**Nota**: poţi schimbă minimul și maximul din care să se aleagă la întâmplăre, dar cele de bază(`1` și `10`) sunt destul de bune pentru acest joc, așa că le poţi lăsa neschimbate.

+ Acum apasă steagul verde și urmărește ce se întâmplă!

--- collapse ---
---
title: Deci ce face acum blocul de "la nesfarșit"?
---

Blocul de "la nesfarșit" face personajul pește să faca 4 lucruri în ordine:
1. Să meargă înainte
1. Să se rotească umpic
1. Să aștepte
1. Să verifice dacă e la marginea Scenei  

Când personajul termină de făcut verificarea, o să înceapă de la capătul buclei și o să meargă, rotească, aștepte, verifice din nou și din nou pana când o să oprești programul Scratch.
 
 --- /collapse ---
 
Cool! Urmează: să prinzi peștele!

