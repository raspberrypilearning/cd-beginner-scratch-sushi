## Zapamiętywanie wyniku

Aby zapamiętać ile ryb złapie gracz, musisz gdzieś przechowywać wynik oraz musisz mieć sposób na zwiększenie go i zresetowanie wyniku po ponownym uruchomieniu gry.

Po pierwsze: zapisywanie wyniku!

--- task --- Przejdź do sekcji **Zmienne** i kliknij **Utwórz zmienną**.

![](images/catch5.png)

Wpisz `wynik` jako nazwę.

![](images/catch6.png)

Sprawdź nową zmienną!

![Zmienna wynik jest wyświetlana na scenie](images/scoreVariableStage.png) --- /task ---

--- collapse ---
---
title: Czym są zmienne?
---

Gdy chcesz zapisać lub przechować informacje w programie, używasz czegoś, co nazywa się **zmienną**. Pomyśl o tym jak o pudełku z etykietą: możesz w nim coś umieścić, sprawdzić, co w nim jest i zmienić to, co w nim jest. Znajdziesz zmienne w sekcji **Zmienne**, ale musisz je najpierw utworzyć, aby się tam pojawiły!

--- /collapse ---

Teraz musisz zaktualizować zmienną za każdym razem, gdy rekin zjada rybę, i resetować ją po ponownym uruchomieniu gry. Wykonanie obu jest całkiem proste:

--- task --- Z sekcji **Zmienne**, weź bloki `ustaw [moja zmienna v] na [0]`{:class="block3variables"} i `zmień [moja zmienna v] o [1]`{:class="block3variables"}. Kliknij małe strzałki w blokach, wybierz `wynik` z listy, a następnie umieść bloki w programie:

### Kod rekina

```blocks3
    kiedy kliknięto zieloną flagę
+    ustaw [wynik v] na [0]
    ustaw styl obrotu na [lewo-prawo v]
    idź do x: (0) y: (0)
```

### Kod dla ryb

```blocks3
    jeżeli <dotyka [rekin v]?> to
+        zmień [wynik v] o [1]
        ukryj
        czekaj (1) sekund
        Idź do x: (losuj liczbę od (-240) do (240)) y: (losuj liczbę od (-180) do (180))
        pokaż
    koniec
```

--- /task ---

Fajnie! Teraz masz wynik i wszystko.