## Pêche!

Le requin bouge, le poisson nage, mais ils n'interagissent pas: si le poisson nage directement dans la bouche du requin, rien ne se passe. Il est temps de changer ça!

Tout d'abord, tu dois savoir si le poisson touche le requin. Pour cela, tu auras besoin d'un bloc **Contrôle** et d'un bloc **Détection**.

\--- task \--- Ajoute le `si ....alors`{: class = "block3control"} **Contrôle** bloc dans la boucle `répéter indéfiniment`{:class="block3control"} du poisson sprite, en dessous du bloc `si rebond`{: class = "block3motion"}.

Fais glisser le bloc `touchant ...`{:class="block3sensing"} dans l'espace situé en haut du bloc `si ... alors`{:class="block3control"}, puis clique sur le petit triangle pour sélectionner le nom du sprite requin. Si tu ne l'as pas changé, ce sera «Sprite1».

```blocks3
    lorsque le drapeau vert est cliqué
    définir style de rotation [gauche-droite v]
    répéter indéfiniment 
        déplacer de (10) pas
        tourner cw (choix aléatoire (1) à (10)) degrés
        attendre (0,5) secondes
        si sur le bord, rebondir
+ si <touching [Sprite1 v] ?> alors
    fin
```

\--- /task \---

## \--- collapse \---

## title: Comment ça marche?

Le `si ... alors`{:class="block3control"} **le bloc de contrôle** doit recevoir une valeur `Vraie/Fausse`.

**Les blocs de détection** collectent des informations, telles que l'emplacement du sprite, ce qui touche, etc. Tu utilises ce bloc:

```blocks3
    <touching [Sprite1 v] ?>
```

A partir de ce bloc, tu peux dire qu'il va te donner la valeur `Vrai/Faux` dont a besoin le bloc `si ... alors`{: class = "block3control"}.

\--- /collapse \---

Bien sûr, tu viens d'ajouter un bloc `si ... alors`{:class="block3control"} sans rien ajouter pour la partie 'alors'. Donc, au moment où ton script vérifie si le sprite poisson touche le sprite requin, il ne fait rien en réponse.

Tu peux faire disparaître le poisson, comme si le requin le mangeait, en utilisant le bloc `cacher`{:class="block3looks"}.

\--- task \--- Recherche le bloc `cacher`{: class = "block3looks"} dans la liste **Apparence** et place-le dans le bloc `si ... alors`{:class="block3control"} , ainsi:

```blocks3
    si <touching [Sprite1 v] ?> alors
+ cacher
    fin
```

\--- /task \---

Maintenant, une fois que le requin attrape le poisson, celui-ci disparaît définitivement. C'est pas génial.

\--- task \--- Mets le bloc `montrer`{:class="block3looks"} à partir de **Apparence** dans le tout début du code de poisson, pour pouvoir réinitialiser le jeu.

```blocks3
    lorsque le drapeau vert est cliqué
+ afficher
    définir style de rotation [gauche-droite v]
    répéter indéfiniment
```

\--- /task \---

C'est déjà mieux, mais tu ne veux pas que le joueur redémarre le jeu à chaque fois qu'il attrape un seul poisson!

\--- task \--- Met à jour le code dans ton bloc `si ... alors`{:class="block3control"} pour qu'il ressemble à ceci:

```blocks3
    si sur le bord, rebondir
    si <touching [Sprite1 v] ?> alors
        cacher
+ attendre (1) secondes
+ aller à x: (choisir au hasard (-240) à (240)) y: (choisir au hasard (-180) à (180))
+ montrer
    fin
```

\--- /task \---

## \--- collapse \---

## title: Comment ça marche?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!