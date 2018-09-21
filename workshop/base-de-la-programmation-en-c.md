# Base de la programmation en C

## Base de la programmation C-like

Ceci détaille les languages "C". Ce sont des langages à présentation libre. Le point-virgule indiquant la fin de l'instruction.

```text
int x = 10; x++; printf("%d",x);
```

est équivalent à :

```text
int x = 10;
                 x++;
      printf("%d",               x);
```

## **Commentaires**

Ce sont des lignes de texte incluses dans le programme et qui ont pour but de vous aider à comprendre \(ou à vous rappeler\) comment votre programme fonctionne ou d'en informer les autres. Ces lignes ne sont pas envoyés au microprocesseur. Il y a deux façons de créer des lignes de commentaires :

```text
/* ceci est
   un commentaire
   sur plusieurs lignes
*/

// Ceci est un comment sur 1 ligne.
```

## Accolades{ }, structure de boucles et de conditions

Les accolades sont un élément majeur de la programmation en langage C. Toute accolade ouverte doit être accompagnée d'une accolade fermée, délimitant un bloc de code.

**Fonctions**

```text
void myfunction(datatype argument){ // ouverture de la fonction
    // vos instructions ici
  } // fermeture de la fonction
```

**Boucles**

```text
while (boolean expression)
  { // accolade d'ouverture du code de la boucle while - 
     // vos instructions ici
  } // fermeture de la boucle

  do{ // accolade d'ouverture du code de la boucle do 
     // vos instructions
  } while (boolean expression); // fermeture de la boucle

  for (initialisation; termination condition; incrementing expr)
  { // ouverture du code de la boucle for
    //instructions
  } // fermeture de la boucle
```

**Conditions**

```text
  if (boolean expression)
  { // ouverture du code de la condition if
     // vos instructions
  } // fermeture du code de la condition if
  else if (boolean expression)
  { // ouverture du code de l'instruction else if
     // vos instructions
  } // fermeture du code de l'instruction else if
  else
  { // ouverture du code de l'instruction else
     // vos instructions
  } // fermeture du code de l'instruction else
```

## Opérateurs

**Assignation**

```text
variable = valeur ;
```

**Binaire**

```text
 variable1 + variable2 / 30 * 1.0 ;
 // Les opérateurs binaires sont donc + - / * 
```

**Unaire**

```text
  i++ ; 
  // est équivalent à 
  i = i + 1 ;
  // est équivalent à 
  i += 1;
```

## Type de données

* byte : entier sur 8 bit 
* char : character \(codé sur 1 byte\)
* int : entier 
* float : nombre à virgule 
* double : nombre à virgule à haut précision ...

## **Instructions :**

**Déclaration d'une variable** on vient avec cette ligne stocker la valeur à droite du signe égal dans la [variable](http://www.mon-club-elec.fr/pmwiki_reference_arduino/pmwiki.php?n=Main.ApprendrePartiesProgramme) à gauche du signe égal.

```text
int led = 13;
```

... To be continued....

