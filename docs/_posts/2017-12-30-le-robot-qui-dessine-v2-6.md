---
layout: post
title: Le robot qui dessine V2 - 6
date: '2017-12-30 19:30:00 CET'
category: Blog
tags: ['Mindstorms', 'Plan de Montage']
published: true
assetsFolder: /le-petit-algonaute/assets/posts/2017-12-27/203000/0-ensemble
assetsFolderProgramme: /le-petit-algonaute/assets/posts/2017-12-27/203000/5-programme
thumbnail: /le-petit-algonaute/assets/posts/2017-12-27/203000/thumbmail-dessinatorv2-150x150.png
---

Ce billet est la dernière partie de la construction du [robot qui dessine]({{site.prefix}}/blog/2017/12/27/le-robot-qui-dessine-v2-1).

L'objectif dans cette étape est d'assembler tous les éléments que l'on vient de construire et de commencer à tester le robot

### Finir le montage

Le robot tout assemblé va ressembler à ça.

![Montage terminé]({{page.assetsFolder}}/dessinateurv2-all-avec-porte-stylo-small.png)

Pour le moment, il est en 3 parties

![Vision explosée]({{page.assetsFolder}}/dessinateurv2-avec-porte-stylo-exploded.png)

Le schéma suivant montre à quel endroit le dessous du chassis se fixe sur le petit moteur.

![chassis-moteur]({{page.assetsFolder}}/chassis-moteur-small.png)

Le schéma suivant montre à quel endroit la brique s'attache sur le chassis.

![chassis-brique]({{page.assetsFolder}}/chassis-brique-small.png)

Il ne reste plus qu'à fixer les cables.
- les deux gros moteurs sont connectés sur B et C
- le petit moteur est connecté sur D

![cablage]({{page.assetsFolder}}/cablage-small.png)

### Le projet exemple

Le projet exemple peut être téléchargé [là]({{page.assetsFolder}}/dessinator-v2.ev3)

### Poser et lever le stylo

On peut tout d'abord tester le fonctionnement du stylo avec le programme suivant. Ce programme lève le stylo puis le repose.

Avant de lancer, il faut positionner la pointe du stylo au niveau de la feuille

![stylo]({{page.assetsFolderProgramme}}/stylo.png)

> Lorsque le moteur tourne en marche arrière (-30) il soulève le stylo.
> Lorsque le moteur tourne en marche avant (30) il abaisse le stylo.

> L'angle de rotation du moteur doit rester petit (45 par exemple) car il suffit de déplacer le stylo sur moins de 1cm.



### Tracer un cercle

La figure la plus simple à tracer est le cercle.

Avant de lancer, il faut positionner la pointe du stylo au niveau de la feuille

![cercle]({{page.assetsFolderProgramme}}/cercle-small.png)

> Si on ne fait tourner qu'une roue, le robot va tourner autour de l'autre roue. Ici, on fait avancer la roue commandée par B, la roue gauche. La roue droite reste immobile et le robot va pivoter sur cette roue. Si on fait ça suffisamment longtemps, le robot trace un cercle.

Aller plus loin :
- comment peut on calculer le rayon de ce cerclsmae ?
- comment calculer le nombre de tours de roues nécessaires pour faire le cercle complet
- comment peut on faire un cercle plus large ?

indices:
- le diamètre des roues est 4,32 cm
- vous pouvez utiliser les deux roues

### Tracer un carré

Tracer un carré nécessaire de faire 4 lignes droites et pivoter pour tourner à chaque coin. On va lever le stylo dans chaque coin pour éviter les gribouillages.
Attention, ce programme démarre (et fini) stylo levé. Si nécessaire, utilisez une partie du programme "stylo" pour  placer le stylo à la bonne hauteur.

![carré]({{page.assetsFolderProgramme}}/carre.png)

> Pour faire pivoter le robot sur place, on faire tourner une roue en marche avant pendant que l'autre tourne en marche arrière. De cette manière, le robot va pivoter autour d'un point qui est entre les deux roues au niveau du stylo.

> L'action "poser le stylo, faire une ligne droite, lever le stylo et pivoter" est répétée 4 fois (une fois par arrête du carré). On utilise un bloc boucle pour indiquer cette répétition. Le nombre de répétitions est indiqué à droite de la boucle, ici c'est 4.

> Sur le bloc qui permet de pivoter, le nombre de degrés est calculé pour que le robot pivote à environ 90°. Attention, le nombre de degré ici est le nombre de degré en tours de roue. Cela n'a pas forcément de rapport avec l'angle de rotation du robot.

Vous aurez peut être à changer le nombre de degrés de rotation du bloc qui pivote. Selon le type de sol le frottement est plus ou moins important et le robot tournera plus ou moins facilement. Il l'angle du virage du robot peut être différent de 90°. Il est possible de vérifier l'angle du rotation avec un capteur, mais pour l'instant on va rester sur un programme simple.


Aller plus loin :
- comment peut on faire un carré plus grand ?
- comment peut on faire un triangle ?

indices:
- il faudra changer la durée ou le nombre de rotations des blocs
- restez à des vitesses moyennes entre 30 et 60 (ou -30 et -60 en marche arrière). Si la vitesse est trop basse, le frottement est très important et le robot avance mal. Si la vitesse est trop grande, les manoeuvres deviennent très imprécises.




