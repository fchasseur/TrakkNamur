# CNC

![CNC dans son habitat premier](../.gitbook/assets/image%20%2828%29.png)

Une CNC est composé d'un systeme de déplacement XYZ, d'une broche et d'un outils de coupe. Le logiciel qui la pilote s'appele KAY\( un module de [Galaad](../software/galaad.md)\). Alternativement, il est possible d'utiliser Fusion360

## **XYZ** 

Notre CNC a une surface de 1700mm sur 900 mm et une surface usinable de 1400mm sur 800mm.  

## **Broche**

La broche Kress est une broche à vitesse variable de 5000 à 21 000 tr/min.  Le réglage se fait via une molette graduée sur le corps de la machine. 

![](../.gitbook/assets/image%20%2819%29.png)



Porte outils de diamètre \(S sur le schéma\): 

* 3mm
* 1/8" \(3.17mm\)
* 6 mm
* 8 mm

![i doit &#xEA;tre sup&#xE9;rieur &#xE0; l&apos;&#xE9;paisseur du panneau \(ou de la profondeur de la gravure\)](../.gitbook/assets/image%20%2848%29.png)

## **Outil de coupe \(Fraise\)**

Ne pas confondre mèche et fraise. L'un coupe verticale tandis que l'autre coupe latéralement

![](../.gitbook/assets/image%20%2840%29.png)

### **Diamètre**

De 0.1mm à 22mm,

### **Profils**

![Differents profils de fraises](../.gitbook/assets/image%20%2830%29.png)

### **Flutes**

 ****Lorsque l'outils rentre dans la matière usinée, chaque flute enlève/ejecte un copeau vers le haut \(fraises upcut\) ou vers le bas \(fraises downcut\) . Au moins il y a de flutes, au plus les copeaux sont gros. Il ne faut jamais usiner plus profondément que la longueur des flutes. Sinon, les copeaux s'accumulent et l'outils s'échauffe à cause des frottements.

![](../.gitbook/assets/image%20%2832%29.png)



En résumé : Plus de flutes --&gt; meilleur rendu de surfaceMoins de flutes --&gt; Evacuation des copeaux accrues \(idéal pour le plastique\)

## **Vitesse d'avance et vitesse de coupe**

La vitesse d'avance \(feed rate\) et la vitesse de coupe doivent adaptée en fonction de l'outils de coupe. 

La broche de la CNC est sensé réaliser des copeaux et non de la poussière. Julien Leresteux a écit un chouette tuto sur le calcul de la vitesse   
→ [http://leresteux.net/comment-choisir-son-feedrate-sur-fusion360/](http://leresteux.net/comment-choisir-son-feedrate-sur-fusion360/)  

### **Vitesse de coupe**

C'est la vitesse à laquelle la lame de l'outil attaque la pièce. Pour une même vitesse de rotation, la vitesse de coupe augmente avec le diamètre de l'outil. C'est pour celà que les outils de petit diamètre doivent tourner très vite. On exprime la vitesse de coupe généralement en mètres par minute. Par exemple, une fraise de 6mm de diamètre tournant à 15 000 tours minutes aura une vitesse de coupe de : 6 /1000 \* 3.14 \* 15000 = 283 m/minute. 

### **Vitesse d'avance**

C'est la vitesse à laquelle avance votre tête de fraisage. Elle s'exprime en métres par minute ou en mm par seconde. Elle ne dépend que du réglage de vitesse de votre machine telle que définie dans votre programme de coupe. Avancer plus vite génère des efforts plus importants, il faut donc que votre machine puisse : 1/ Atteindre cette vitesse 2/ Développer sufisamment de force à la vitesse atteinte Une vitesse d'avance plus faible donne généralement un meilleur fini de surface. Ne pas avoir des vitesses d'avance trop faibles, cela fait chauffer les matériaux. Il faut faire des copeaux, pas de la poudre ! Une vitesse trop faible use votre fraise nettement plus rapidement.L'effort dépend de tous les paramètres de coupe, mais surtout du matériau usiné, l'acier étant de loin le plus difficile. Si vous êtes obligé de diminuer l'avance \(pour une question de capacité machine ou pour obtenir un meilleur fini\), il est parfois nécessaire de diminuer la vitesse de coupe \(diminuer la vitesse de rotation\), pour maintenir une épaisseur de copeau suffisante. ****

### **Profondeur de coupe**

**S**i les matériaux découpés sont relativement épais, on ne pourra pas les couper en une seule fois, il faudra effectuer plusieurs passes en descendant l'outil au fur et à mesure. Pour découper des panneaux en bois, par exemple, il est généralement déconseillé de dépasser le diamètre de la fraise comme profondeur de passe. Une plus grande profondeur augmente aussi les efforts de coupe.  De manière générale, on veut le déplacer le plus rapidement possible sans sacrifier la finition de la surface. Au plus l'outils usine au même endroit, au plus il chauffe, et au plus il s'use. 

* Une vitesse de rotation trop elevée et une vitesse d'avance trop lente. :La matière s'échauffe, fond ou brule.
* Une vitesse de rotation trop faible et un un vitesse d'avance trop rapide :  usure accrue de l'outils de coupe et risque de casse.

  
Sources : [http://makezine.com/magazine/make-40/endmills/](http://makezine.com/magazine/make-40/endmills/)   

