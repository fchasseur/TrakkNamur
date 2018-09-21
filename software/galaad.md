# Galaad

## Comment utiliser Galaad? 

 Galaad est le logiciel qui pilote la [+CNC](https://paper.dropbox.com/doc/mjqjcTxSBkEr5s9zb7SP0). Le manuel complet se trouve ici : [http://www.galaad.net/Galaad-Fra.pdf](http://www.galaad.net/Galaad-Fra.pdf)Il est téléchargeable gratuitement ici : [http://www.galaad.net/download-fra.html](http://www.galaad.net/download-fra.html)Il y a également un petit tuto sur l'installation de [+galaad sur un mac ici.](https://paper.dropbox.com/doc/zPO2BssdD0HMiYoXZlvLO) Alternativement, il est possible [+Utiliser Fusion360 avec la CNC de Trakk](https://paper.dropbox.com/doc/XCIaHpuHyK7ui8p06Ya1U)

## Interface

  La fenêtre de travail se divise en cinq zones distinctes : 

 ![](https://hackpad-attachments.imgix.net/hackpad.com_W2FyB658rNH_p.329185_1428396300685_undefined?fit=max&w=882)

![](../.gitbook/assets/image%20%2839%29.png)



* - Au centre, votre planche à dessin. Réceptacle de votre génie créatif mené à sa quintessence graphique, elle se tient prête à être envoyée directement à la machine pour un usinage sans histoire. Bref, c'est dans cette zone que vous allez exacerber vos talents artistiques avec la modeste contribution technique de Galaad. 
*  - Tout en haut, la classique barre de menus. Elle vous donne accès aux fonctions de manipulation globale et de supervision de votre travail, classées par type de fonctionnalité. Rien de bien original. Même dans l'hémisphère sud, la barre de menus est en haut, paraît-il. 
* - Juste au dessous, la non moins classique barre de commandes rapides. Chaque icone ici présente est un raccourci pour accéder à une fonction d'un sous-menu, sans passer par la fastidieuse ouverture dudit. Pour donner dans le genre non-conformiste propre à Galaad, quelques icones sous-jacentes ont été ajoutées.
*  - Sur la gauche de l'appareil, les icones de dessin. Vous trouverez là de quoi stimuler votre créativité, pour peu qu'elle manque d’additifs effervescents, et par conséquent de quoi former les objets composant votre dessin. Lorsque la souris passe sur les icones de base, un sous-groupe associé jaillit aussitôt pour affiner le choix. 
*  - Reléguée tout en bas, enfin, la zone d'affichage. Un vrai marché aux puces où l'on trouve pêle-mêle toutes les informations possibles et plus ou moins utiles sur ce qui se passe dans le dessin à un moment donné, c'est à dire principalement des cotes, dimensions et angles. 

## Démarrer un nouveau projet

**Définir la planche :** CTRL + N --&gt; et on donne les dimensions de la planche qui sera usinée

![](../.gitbook/assets/image%20%2818%29.png)



 On détermine ensuite les valeurs par defaut qui seront utilisées pour l'usinage. 

![](../.gitbook/assets/image%20%2877%29.png)

## **Design**

Galaad  travaille en vectoriel et importe sans soucis le format DXF. Inkscape, Illustrator, AutoCad,... peut exporter en DXF sans soucis.Il a été montré que Galaad peut également importer des fichier DWG 2000.Alternativement, il est possible de dessiner directement dans galaad.   

### **Définition de la stratégie d'usinage**

Par défaut, la fraise usine à la profondeur déterminée par défaut, son centre, se déplaçant le long de chaque trait. ContournageIl est cependant possible \(et heureusement\) de définir la compensation d'outils : la fraise se déplace alors de facon tangentiel, à l'intérieur ou à l'extérieur du trait : 

![](../.gitbook/assets/image%20%2859%29.png)

Pour cela, sélectionner le trait, cliquer sur l'icone "contournage" et déterminer si l'outil passe à l'intérieur ou à l'extérieur.

### Profondeur ****

Il est également possible de définir une profondeur d'usinage différente pour les traits selectionnés



![](../.gitbook/assets/image%20%2861%29.png)

###  Hachurage

![](../.gitbook/assets/image%20%283%29.png)

## Usinage

### **Paramètre d'usinage**

Il est toujours bon de faire une simulation avant de démarrer.  \(Menu usinage/ Simulation fraisage 3 Axes\)Déterminer[ les vitesses d'avance et les paliers de profondeur](../tools/cnc.md#vitesse-davance-et-vitesse-de-coupe).

![](../.gitbook/assets/image%20%2816%29.png)

### **Origine** 

La page de paramètres d'usinage disparaît pour laisser place à la page de réglage de l'origine pièce, non moins fournie en zones de contrôle  Le dialogue entre votre logiciel préféré et votre commande numérique s'ouvre dès validation du message de présentation d'outil. Cette première ouverture peut parfois durer quelques longues secondes.

![](../.gitbook/assets/image%20%2872%29.png)

  Il s'agit maintenant d'indiquer à Galaad où se trouve la pièce à usiner sur le plateau de votre machine.  Il n'en connaît que les dimensions et les tracés à usiner. Il va donc falloir lui donner un point de référence XYZ et préciser où se trouve la pièce par rapport à ce point. 

![](../.gitbook/assets/image%20%2814%29.png)

\(En gris la table de la CNC, en blanc, la planche et en noir sur la planche le trajet de l'outil\)  La position de l'origine pièce a été validée pour les trois axes \(par les boutons 'X Ok', 'Y Ok', 'Z Ok'\) Galaad sait maintenant tout ce qu'il voulait savoir, c'est à dire où se trouve le point origine, et où se trouve votre pièce par rapport à ce point. Vous pouvez cliquer sur le gros bouton jaune de "Lancement de l'usinage".



## Usinage 3D avec  Fusion 360 et KAY

Afin de piloter la CNC en 3D, vous devrez dessiner votre pièce en Fusion360 et paramétrer l'usinage dans le module CAM de Fusion360. Lorsque vous êtes satisfait de la simulation d'usinage, il faut transférer le fichier d'usinage sur le PC de la CNC. Pour cela, dans Fusion360, vous devez choisir le post processeur "acurite millpwr 3.cps". Sauver le fichier \(extension .nc\) sur une clé USB pour le transférer sur le PC de la CNC. Sur le PC de la CNC, ouvrir le module KAY de Galaad et ouvrir votre fichier ".nc". Il faut ensuite déterminer les origines en x, y et z de votre matériau et lancer l'usinage.Merci le [makilab](https://wiki.makilab.org/index.php/CNC)!



