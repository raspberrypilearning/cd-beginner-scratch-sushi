## Złap rybę!

Rekin porusza się, ryba pływa, ale nie wchodzą w interakcję: jeśli ryba popłynie prosto w usta rekina, nic się nie stanie. Czas to zmienić!

Po pierwsze, musisz wiedzieć, czy ryba dotyka rekina. Do tego potrzebny jest blok z sekcji **Kontrola** i blok z sekcji **Czujniki**.

--- task --- Dodaj blok `jeżeli...to`{:class="block3control"} z sekcji **Kontrola** wewnątrz bloku pętli `zawsze`{:class="block3control"} dla duszka ryby, poniżej bloku `jeżeli na brzegu, odbij się`{:class="block3motion"}.

Przeciągnij blok `dotyka...`{:class="block3sensing"} do miejsca na górze bloku `jeżeli...to`{:class="block3control"} i kliknij mały trójkąt, aby wybrać nazwę duszka rekina. Jeśli go nie zmieniłaś, będzie to „rekin”.

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw styl obrotu [lewo-prawo v]
    zawsze 
        przesuń o (10) kroków
        obróć w prawo o (losuj liczbę od (1) do (10)) stopni
        czekaj (0.5) sekund
        jeżeli na brzegu, odbij się
+        jeżeli < dotyka [rekin v] ?> to
    koniec
```

--- /task ---

--- collapse ---
---
title: Jak to działa?
---

Blok `jeżeli... to`{:class="block3control"} w sekcji **Kontrola** musi mieć wartość `Prawda/Fałsz`.

Bloki z sekcji **Czujniki** zbierają informacje, np. gdzie jest duszek, czego dotyka, itp. Używasz tego bloku:

```blocks3
    < dotyka [rekin v] ?>
```

Na podstawie spiczastych końców tego bloku możesz stwierdzić, że zwróci ci on wartość `Prawda/Fałsz`, której potrzebuje blok `jeżeli... to`{:class="block3control"}.

--- /collapse ---

Oczywiście właśnie dodałeś blok `jeżeli...to `{:class="block3control"} bez dodawania czegokolwiek do części „to”. W tej chwili Twój skrypt sprawdza, czy duszek ryby dotyka duszka rekina, ale w rezultacie nic nie dzieje się.

Możesz sprawić, że ryba zniknie, jakby zjadł ją rekin, używając bloku `ukryj`{:class="block3looks"}.

--- task --- Znajdź blok `ukryj`{:class="block3looks"} w sekcji **Wygląd** i umieść go wewnątrz bloku `jeżeli...to`{:class="block3control"} w taki sposób:

```blocks3
    jeżeli < dotyka [rekin v] ?> to
+        ukryj
    koniec
```

--- /task ---

Teraz, gdy rekin złapie rybę, ryba znika na dobre. To nie do końca jest super.

--- task --- Umieść blok `pokaż`{:class="block3looks"} z sekcji **Wygląd** na samym początku kodu ryby, aby można było zresetować grę.

```blocks3
    kiedy kliknięto zieloną flagę
+    pokaż
    ustaw styl obrotu [lewo-prawo v]
    zawsze
```

--- /task ---

To już lepiej, ale nie chcesz, aby gracz musiał restartować grę za każdym razem, gdy złapie jedną rybę!

--- task --- Zaktualizuj kod wewnątrz bloku `jeżeli...to`{:class="block3control"}, aby wyglądał następująco:

```blocks3
    jeżeli na brzegu, odbij się
    jeżeli <dotyka [rekin v] ?> to 
        ukryj
+        czekaj (1) sekund
+        Idź do x: (losuj liczbę od (-240) do (240)) y: (losuj liczbę od (-180) do (180))
+        pokaż
    end
```

--- /task ---

--- collapse ---
---
title: Jak to działa?
---

Jesteś tutaj sprytna: gdy ryba jest ukryta, to czeka, porusza się, a następnie pojawia się ponownie.

Wygląda na to, że pojawia się wiele ryb, ale to ten jeden duszek się porusza!

--- /collapse ---

To jest gra! Ale nie ma jeszcze sposobu na zapisanie wyniku lub wygranej. Możesz to również naprawić - na następnej karcie!