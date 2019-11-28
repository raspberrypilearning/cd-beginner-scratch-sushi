## Poisson télécommandé

D'accord, il est maintenant temps de faire nager le poisson tout seul. Pour ce faire, tu auras besoin d’un nouveau type de bloc: un bloc **Contrôle**.

\--- task \--- Sélectionne ton sprite poisson.

Fais glisser un bloc `lorsque le drapeau vert est cliqué`{:class="block3events"} **Événement**, un bloc `répéter indéfiniment`{: class = "block3control"} **Contrôle**, et un bloc `déplacement de 10 pas`{:class="block3motion"} **Mouvement** dans le **panneau sprite**, comme ceci:

```blocks3
    lorsque le drapeau vert est cliqué sur
    répéter indéfiniment
        déplacer de (10) pas
    fin
```

\--- /task \---

## \--- collapse \---

## title: que fait le nouveau bloc?

**Les blocs de contrôle** obligent ton programme à effectuer des tâches un certain nombre de fois ou dans certaines conditions.

Ici, le poisson fait ce qui est dans le bloc `répéter indéfiniment`{:class="block3control"} encore et encore sur une boucle, pour toujours. Ainsi, une fois la dernière chose (bloc) passée dans le bloc `répéter indéfiniment`{:class="block3control"}, il recommence en haut et fait de nouveau tout, et ainsi de suite.

\--- /collapse \---

\--- task \--- Maintenant, clique sur le drapeau vert et regarde ce qui se passe! \--- /task \---

Eh bien, ce poisson vient de s'écraser sur le côté de la scène et il se déplaçait beaucoup trop vite pour que ton requin puisse l'attraper.

Tout d'abord, tu dois ralentir le poisson. C'est en fait assez facile, tu as juste besoin d'attendre un peu après avoir bougé ces 10 pas. Il y a un bloc **Contrôle** qui t'aideras ici:

```blocks3
    attendre (1) secondes
```

\--- task \--- Ajoute le bloc `attendre`{:class="block3control"} dans ton code à l'intérieur du bloc `répétez indéfiniment`{:class="block3control"} et modifie le nombre à `0.5`, comme ceci:

```blocks3
    lorsque le drapeau vert est cliqué 
    répéter indéfiniment
        déplacer de (10) pas
+ attendre (0,5) secondes
    fin
```

\--- /task \---

## \--- collapse \---

## title: faire des ajustements

Le numéro que tu définis dans le bloc `attendre`{:class="block3control"} dit combien de **secondes** tu veux que le poisson attende. `0.5` est une demi-seconde.

Tu peux tester différentes valeurs pour déterminer laquelle est la meilleure pour le jeu. Et rappelles-toi que tu peux également modifier le nombre de pas dans le bloc `déplacer`{:class="block3motion"}!

\--- /collapse \---

Le poisson bouge maintenant, mais tu en as aussi besoin pour rebondir sur le bord de la scène. Encore une fois, il y a un bloc **Mouvement** pour cela!

\--- task \--- Recherche le bloc `si rebondi sur le bord`{:class="block3motion"} et ajoute-le après le bloc `attendre`{: class="block3control"}. \--- /task \---

## \--- collapse \---

## title: que fait le nouveau bloc?

Le bloc `si rebondi sur le bord`{:class="block3motion"} vérifie si le sprite touche le bord de la scène et, le cas échéant, il tourne à gauche, à droite, en haut ou en bas, selon le cas.

\--- /collapse \---

Bien sûr, cela conduira à un poisson à l'envers, tu as donc besoin de nouveau d'un bloc `définir style de rotation`{:class="block3motion"}.

\--- task \--- Mets à jour ton code pour définir le style de rotation du poisson sur `gauche-droite`{:class="block3motion"} au début du script du sprite:

```blocks3
    lorsque le drapeau vert est cliqué 
+ définir le style de rotation [gauche-droite v]
    répéter indéfiniment
        déplacer de (10) pas
        attendre (0.5) secs
        si sur le bord, rebondir
    fin
```

\--- /task \---

Le poisson se déplace maintenant en avant et en arrière, mais uniquement en ligne droite - un peu trop facile à attraper pour le joueur avec le requin! Tu dois rendre le poisson moins prévisible.

Tu sais déjà depuis une étape précédente comment faire un sprite qui tourne, alors démarre là.

\--- task \--- Ajoute un tournant dans les instructions de nage du poisson et clique sur le drapeau vert.

```blocks3
    lorsque le drapeau vert est cliqué 
    définir le style de rotation [gauche-droite v]
    répéter indéfiniment
        déplacer de (10) pas
+ tourner cw (10) degrés
        attendre (0.5) secs
        si sur le bord, rebondir
    fin
```

\--- /task \---

C'est mieux, mais il y a encore trop de tendance. Cela doit être plus aléatoire. Heureusement, Scratch peut faire du hasard pour vous! Tu as juste besoin d'un nouveau type de bloc, appelé bloc **opérateur**.

## \--- collapse \---

## title: Qu'est-ce qu'un opérateur?

**Les opérateurs** saisissent une ou plusieurs valeurs (telles que des nombres, du texte ou `valeurs Vrai/Faux` ) et renvoient une valeur unique. Tu peux déterminer le type de valeur qu’elle rendra par la forme du bloc: arrondi donne des chiffres ou du texte, pointu donne `vrai/faux`.

```blocks3
    (() + ())

    (rejoindre [bonjour] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \--- Trouve le bloc `choix aléatoire`{:class="block3operators"} bloc **opérateur** et branche-le dans le bloc `tourner degrés`{: class = "block3motion"} **Mouvement** en cliquant et en le glissant dans le champ où tu définis le nombre de degrés.

```blocks3
    lorsque le drapeau vert est cliqué
    définir le style de rotation [gauche-droite v]
    répéter indéfiniment
        déplacer de (10) pas
+ tourner cw (choisir au hasard (1) à (10)) degrés
        attendre (0.5) secondes
        si sur le bord, rebondir
    fin
```

\--- /task \---

**Remarque**: tu peux modifier les nombres minimum et maximum qu’il choisira, mais les valeurs par défaut (`1` et `10`) sont plutôt bonnes pour ce jeu, tu peux donc les laisser.

\--- task \--- Clique sur le drapeau vert pour exécuter le code! \--- /task \---

## \--- collapse \---

## title: Alors, que fait maintenant le bloc répéter indéfiniment ?

Le bloc répéter indéfiniment oblige désormais le sprite poisson à faire quatre choses dans l'ordre:

1. Avancer
2. Tourner un peu
3. Attendre brièvement
4. Vérifier si c'est au bord de la scène

Une fois que le sprite a effectué la vérification, il recommence au début de la boucle et se déplace, tourne, attend, vérifie, tant que tu laisses ton programme Scratch s'exécuter.

\--- /collapse \---

Cool! Prochaine étape: attraper ce poisson!