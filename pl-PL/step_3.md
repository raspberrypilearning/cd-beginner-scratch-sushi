## Dodawanie i usuwanie bloków kodu

Świetnie! Napisałaś swój pierwszy program w Scratch. Czas dowiedzieć się nieco więcej o wprowadzaniu i usuwaniu kodu w Scratch! Kod w Scratch składa się z **bloków** takich jak te:

![](images/code1.png)

Znajdziesz tu wszystkie bloki w **palecie bloków kodu**, podzielone na różne kategorie w zależności od tego, co robią.

--- collapse ---
---
title: Używanie bloków z różnych kategorii
---

Kliknij na nazwę kategorii, aby zobaczyć bloki w tej kategorii. Tutaj wybrana jest kategoria **Ruch**:

![](images/code2a.png)

Wszystkie bloki w klikniętej kategorii są wyświetlane na liście:

![](images/code2b.png)

Możesz kliknąć dowolny blok, a następnie przeciągnąć go do panelu bieżącego duszka i upuścić go. Po umieszczeniu go w panelu możesz go przenosić i łączyć z innymi blokami.

--- /collapse ---

Jeśli chcesz zobaczyć, co robi blok, kliknij go dwukrotnie, aby go uruchomić!

--- task --- Spróbuj dwukrotnie kliknąć na niektóre bloki, aby zobaczyć, co robią. --- /task ---

--- collapse ---
---
title: Uruchamianie kodu
---

Zwykle chcesz, aby Twój kod uruchamiał się automatycznie, gdy wydarzy się coś konkretnego. Dlatego wiele z twoich programów rozpocznie się od bloku z kategorii **Zdarzenia**, najczęściej od tego:

```blocks3
    kiedy flaga kliknięta
```

Bloki kodu podłączone do tego bloku będą uruchamiane po kliknięciu **zielonej flagi**.

Bloki kodu uruchamiane są od góry do dołu, więc kolejność, w jakiej łączysz bloki, ma znaczenie. W tym przykładzie duszek `powie`{:class="block3looks"} `Witaj!` zanim `odtworzy`{:class="block3sound"} dźwięk `miau` (ang. meow).

```blocks3
    kiedy flaga kliknięta
    powiedz [Cześć]
    odtwarzaj dźwięk [meow v]
```

--- /collapse ---

Usuwanie bloków kodu, których nie chcesz w swoim programie, jest proste! Po prostu przeciągnij je z powrotem do palety bloków kodu.

**Bądź ostrożna:** przeciągając je do palety bloków kodu, usuniesz wszystkie bloki połączone z blokiem, który przeciągasz, więc upewnij się, że oddzielasz bloki kodu, które chcesz zachować, od bloków, które chcesz usunąć. Jeśli przez przypadek usuniesz niektóre bloki kodu i chcesz je odzyskać, kliknij prawym przyciskiem myszy, a następnie kliknij opcję **cofnij**, aby wszystko odzyskać.

![](images/code6.png)

--- task --- Spróbuj dodać, usunąć i przywrócić niektóre bloki kodu! --- /task ---

### Składanie wszystkiego w całość

Teraz, gdy wiesz, jak przesuwać kod i sprawiać, że coś się dzieje, nadszedł czas, aby stworzyć program, który spowoduje, że kot Scratch będzie chodził w kółko!

--- task --- Upewnij się, że na liście duszków został wybrany duszek kota, a następnie przeciągnij następujące bloki do panelu duszka i połącz je. Znajdziesz je na listach **Zdarzenia** i **Ruch**.

```blocks3
    kiedy flaga kliknięta
    przesuń o [10] kroków
```

--- /task ---

--- task --- Kliknij zieloną flagę nad sceną.

![](images/code7.png) --- /task ---

Powinnaś zobaczyć kota idącego w linii prostej... niezupełnie tego chciałaś, prawda?

Uwaga: Jeśli klikniesz flagę zbyt wiele razy, a kot odejdzie, możesz przeciągnąć go z powrotem!

--- task --- Przyczep na końcu blok skręcania, aby duszek kota chodził w kółko. Jest on także na liście **Ruch**.

```blocks3
    kiedy flaga kliknięta
    przesuń o [10] kroków
+ obróć cw o (15) stopni
```

--- /task ---

--- collapse ---
---
title: Jak działa obracanie?
---

Ten blok powoduje, że ikonka obraca się o 15 stopni (z pełnych 360 stopni tworzących okrąg). Możesz zmienić tę liczbę i liczbę kroków, klikając numer i wpisując nową wartość.

![](images/code9.png)

--- /collapse ---

--- task --- Teraz zapisz swoją pracę! --- /task ---