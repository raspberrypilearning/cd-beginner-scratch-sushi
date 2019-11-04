## Wszystkie duszki

Teraz masz rekina, którym możesz poruszać za pomocą klawiszy strzałek. Nieźle! Czas dodać rybę, którą by mógł złapać.

\--- task \---

Kliknij przycisk **Nowy duszek**, a na ekranie, który zostanie otwarty, wybierz rybę.

![The New sprite button](images/spritesNewFromLibrary.png)

Jeśli twoja ryba jest trochę duża w porównaniu z twoim rekinem, możesz użyć kontroli rozmiaru, aby oba duszki miały odpowiedni rozmiar!

![Sprite size control](images/sprites2.png)

Zmień liczbę w kontrolce rozmiaru, aby zwiększyć lub zmniejszyć duszka.

\--- /task \---

Świetnie! Później dodasz trochę kodu, aby ryby same się poruszały, bez pomocy gracza. Twój gracz będzie kierował rekinem i spróbuje złapać rybę.

## \--- collapse \---

## title: A co z rekinem poruszającym się wstecz?

Wygląda trochę śmiesznie, gdy rekin płynie do tyłu. Tak jak zwykle odwracasz się zamiast chodzić do tyłu, tak rekin również odwróciłby się, zamiast pływać do tyłu. Na szczęście dla Ciebie Scratch ma do tego blok!

Blok `ustaw kierunek na`{:class="block3motion"} pozwala wybrać kierunek, w który odwraca się twój duszek. Znajdziesz go w sekcji bloków **Ruch**. Możesz wpisać dowolną liczbę stopni, aby skierować duszka w dowolnym kierunku. \--- /collapse \---

\--- task \--- Chwyć kilka kopii bloku `ustaw kierunek na`{:class="block3motion"} z listy **Ruch** i połącz je z kodem Twojego rekina, tak jak poniżej:

```blocks3
    gdy klawisz [strzałka w lewo v] naciśnięty
+ ustaw kierunek na (-90)
    przesuń o (10) kroków
```

```blocks3
    gdy klawisz [strzałka w prawo v] naciśnięty
+ ustaw kierunek na (-90)
    przesuń o (10) kroków
```

\--- /task \---

\--- task \--- Zmień liczbę kroków w bloku `przesuń`{:class="block3motion"} z `-10` na `10`.

Jeśli spróbujesz przesunąć rekina teraz po dodaniu bloków `ustaw kierunek na`{:class="block3motion"}, możesz zauważyć coś dziwnego. Rekin może nie odwracać się tak jak powinien!

![Upside down shark](images/spritesUpsideDown.png)

\--- /task \---

## \--- collapse \---

## title: Dlaczego obraca się do góry nogami?

Problem polega na tym, że duszek rekina rozpoczął, tak jak wszystkie inne duszki, ze **stylem obrotu** ustawionym na "dookoła", a potrzebujesz go ze stylem obrotu "lewo-prawo".

Jak zwykle, jest do tego blok i znajduje się w sekcji **Ruch**!

\--- /collapse \---

\--- task \--- Look in the **Motion** category for the block `set rotation style`{:class="block3motion"}.

Add the block to your shark reset code from earlier, and set the rotation style to `left-right`{:class="block3motion"}, like this:

```blocks3
    when green flag clicked
+     set rotation style [left-right v]
    go to x: (0) y: (0)
```

\--- /task \---