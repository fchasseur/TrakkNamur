# Mon scanneur à livre, version diy

Oui, grâce au [TRAKK](http://www.trakk.be/) et au [Makilab](https://makilab.org/) j'ai construit un bidule qui scanne les livres. Non, les pages ne tournent pas automatiquement.

![](../.gitbook/assets/image%20%281%29.png)

Je ne documenterai pas en détail toute la construction du scanneur, mais vous trouverez ici les grandes étapes du projet, les choix que j'ai fait. Une sorte de présentation générale.

## **1. Quel scanneur construire ?**

On peut distinguer deux grandes catégories de scanneur à livre : ceux qui tournent les pages automatiquement, et ceux qui nécessitent un opérateur chargé de tourner les pages. Pour faire simple, on parlera de scanneur automatique ou manuel. Chaque catégorie a bien-entendu ses avantages et inconvénients.

J'ai fait le choix de construire un scanneur manuel pour les raisons suivantes : — la simplicité : ça peut paraître débile, mais j'ai construit un scanneur à livre pour scanner des livres. Pas pour l’exploit. Pas pour m'occuper les jours de pluie. Le but est d'avoir un scanneur qui fonctionne bien, pas de construire un scanneur-fusée-lazer-IRM compliqué à réparer quand il casse. — la fiabilité : je peux scanner le livre quoi qu'il arrive ; même si les pages collent entre elles, même si une page est écornée ou pliée, même si le livre a tendance à se refermer. — la flexibilité : je veux scanner des livres. Des gros, des petits, des grands, des feuillets, des livres anciens, etc. En général, les scanneurs automatiques ont plus de mal à numériser des format « extraordinaires » ou des livres plus fragiles.

Le seul inconvénient du scanneur manuel, c'est qu'il n'est pas automatique \(_cap'tain obvious_\). Le tout c'est de relativiser :  
— numériser un livre est quoi qu'il arrive une opération lente et laborieuse. Après le scan, il reste le post-traitement, c'est-à-dire la création du fichier, le rognage des marges, l'OCR \(logiciel de reconnaissance des caractères\), la relecture, etc. Le post-traitement est la partie la plus longue en temps. Elle est nécessaire que l'on ait un scanneur automatique ou manuel. Le scanneur automatique ne résout donc pas tout ! — les scanneurs automatiques ne sont pas forcément plus rapides. — un scanneur automatique a de toute façon besoin de quelqu'un dans les parages pour surveiller le processus.

Ceci dit, il est fort probable, qu'une fois mon scanneur manuel terminé, je m'attaque à une version automatique. Je dois admettre avoir un faible pour [celui-ci](https://www.youtube.com/watch?v=1rbYpOiYEdA).

## **2.** _**The archivist**_ **la 2CV des scanneurs à livre.**

Un scanneur à livre manuel, ce n'est pas technologiquement très compliqué. Il s'agit d'un assemblage qui réunit : — un support pour le livre — deux appareils photos \(un pour la page de gauche, un pour la page de droite\) — un éclairage — un logiciel pour déclencher la capture d'image

Si ça peut paraître très simple, il y a déjà des dizaines de questions qui se posent : Comment maintenir le livre ouvert ? Selon quel angle ouvrir le livre ? Comment maintenir le livre face à l'appareil ? Quel appareil photo utiliser ? Comment le déclencher ? Quel éclairage utiliser ? Selon quel angle placer l'éclairage ? Comment éviter les reflets ? Etc.

Toutes ces questions ont été traitées pendant des années par toute la communauté du site [http://www.diybookscanner.org/forum/](http://www.diybookscanner.org/forum/). Daniel Reetz, membre du forum, a synthétisé toutes les solutions en concevant un modèle appelé [the archivist](http://www.diybookscanner.org/archivist/) . Ce modèle est en fait la 2CV des scanneurs à livre : efficace, simple à fabriquer, passe partout, facilement réparable, etc. C'est ce modèle que j'ai construit. Notons que le site archive.org a déjà numérisé des millions de livres avec un scanneur très proche et dérivé de _the archivist_ \([plus d'infos](https://archive.org/details/tabletopscribesystem)\).

## **3. La construction**

_to be continued…_ revenez plus tard, je peux pas continuer j'ai piscine.

![](../.gitbook/assets/image%20%2866%29.png)

![](../.gitbook/assets/image%20%285%29.png)

## **Pour aller plus loin**

Voici quelques liens pour approfondir le sujet, et pourquoi pas, construire toi aussi un scanneur à livre !

[http://www.diybookscanner.org/forum/](http://www.diybookscanner.org/forum/) C'est là que tout se passe. Ce forum \(en anglais\), réunit la communauté des constructeurs de scanneurs à livre. Chaque membre y publie ses avancées dans l'esprit open-source. On y trouves des modèles différents, des prototypes bizarres, des tutos, des idées, des solutions… La communauté n'est pas très large, mais tous sont passionnés et ravis de faire vivre le projet.

[http://www.diybookscanner.org/archivist/](http://www.diybookscanner.org/archivist/) C'est le site du scanneur _the archivist_. C'est le modèle que j'ai construit. Vous y trouverez toutes les informations détaillées pour assembler ce modèle.

[http://makezine.com/projects/make-41-tinkering-toys/diy-book-scanner/](http://makezine.com/projects/make-41-tinkering-toys/diy-book-scanner/) Pareil que le précédant mais légèrement simplifié pour être assemblé à partir de pièces plus faciles à se procurer.

[https://github.com/markvdb/diybookscanner](https://github.com/markvdb/diybookscanner) Un répertoire github, à nouveau pas mal d'infos et de petites variations autours du modèle _the archivist_.

[https://www.bookscanner.fr/](https://www.bookscanner.fr/) Le site d'un projet de scanneur à livre. Intéressant en guide d'introduction.

