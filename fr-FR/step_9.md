## Garder le score

Pour garder le score du nombre de poissons capturés par le joueur, tu as besoin d'un emplacement pour stocker le score, un moyen de l'ajouter et un moyen de le réinitialiser au redémarrage de la partie.

Premièrement : enregistrer le score!

--- task ---

Va dans la catégorie du bloc **Variables** et clique sur **Créer une Variable**.

![](images/catch5.png)

Entre `score` comme nom.

![](images/catch6.png)

Vérifie ta nouvelle variable !

![La variable Score est affichée sur la scène](images/scoreVariableStage.png)

--- /task ---

--- collapse ---
---
title: Que sont les variables?
---

Lorsque tu souhaites stocker des informations dans un programme, tu utilises quelque chose appelé **variable**. Penses-y comme à une boîte avec une étiquette: tu peux y insérer quelque chose, vérifier son contenu et en changer le contenu. Tu trouveras des variables dans la section **Variables** , mais tu dois d'abord les créer pour les afficher !

--- /collapse ---

Maintenant, tu dois mettre à jour la variable chaque fois que le requin mange un poisson et la réinitialiser au redémarrage du jeu. Faire les deux est assez facile :

--- task ---

Dans la section **Variables** , prend le `définir [ma variable v] à [0]`{:class="block3variables"} et `changez les bloc [ma variable v] par [1]`{:class="block3variables"}. Clique sur les petites flèches dans les blocs, choisis `score` dans la liste, puis insère les blocs dans ton programme :

### Code pour le requin

```blocks3
    when green flag clicked
+    set [score v] to [0]
    set rotation style [left-right v]
    go to x: (0) y: (0)
```

### Code pour le poisson

```blocks3
    if <touching [Sprite1 v] ?> then
+        change [score v] by [1]
        hide
        wait (1) secs
        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
        show
    end
```

--- /task ---

Cool ! Maintenant, tu as un score et tout.
