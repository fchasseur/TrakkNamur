# Workshop ACMJ



## Planning de la semaine

* Jour 1
  * Accueil & répartition en 2 équipes \(jeu icebreaker\) 
  * Brainstorming \(Véro & Anne\) \(1/2 journée\)
  * Intro à la programmation \(A l'extérieur\)
  * Et/ou the hour of code : [https://studio.code.org/s/mc/stage/1/puzzle/1](https://studio.code.org/s/mc/stage/1/puzzle/1)
* Jour 2
  * Soudure microcontrolleur + led 
  * Assemblage breadboard & intro à l'electronique
  * Upload du premier sketch
* Jour 3
  * Découpe des boitiers à la laser
  * Assemblage des boitiers
  * Création d'un compte adafruit
    * io.adafruit.com 
* Jour 4
  * Customisation des boitiers
* Jour 5

  * Progra dashboard && IFTT en fonction des projets

  \*\*\*\*

## **Schema électronique**

![](../.gitbook/assets/image%20%2870%29.png)

![](../.gitbook/assets/image%20%2857%29.png)



## Comment connecter la boite au WIFI

Pour mettre en marche la boîte et mettre en action les différentes fonctionnalités que les enfants ont programmées, il faut tout d’abord connecter celle-ci au wifi. Une fois connectée, les fonctionnalités programmées par les participants se mettront en marche automatiquement.

1\) **Redémarrer la boîte** \(bouton latéral\) Au démarrage de la boite, la LED clignote en bleu. Cela signifie que la boîte cherche un réseau connu dans sa liste, auquel se connecter pour aller récupérer des informations et s’actioner en fonction de celles-ci. Si elle ne trouve pas de réseau, elle en crée un dénommé \[PRENOM\]\_AP \(où \[PRENOM\] est le prénom du participant\).

2\) **Ouvrez votre Smartphone, PC ou ma**c, ouvrez les préférences WIFI et connectez-vous à ce réseau wifi créé par la boîte \(PRENOM\_AP\).

![](../.gitbook/assets/image%20%2832%29.png)

 Une page internet s’ouvre automatiquement après quelques instants. 

![](../.gitbook/assets/image%20%2822%29.png)

3\) **Cliquez sur** **“Configure** **WIFI”.** Une autre page s’ouvre. 

![](../.gitbook/assets/image%20%2853%29.png)

4\) **Selectionnez le wifi de votre habitation** \(ici : ROBIN HOOD\) et entrez votre mot de passe dans la case “password”.Cliquez sur “Save”.  La boite redémarrera automatiquement et tentera de se connecter au WIFI de votre habitation. Si la connexion échoue, elle se remettra en mode “Bleu clignotant”. Si la connexion réussit, la LED restera éteinte.  Une fois connectée, la boîte est fonctionnelle et peut activer les fonctionnalités programmées par les enfants \(ex: LED qui s’allume selon la météo, mouvement en fonction des notifications facebook, etc.\)

## Pour aller plus loin…

Si vous désirez programmer d’autres fonctionnalités sur la boîte, vous aurez besoin de deux outils : IFTT et io.adafruit.com. Il s’agit des deux platformes sur lesquelles nous vous avions demandé de créer un identifiant durant le stage. IFTT permettra de récolter les informations \(ex: notifications facebook, météo, …\), de les connecter à io.adafruit.com. Cette plateforme sera connectée à la boîte et pourra la faire réagir \(ex: mouvement, LED qui s’allume, qui change de couleur, etc\).

## IFTT

 **Qu'est-ce que IFTTT ?** IFTTT, « If This Then That », est un outil d'automatisation de tâches sur le web, qui met en relation un peu plus de 300 différents « canaux » couramment utilisés sur internet \(voir l[iste ici](https://ifttt.com/channels)\). 

![](../.gitbook/assets/image%20%2851%29.png)

Il permet de générer une action sur un canal en fonction d'un élément « déclencheur » défini sur l'autre : « si une photo est partagée sur Facebook **\(If This\)**, alors elle est archivée sur Dropbox **\(Then That\).**

Elle permet par exemple de faire en sorte de :

* Partager sur son mur Facebook un post publié sur son blog Wordpress
* Archiver automatiquement des tweets ou des photos Instagram dans Evernote, à mesure qu'ils sont partagés sur les deux services
* Chaque fois qu'une photo est partager sur Facebook, celle-ci est partagée sur Picasa.

  **Dans notre cas** IFFT permet par exemple de :

* faire bouger le bras de la boîte quand on reçoit un e-mail
* faire s’allumer la LED en bleu quand il va faire mauvais le lendemain,
* ...

Le canal “That” \(appelé ACTION\) \(exemple d’action : “le nez s’allume en vert”\) qui sera utilisé pour la boite, est la plateforme “io.adafruit.com”.

En fonction des déclencheurs sélectionnés \(exemples : e-mail, notifications facebook, météo, etc\), il faudra ajouter des données au feed “action” \(exemple : la LED s’allume en bleu\). Ces données seront à rentrer dans la case “Data to save” et seront envoyées sous forme de code \(cf. plus bas “Commandes disponibles à mettre dans data to save”\).

![](../.gitbook/assets/image%20%2828%29.png)

\(ici, par exemple, l’action est “la led s’allume en bleu\)

Voici un petit tutoriel sur la création de "Recette" sur IFTT: [http://fr.slideshare.net/baptistesavarypro/tutoriel-ifttt](http://fr.slideshare.net/baptistesavarypro/tutoriel-ifttt)

## io.adafruit.com : Commandes disponibles

\(à mettre dans “data to Save”\)

**Pulse \(Le moteur fait des mouvements de va&vient\)** P\#_Nb_\#_Min_\#_Max_\#_Speed_\# → Exemple : **P\#3\#0\#180\#4** → 3 aller-retours de 0 à 180 degrés à la vitesse 4 Note : Min et max: valeurs entre 0 et 180

**Go** G\#Position\# → Exemple : **G\#100\#** → Aller à la position 100 Note : Position : Valeur entre 0 et 180

**Led** L\#Duration\#Rouge\#Vert\#Bleu\# → Exemple: **L\#100\#255\#0\#0\#** → Allumer la led en rouge pendant 10 secs \(100 \* 1/10 sec\) Note : Rouge, Vert et bleu : Valeurs entre 0 et 255

**Rainbow** R\# → Exemple: **R\#** → Afficher le mode “arc-en-ciel”

**Sleep** S\# → **S\#** → Mettre en veille de longue durée. !! Attention, contrairement au schéma electronique, le bouton doit être raccordé entre le RST et le GND pour réveiller la boite !!

## Exemple

Comment faire pour faire en sorte de faire allumer la led mode arc-en-ciel lorsque je reçois un email de jil sur gmail.

1. Se connecter à IFTT
2. Cliquer sur “My Recipes” puis sur “Create RECIPE”
3. Cliquer sur “This”
4. taper “gmail” dans la barre de recherche des “channels”
5. Cliquer sur “connect” et authoriser l’accès à votre compte gmail à IFTT
6. Cliquer sur “DONE” puis sur “Continue to the next Step”
7. Dans “Choose a trigger”, cliquer sur “New email in inbox from”
8. Entrer l’adresse de jil dans la case email address.Puis cliquer sur “Save”
9. Cliquer sur That puis cliquer sur “adafruit” 
10. Cliquer sur “Send data to Adafruit IO”
11. Selectionner “Action” dans la section “Feed name”
12. Entrer “R\#” dans la section “Data to save”
13. Cliquer sur “Create Action”
14. Cliquer sur “Create Recipe”

Dès qu'un mail de jil arrivera dans ma boite mail, la led de ma boite s'allumera en bleu!

## Pour aller BEAUCOUP plus loin...

Voici :

* [le code source](https://drive.google.com/folderview?id=0B-j1CyUhWkIaRlZiN3hKcEVJU3M&usp=sharing) de la boite, à compiler avec Arduino V1.6.9, en ajoutant l'ESP8266 dans le board manager \([http://arduino.esp8266.com/versions/2.2.0/package\_esp8266com\_index.json](http://arduino.esp8266.com/versions/2.2.0/package_esp8266com_index.json)\)
* [Le design de la boite](https://drive.google.com/file/d/0B-j1CyUhWkIaQkFYZ040U0hkWjg/view?usp=sharing) 
* Le BOM: 
  * 1 [Huzzah Feather ESP8266](http://www.mouser.be/Search/ProductDetail.aspx?R=2821virtualkey54850000virtualkey485-2821)
  * 1 [Breadboard](http://www.mouser.be/Search/ProductDetail.aspx?R=BB400Tvirtualkey57130000virtualkey854-BB400T)
  * 1 [MicroServo](http://www.mouser.be/Search/ProductDetail.aspx?R=169virtualkey54950000virtualkey485-169)
  * 1 [PushButton](http://www.mouser.be/Search/ProductDetail.aspx?R=30-100virtualkey58730000virtualkey706-30-100) 
  * 1 [neoPixel](http://www.mouser.be/Search/ProductDetail.aspx?R=1312virtualkey54950000virtualkey485-1312) 
  * Du fil de toutes les couleurs

## Licence d'utilisation

![](../.gitbook/assets/image%20%2846%29.png)

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

