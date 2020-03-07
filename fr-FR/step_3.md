## Ajout et suppression de blocs de code

Génial! Tu as écrit ton tout premier programme Scratch. Il est temps d'en apprendre un peu plus sur l'introduction et la suppression de code dans Scratch! Le code Scratch est composé de **blocs** tels que:

![](images/code1.png)

Tu trouveras tous les blocs dans la **palette des blocs de code**, classés en différentes catégories en fonction de ce qu'ils font.

## \--- collapse \---

## title: Utilisation de blocs de différentes catégories

Clique sur un nom de catégorie pour voir les blocs de cette catégorie. Ici, la catégorie **Mouvement** est sélectionnée :

![](images/code2a.png)

Tous les blocs de la catégorie sur laquelle tu as cliqué sont affichés dans une liste :

![](images/code2b.png)

Tu peux cliquer sur le bloc que tu cherches, puis le faire glisser dans le panneau du sprite actuel, puis lâcher le bouton de la souris. Une fois que le bloc est dans le panneau, tu peux le déplacer et le relier à d'autres blocs.

\--- /collapse \---

Si tu veux voir ce que fait un bloc, tu peux double-cliquer dessus pour le faire exécuter!

\--- task \---

Essaie de double-cliquer sur certains blocs pour voir ce qu’ils font.

\--- /task \---

## \--- collapse \---

## title: Exécuter le code

Généralement, tu veux que ton code soit exécuté automatiquement chaque fois que quelque chose de spécifique se produit. C’est pourquoi beaucoup de tes programmes commenceront avec un bloc de la catégorie **Événements**, le plus souvent celui-ci :

```blocks3
    quand le drapeau vert est cliqué
```

Les blocs de code reliés à ce bloc seront exécutés après que le **drapeau vert** sera cliqué.

Les blocs de code vont du haut vers le bas. L'ordre dans lequel tu assembles tes blocs est donc important. Dans cet exemple, le sprite `dira`{:class = "block3looks"} `Bonjour!` avant de `jouer`{:class = "block3sound"} le son `Meow`.

```blocks3
    quand le drapeau vert est cliqué
    dire [Bonjour]
    jouer le son [Meow v]
```

\--- /collapse \---

Il est facile d'enlever ou de supprimer des blocs de code que tu ne veux pas dans ton programme ! Fais-les simplement glisser dans la palette des blocs de code.

**Fais attention:** si tu fais glisser un bloc de code dans la palette des blocs de code, cela supprimera tous les blocs reliés au bloc que tu fais glisser. Veille donc à séparer les blocs de code que tu souhaites conserver de ceux que tu souhaites enlever. Si tu supprimes des blocs de code par accident et que tu souhaites les récupérer, clique avec le bouton droit de la souris, puis clique sur **Restaurer** pour tout récupérer.

![](images/code6.png)

\--- task \---

Essaie d'ajouter, de supprimer, et d'annuler la suppression de certains blocs de code !

\--- /task \---

### Les assembler

Maintenant que tu sais comment déplacer le code et faire bouger les choses, il est temps de créer un programme pour faire en sorte que le chat Scratch marche en cercle !

\--- task \---

Assure-toi que le sprite chat est sélectionné dans la liste, puis fais glisser les blocs suivants dans le panneau sprite et relie-les. Tu les trouveras dans les listes **Événements** et **Mouvement**.

```blocks3
    quand le drapeau vert est cliqué
    avancer de [10] pas
```

\--- /task \---

\--- task \---

Maintenant, clique sur le drapeau vert au-dessus de la scène.

![](images/code7.png)

\--- /task \---

Tu devrais voir le chat marcher en ligne droite ... pas exactement ce que tu veux, exact ?

Remarque: si tu cliques trop souvent sur le drapeau et que le chat s'éloigne, tu peux le faire glisser !

\--- task \---

Accroche le bloc tourner à la fin pour faire marcher le sprite du chat en cercle. C'est aussi dans la liste **Mouvement**.

```blocks3
    lorsque le drapeau vert est cliqué 
    déplacez de [10] pas
+ tournez cw (15) degrés
```

\--- /task \---

## \--- collapse \---

## title: Comment fonctionne la rotation?

Ce bloc fait tourner le sprite de 15 degrés sur 360 degrés complets qui forment un cercle. Tu peux modifier ce nombre et le nombre de pas en cliquant dessus et en saisissant une nouvelle valeur.

![](images/code9.png)

\--- /collapse \---

\--- task \---

Maintenant, enregistre ton travail !

\--- /task \---