## Vissen!

De haai beweegt, de vis zwemt, maar ze reageren niet op elkaar: als de vis in de bek van de haai zwemt, gebeurt er niets. Hoog tijd om dat te veranderen!

Eerst moet je weten of de vis de haai aanraakt. Hiervoor heb je een **Besturen** blok en een **Waarnemen** blok nodig.

\--- task \--- Voeg het `als...dan`{:class="block3control"} **Besturen** blok toe aan de `herhaal`{:class="block3control"} lus van de vis sprite, onder het `keer om aan de rand`{:class="block3motion"} blok.

Sleep het `raak ik`{:class="block3sensing"} blok boven in het vlakje van het `als...dan`{;class="block3control"} blok, en klik op het kleine driehoekje om de naam van de haai sprite te selecteren. Als je die naam niet verandert hebt, zal dat 'Sprite1' zijn.

```blocks3
    wanneer op de groene vlag wordt geklikt
maak draaistijl [links-rechts v]
herhaal
neem (10) stappen
draai cw (willekeurig getal tussen (1) en (10)) graden
wacht (0.5) sec
keer om aan de rand
+ als <touching [Sprite1 v] ?> dan
einde
```

\--- /task \---

## \--- collapse \---

## title: Hoe werkt het?

Het `als...dan`{:class="block3control"} **Besturen** blok heeft een `Waar/Niet waar` waarde nodig.

**Waarnemen** blokken verzamelen informatie, zoals waar de sprite is, wat hij aanraakt, etc. Je gebruikt dit blok:

```blocks3
    <raak ik [Sprite1 v]>
```

Door de puntige hoeken van dit blok, weet je dat het je een `Waar/Niet waar` waarde zal geven dat het `als...dan`{:class="block3control"} blok nodig heeft.

\--- /collapse \---

Uiteraard heb je net een `als...dan`{:class="block3control"} blok toegevoegd zonder iets voor het 'dan' gedeelte te zetten. Dus nu controleert je code of de vis de haai aanraakt, maar gebeurt er verder helemaal niets.

Je kunt de vis laten verdwijnen, alsof de haai hem heeft opgegeten, door het `verdwijn`{:class="block3looks"} blok te gebruiken.

\--- task \--- Zoek het `verdwijn`{:class="block3looks"} blok in **Uiterlijken** en zet het in het `als...dan` blok{:class="block3control"} blok:

```blocks3
    als <touching [Sprite1 v] ?> dan
+ verdwijn
einde
```

\--- /task \---

Als de haai nu de vis pakt, verdwijnt de vis definitief. Dat is niet zo mooi.

\--- task \--- Zet het `verschijn`{:class="block3looks"} blok uit **Uiterlijken** helemaal aan het begin van de vis code, zodat je het spel kunt hervatten.

```blocks3
    wanneer op de groene vlag wordt geklikt
+ verschijn
maak draaistijl [links-rechts v]
herhaal
```

\--- /task \---

Dat is al beter, maar je wilt niet dat de speler het spel moet herstarten zodra er een vis is gevangen!

\--- task \--- Werk je code bij in het `als...dan`{:class="block3control"} blok om het er zo uit te laten zien:

```blocks3
    keer om aan de rand
als <touching [Sprite1 v] ?> dan
verdwijn
+ wacht (1) sec
+ ga naar x: (willekeurig getal tussen (-240) en (240)) y: (willekeurig getal tussen (-180) en (180))
+ verschijn
einde
```

\--- /task \---

## \--- collapse \---

## title: Hoe werkt dit?

Jij bent slim: als de vis verdwenen is, dan wacht hij, beweegt, en komt weer te voorschijn.

Het lijkt alsof er heel veel vissen verschijnen, maar het is slechts één sprite die beweegt!

\--- /collapse \---

Dat is pas een spel! Maar je hebt nog geen manier om de score bij te houden, of te winnen. Ook dat kun je oplossen - op de volgende kaart!