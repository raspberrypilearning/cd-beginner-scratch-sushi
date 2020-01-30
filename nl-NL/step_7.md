## Vis op afstand bestuurbaar

Oké, hoog tijd om de vis zelfstandig te laten zwemmen. Hiervoor heb je een nieuw soort blok nodig: een **Besturen** blok.

\--- task \---

Selecteer je vis sprite.

Sleep een `wanneer op groene vlag wordt geklikt`{:class="block3events"} **Gebeurtenissen** blok, een `herhaal`{:class="block3control"} **Besturen** blok en een `neem 10 stappen`{:class="block3motion"} **Beweging** blok naar het **sprite paneel**:

```blocks3
    wanneer op groene vlag wordt geklikt
herhaal
neem (10) stappen
einde
```

\--- /task \---

## \--- collapse \---

## title: Wat doet dit nieuwe blok?

**Besturen** blokken zorgen ervoor dat je programma dingen een bepaald aantal keren doet, of onder bepaalde omstandigheden.

Hier herhaalt de vis alles wat in het `herhaal`{:class="block3control"} blok staat voor eeuwig. Dus als het het laatste ding (blok) binnen het `herhaal`{:class="block3control"} heeft gedaan, begint hij bovenaan weer helemaal op nieuw, en blijft dat herhalen.

\--- /collapse \---

\--- task \---

Klik nu op de groene vlag en kijk wat er gebeurt!

\--- /task \---

Tjonge, die vis botste tegen de zijkant van het Speelveld en ging véél te snel voor je haai.

Eerst moet je de vis langzamer laten gaan. Dat is vrij simpel, je moet een pauze inlassen als de vis 10 stappen genomen heeft. Er is een **Besturen** blok dat je hierbij helpt:

```blocks3
    wacht (1) sec
```

\--- task \---

Voeg het `wacht`{:class="block3control"} blok toe aan je code binnen het `herhaal`{:class="block3control"} blok, en verander het getal naar `0.5`:

```blocks3
    wanneer op groene vlag wordt geklikt
herhaal
neem (10) stappen
+ wacht (0.5) sec
einde
```

\--- /task \---

## \--- collapse \---

## title: Aanpassingen maken

Het getal dat je ingevoerd hebt in het `wacht`{:class="block3control"} blok vertelt hoeveel **seconden** jij wilt dat de vis moet wachten. `0.5` is een halve seconde.

Je kunt verschillende getallen invoeren om uit te zoeken wat het beste bij het spel past. En onthoud dat je het aantal stappen binnen het `neem stappen`{:class="block3motion"} blok ook kunt veranderen!

\--- /collapse \---

De vis beweegt nu, maar je wilt ook dat hij omdraait aan de rand van het Speelveld. Ook hier is een **Beweging** blok voor!

\--- task \---

Zoek het `keer om aan de rand`{:class="block3motion"} blok en zet het onder het `wacht`{:class="block3control"} blok.

\--- /task \---

## \--- collapse \---

## title: Wat doet dit nieuwe blok?

Het `keer om aan de rand`{:class="block3motion"} blok controleert of de sprite de rand van het Speelveld raakt, en zo ja, zorgt dat de sprite al naar gelang naar links, rechts, boven of beneden draait.

\--- /collapse \---

Natuurlijk betekent dit dat je vis ondersteboven gaat zwemmen, dus heb je weer een `maak draaistijl`{:class="block3motion"} nodig.

\--- task \---

Werk je code bij door de draaistijl van de vis `links-rechts`{:class="block3motion"} aan het begin van de sprite code toe te voegen:

```blocks3
    wanneer op groene vlag wordt geklikt
+ maak draaistijl [links-rechts v]
herhaal
neem (10) stappen
wacht (0.5) sec
keer om aan de rand
einde
```

\--- /task \---

De vis beweegt nu vooruit en achteruit, maar alleen in een rechte lijn - de speler kan nu met de haai wel heel makkelijk de vis pakken! Je moet de vis minder voorspelbaar maken.

Je weet van een vorige stap al hoe je een sprite kunt laten draaien, dus daar begin je mee.

\--- task \---

Voeg een draai toe aan de zweminstructies van de vis, en klik op de groene vlag.

```blocks3
    wanneer op groene vlag wordt geklikt
maak draaistijl [links-rechts v]
herhaal
neem (10) stappen
+ draai cw (10) graden
wacht (0.5) sec
keer om aan de rand
einde
```

\--- /task \---

Al beter, maar nog steeds te voorspelbaar. Het moet willekeuriger worden. Gelukkig kan Scratch willekeurig voor je uitvoeren! Je hebt een nieuw blok nodig, een **functie** blok.

## \--- collapse \---

## title: Wat is een functie?

**Functies** nemen één of meer waarden (zoals getallen, tekst, of `Waar/Niet waar` waarden) en geven daar een enkele waarde voor terug. Je kunt zien wat voor waarde het terug zal geven door de vorm van het blok: afgeronde blokken geven getallen of tekst, puntige blokken geven `Waar/Niet waar`.

```blocks3
    (() + ())

(voeg [hallo ] en [wereld] samen)

<[] = []>
```

\--- /collapse \---

\--- task \---

Zoek het `willekeurig getal tussen`{:class=block3operators"] **Functies** blok, en stop het in het `draai graden`{:class="block3motion"} **Beweging** blok door erop te klikken en het in het getalvakje van de graden te slepen.

```blocks3
    wanneer op groene vlag wordt gedrukt
maak draaistijl [links-rechts v]
herhaal
neem (10) stappen
+ draai cw (willekeurig getal tussen (1) en (10)) graden
wacht (0.5) sec
keer om aan de rand
einde
```

\--- /task \---

**Let op**: je kan het laagste en hoogste getal veranderen dat gekozen moet worden, maar de standaard waarden (`1` en `10`) zijn zeer geschikt voor dit spel, dus je mag ze ook laten staan.

\--- task \---

Klik op de groene vlag om de code uit te voeren!

\--- /task \---

## \--- collapse \---

## title: Dus wat doet het herhaalblok nu?

Het herhaalblok laat de vis vier dingen in deze volgorde doen:

1. Beweeg vooruit
2. Draai een beetje
3. Wacht even
4. Controleer of het aan de rand van het Speelveld is

Zodra de sprite de controle gedaan heeft, zal het, zolang je het Scratch programma uitvoert, weer teruggaan naar het begin van de lus en bewegen, draaien, wachten, controleren.

\--- /collapse \---

Gaaf! Volgende stap: pak die vis!