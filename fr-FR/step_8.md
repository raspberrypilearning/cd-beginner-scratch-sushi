## Pêche!

Le requin bouge, le poisson nage, mais ils n'interagissent pas: si le poisson nage directement dans la bouche du requin, rien ne se passe. Il est temps de changer ça!

Tout d'abord, tu dois savoir si le poisson touche le requin. Pour cela, tu auras besoin d'un bloc **Contrôle** et d'un bloc **Détection**.

--- task ---

Ajoute le bloc `si ....alors`{:class="block3control"} **Contrôle** dans la boucle `répéter indéfiniment`{:class="block3control"} du poisson sprite, en dessous du bloc `si rebond`{:class="block3motion"}.

Fais glisser le bloc `touchant ...`{:class="block3sensing"} dans l'espace situé en haut du bloc `si ... alors`{:class="block3control"}, puis clique sur le petit triangle pour sélectionner le nom du sprite requin. Si tu ne l'as pas changé, ce sera « Sprite1 ».

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
+        if <touching [Sprite1 v] ?> then
    end
```

--- /task ---

--- collapse ---
---
title: Comment ça marche?
---

Le `si ... alors`{:class="block3control"} **le bloc de contrôle** doit recevoir une valeur `Vraie/Fausse`.

**Les blocs de détection** collectent des informations, telles que l'emplacement du sprite, ce qu'il touche, etc. Tu utilises ce bloc :

```blocks3
    <touching [Sprite1 v] ?>
```

A partir de ce bloc, tu peux dire qu'il va te donner la valeur `Vrai/Faux` dont a besoin le bloc `si ... alors`{: class = "block3control"}.

--- /collapse ---

Bien sûr, tu viens d'ajouter un bloc `si ... alors`{:class="block3control"} sans rien ajouter pour la partie 'alors'. Donc, au moment où ton script vérifie si le sprite poisson touche le sprite requin, il ne fait rien en réponse.

Tu peux faire disparaître le poisson, comme si le requin le mangeait, en utilisant le bloc `cacher`{:class="block3looks"}.

--- task ---

Recherche le bloc `cacher`{: class = "block3looks"} dans la liste **Apparence** et place-le dans le bloc `si ... alors`{:class="block3control"} , ainsi :

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

--- /task ---

Maintenant, une fois que le requin attrape le poisson, celui-ci disparaît définitivement. Ce n'est pas génial.

--- task ---

Mets le bloc `montrer`{:class="block3looks"} à partir de **Apparence** dans le tout début du code de poisson, pour pouvoir réinitialiser le jeu.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

--- /task ---

C'est déjà mieux, mais tu ne veux pas que le joueur redémarre le jeu à chaque fois qu'il attrape un seul poisson !

--- task ---

Mets à jour le code dans ton bloc `si ... alors`{:class="block3control"} pour qu'il ressemble à ceci :

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

--- /task ---

--- collapse ---
---
title: Comment ça marche?
---

Tu es malin ici : quand le poisson est caché, il attend, bouge et se montre à nouveau.

On dirait que beaucoup de poissons continuent à apparaître, mais c'est ce sprite qui se déplace !

--- /collapse ---

C'est un jeu ! Mais il n’y a encore aucun moyen de marquer des points ou de gagner. Tu peux également résoudre ce problème - sur la carte suivante !