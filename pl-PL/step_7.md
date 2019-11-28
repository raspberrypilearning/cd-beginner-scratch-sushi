## Ryby zdalnie sterowane

Ok, teraz nadszedł czas, aby spowodować, żeby ryba płynęła sama. Aby to zrobić, będziesz potrzebować nowego rodzaju bloku: bloku **Kontrola**.

--- task --- Wybierz duszek ryby.

Przeciągnij do panelu duszka blok `kiedy flaga kliknięta`{:class="block3events"} z sekcji **Zdarzenia**, blok pętli `zawsze`{:class="block3control"} z sekcji **Kontrola** oraz blok `przesuń o 10 kroków`{:class="block3motion"} z sekcji **Ruch**, tak jak pokazano poniżej:

```blocks3
    kiedy kliknięto zieloną flagę
    zawsze
        przesuń o (10) kroków
    koniec
```

--- /task ---

--- collapse ---
---
title: Co robi nowy blok?
---

Bloki **Kontroli** powodują, że Twój program wykonuje pewne czynności kilka razy lub pod pewnymi warunkami.

Tutaj ryba robi wszystko, co znajduje się w bloku pętli `zawsze`{:class="block3control"} powtarzając to w nieskończoność. Kiedy więc zrobi ostatnią rzecz (blok) wewnątrz bloku pętli `zawsze`{:class="block3control"}, zaczyna od początku i robi wszystko ponownie, i tak w nieskończoność.

--- /collapse ---

--- task --- Teraz kliknij zieloną flagę i zobacz, co się stanie! --- /task ---

Cóż, ta ryba właśnie uderzyła w ścianę Sceny i poruszała się o wiele za szybko, aby Twój rekin mógł ją złapać.

Najpierw musisz spowolnić rybę. W rzeczywistości jest to całkiem proste, wystarczy, że poczeka chwilę, po przesunięciu się o 10 kroków. Jest blok w sekcji **Kontrola**, który pomoże Ci w tym:

```blocks3
    czekaj (1) sekund
```

--- task --- Dodaj blok `czekaj`{:class="block3control"} do swojego kodu wewnątrz bloku pętli `zawsze`{:class="block3control"} i zmień liczbę na `0.5`, jak poniżej:

```blocks3
    kiedy kliknięto zieloną flagę
    zawsze
        przesuń o (10) kroków
+ czekaj (0.5) sekund
    koniec
```

--- /task ---

--- collapse ---
---
title: Dokonywanie zmian
---

Liczba ustawiona w bloku `czekaj`{:class="block3control"} mówi, ile **sekund** chcesz, żeby ryba czekała. `0.5` to pół sekundy.

Możesz przetestować różne wartości, aby zobaczyć, która jest najlepsza dla gry. I pamiętaj, że możesz także zmienić liczbę kroków w bloku `przesuń o`{:class="block3motion"}!

--- /collapse ---

Teraz ryba porusza się, ale musisz spowodować, żeby również odbijała się od krawędzi sceny. Po raz kolejny jest na to blok w sekcji **Ruch**!

--- task --- Znajdź blok `jeżeli na brzegu, odbij się`{:class="block3motion"} i dodaj go zaraz po bloku `czekaj`{:class="block3control"}. --- /task ---

--- collapse ---
---
title: Co robi nowy blok?
---

Blok `jeżeli na brzegu, odbij się`{:class="block3motion"} sprawdza, czy duszek dotyka krawędzi sceny i, jeśli tak jest, obraca się odpowiednio w lewo, w prawo, w górę lub w dół.

--- /collapse ---

Oczywiście, będzie to prowadzić do ryby w pozycji do góry nogami, więc trzeba ponownie wykorzystać blok `ustaw styl obrotu`{:class="block3motion"}.

--- task --- Zaktualizuj swój kod, aby ustawić styl obrotu ryby na `lewo-prawo`{:class="block3motion"} na początku kodu duszka:

```blocks3
    kiedy kliknięto zieloną flagę
+    ustaw styl obrotu na [lewo-prawo v]
    zawsze
        przesuń o (10) kroków
        czekaj (0.5) sekund
        jeżeli na brzegu, odbij się
    koniec
```

--- /task ---

Ryba porusza się teraz do tyłu i do przodu, ale tylko w linii prostej - trochę zbyt łatwo jest graczowi złapać tą rybę rekinem! Musisz sprawić, aby ryba była mniej przewidywalna.

Już wiesz z poprzedniego kroku, jak zrobić, żeby duszek się obracał, więc zacznij od tego.

--- task --- Dodaj obrót do instrukcji pływania ryby i kliknij zieloną flagę.

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw styl obrotu na [lewo-prawo v]
    zawsze 
          przesuń o (10) kroków
+           obróć w prawo o (10) stopni
          czekaj (0.5) sekund
          jeżeli na brzegu, odbij się
    koniec
```

--- /task ---

Jest lepiej, ale ryba wciąż porusza się według wzoru. Poruszanie się ryby musi być bardziej przypadkowe. Na szczęście Scratch może ustawić dla Ciebie losowość w programie! Potrzebujesz tylko nowego rodzaju bloku, zwanego blokiem **Wyrażenia**.

--- collapse ---
---
title: Co to jest wyrażenie (ang. operator)?
---

**Wyrażenia** przyjmują jedną lub więcej wartości (takich jak liczby, tekst lub wartości `Prawda/Fałsz`) i zwracają pojedynczą wartość. Możesz określić rodzaj wartości, jaką wyrażenie zwróci na podstawie kształtu bloku: zaokrąglone końce zwracają liczby lub tekst, spiczaste końce zwracają `Prawda/Fałsz`.

```blocks3
    (() + ())

(połącz [witaj ] i [świecie])

<[] = []>
```

--- /collapse ---

--- task --- Znajdź w sekcji **Wyrażenia** blok `losuj liczbę od do`{:class="block3operators"} i podłącz go do bloku `obróć o`{:class="block3motion"} z sekcji **Ruch** klikając i przeciągając go w pole, w którym ustawiasz liczbę stopni.

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw styl obrotu na [lewo-prawo v]
    zawsze 
        przesuń o (10) kroków
+        obróć w prawo o (losuj liczbę od (1) do (10)) stopni
        czekaj (0.5) sekund
        jeżeli na brzegu, odbij się
    koniec
```

--- /task ---

**Uwaga**: możesz zmienić minimalną i maksymalną liczbę, z zakresu którego program wybierze losowo wartość, ale wartości domyślne (`1` i `10`) są całkiem dobre dla tej gry, więc możesz je po prostu zostawić.

--- task --- Kliknij zieloną flagę, aby uruchomić kod! --- /task ---

--- collapse ---
---
title: Co teraz robi blok pętli zawsze?
---

Blok pętli zawsze sprawia, że duszek ryby robi cztery rzeczy w kolejności:

1. Ruch do przodu
2. Obróć się trochę
3. Poczekaj chwilę
4. Sprawdź, czy jest na skraju sceny

Gdy duszek dokona sprawdzenia, zacznie na początku pętli i będzie się poruszał, obracał, czekał i sprawdzał tak długo, jak długo uruchomiony będzie Twój program Scratch.

--- /collapse ---

Fajnie! Dalej: łap tą rybę!