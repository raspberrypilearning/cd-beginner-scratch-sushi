## Peștele care se mișcă singur

Ok, acum este timpul să faci peștele să înoate singur. Pentru a face asta, vei avea nevoie de un nou tip de bloc: un bloc **Control**.

\--- task \---

Selectează-ți costumul de pește.

Trage un bloc `când se dă click pe stegulețul verde`{:class="block3events"} de la **Evenimente**, un bloc `la infinit`{:class="block3control"} de la **Control** și un bloc `mergi 10 pași`{:class="block3motion"} de la **Mișcare** în **panoul personajului**, astfel:

```blocks3
    when green flag clicked
    forever
        move (10) steps
    end
```

\--- /task \---

## \--- collapse \---

## title: Ce face noul bloc?

**Blocurile de control** sunt folosite pentru a face lucruri de un anumit număr de ori, sau pentru a le face doar în anumite condiții.

Aici, peștele repetă la infinit tot ce este în interiorul blocului `la infinit`{:class="block3control"}. Deci, odată ce a făcut ultimul lucru (bloc) din blocul `la infinit`{:class="block3control"}, o ia de la început și face totul din nou.

\--- /collapse \---

\--- task \---

Acum apasă pe steagul verde și urmărește ce se întâmplă!

\--- /task \---

Ei bine, acel pește tocmai s-a izbit de marginea scenei și se mișcă prea repede pentru a îl putea prinde rechinul.

Primul lucru pe care trebuie să îl faci este să încetinești peștele. Acest lucru este destul de ușor, trebuie doar să îl faci să aștepte puțin după ce face cei 10 pași. Există un bloc **Control** care te va ajuta cu asta:

```blocks3
    așteaptă (1) secunde
```

\--- task \---

Adaugă blocul `așteaptă`{:class="block3control"} în codul din interiorul blocului `la infinit`{:class="block3control"} și schimbă numărul la `0.5`, astfel:

```blocks3
    when green flag clicked
    forever
        move (10) steps
+      wait (0.5) secs
    end
```

\--- /task \---

## \--- collapse \---

## title: Ajustarea

Numărul pe care l-ai setat în blocul `așteaptă`{:class="block3control"} reprezintă câte **secunde** vrei să aștepte peștele. `0.5` este o jumătate de secundă.

Poți testa diferite valori pentru a vedea care este cea mai bună pentru joc. Și ține minte că poți schimba numărul de pași din blocul `mergi`{:class="block3motion"}!

\--- /collapse \---

Peștele se mișcă acum, dar trebuie și să ricoșeze din marginea scenei. Din nou, există un bloc **Mișcare** pentru asta!

\--- task \---

Caută blocul `dacă atinge marginea, ricoșează`{:class="block3motion"} și adaugă-l sub blocul `așteaptă`{:class="block3control"}.

\--- /task \---

## \--- collapse \---

## title: Ce face noul bloc?

Blocul `dacă atinge marginea, ricoșează`{:class="block3motion"} verifică dacă personajul a atins marginea Scenei și, dacă da, îl întoarce spre stânga, dreapta, sus sau jos, după caz.

\--- /collapse \---

Bineînțeles, acest lucru va face ca peștele să ajungă cu capul în jos, deci ai nevoie de un bloc `setează stilul de rotație`{:class="block3motion"} din nou.

\--- task \---

Modifică-ți codul să seteze stilul de rotație al peștelui la `stânga-dreapta`{:class="block3motion"} la începutul scriptului personajului:

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

Acum peștele se mișcă înainte și înapoi, dar se mișcă în linie dreaptă — e un pic prea ușor pentru jucător să prindă-l cu rechinul! Trebuie să faci peștele mai puțin previzibil.

Deja știi dintr-un pas anterior cum să faci un personaj să se rotească, așa că poți să începi de acolo.

\--- task \---

Adaugă o rotire în instrucțiunile de înot ale peștelui și apasă pe steagul verde.

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

E mai bine, dar e încă prea previzibil. Trebuie să fie mai aleatoriu. Din fericire, Scratch poate face asta! Vei avea nevoie de un nou tip de bloc, numit bloc **operator**.

## \--- collapse\---

## title: Ce este un operator?

**Operatorii** iau una sau mai multe valori (cum ar fi numere, text sau valori `Adevărat/Fals`) și returnează o singură valoare. Îți poți da seama ce tip de valoare va întoarce dupa forma blocului: cele cu capete rotunjite întorc numere sau text, iar cele cu capete ascuțite returnează `Adevărat/Fals`.

```blocks3
    (() + ())

    (alătură [salut ] [lume])

    <[] = []>
```

\--- /collapse \---

\--- task \---

Caută blocul **Operator** `alege aleator`{:class="block3operators"} și inserează-l în blocul `rotește-te`{:class="block3motion"} din **Mișcare**, trăgându-l până în căsuța unde se setează numărul de grade.

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

**Notă**: poți schimba numărul minim și maxim din care va alege, dar valorile implicite (`1` și `10`) sunt destul de bune pentru acest joc, deci să le poți lăsa așa.

\--- task \---

Apasă pe steagul verde pentru a executa codul!

\--- /task \---

## \--- collapse \---

## title: Deci, ce face blocul la infinit acum?

Blocul la infinit face ca personajul pește să facă patru lucruri în ordine:

1. Merge înainte
2. Se rotește puțin
3. Așteaptă puțin
4. Verifică dacă este la marginea Scenei

După ce personajul a făcut verificarea, va începe din nou de la începutul buclei și se va mișca, se va întoarce, va aștepta, va verifica, cât timp cât timp programul Scratch va rula.

\--- /collapse \---

Super! Următorul pas: prinderea peștelui!