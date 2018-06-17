---
layout: post
title: Le robot qui dessine V2 - 1
date: '2017-12-27 20:30:00 CET'
category: Blog
tags: ['Mindstorms', 'Plan de Montage']
published: true
assetsFolder: /le-petit-algonaute/assets/posts/2017-12-27/203000/
thumbnail: /le-petit-algonaute/assets/posts/2017-12-27/203000/thumbmail-dessinatorv2-150x150.png
---

### Les principes de fonctionnement

Le robot qui dessine est construit sur une base de rover.

![Rover Monté]({{page.assetsFolder}}/0-ensemble/dessinateurv2-all-small.png)


### Comment poser et lever le stylo ?

Un petit moteur annexe est placé dans le rover pour poser/lever le stylo.

Ce moteur va actionner un bras mobile à l'avant. Lorsque le bras est en position basse le robot peut écrire. Quand il est en position haute le stylo ne touche plus la feuille.

Dans la conception il est important que le stylo se trouve entre les roues avant. De cette manière lorsque le robot pivote, le stylo peut dessiner un angle.

![Porte-stylo Monté]({{page.assetsFolder}}/0-ensemble/dessinateurv2-all-avec-porte-stylo-small.png)


Comme le moteur tourne sur un plan horizontal et que l'on veut convertir ce mouvement en déplacement vertical linéaire on va utiliser deux mécanismes.

Les deux engrenages font tourner un axe qui est perpendiculaire au moteur. L'engrenage jaune est entraîné par le moteur, il fait tourner l'engrenage noir qui fait tourner l'axe auquel le bras est relié.

![Linear actuator 1]({{page.assetsFolder}}/0-ensemble/linear-actuator-1.png)

Le bras à l'avant convertit la rotation de l'axe en mouvement de haut en bas. Lorsque l'axe tourne les barres du bas tournent avec l'axe. Le reste des barres suit le mouvement car les connecteurs gris sont sans friction.

![Linear actuator 2]({{page.assetsFolder}}/0-ensemble/linear-actuator-2-small.png)

### Les points d'attention

Après plusieurs essais ratés nous avons constaté que le robot ne doit pas avoir pas être trop lourd (il emporte la feuille de papier) et ne doit pas avoir trop de poids à l'arrière (il pivote sur la roue folle à l'arrière au lieu de pivoter sur les roues avant)


### Le plan de montage

Le rover va être construit en quatre parties :
- [le moteur du porte-stylo]({{site.prefix}}/blog/2017/12/28/le-robot-qui-dessine-v2-2),
- [le porte-stylo]({{site.prefix}}/blog/2017/12/28/le-robot-qui-dessine-v2-3),
- [le chassis]({{site.prefix}}/blog/2017/12/29/le-robot-qui-dessine-v2-4),
- [la brique de contrôle]({{site.prefix}}/blog/2017/12/29/le-robot-qui-dessine-v2-5).

![Rover Eclaté]({{page.assetsFolder}}/0-ensemble/dessinateurv2-avec-porte-stylo-exploded.png)

La liste complète des pièces nécessaires peut être téléchargée [ici]({{page.assetsFolder}}/BOM-dessinateurv2-avec-porte-stylo.xlsx). Toutes les pièces proviennent du kit EV3 Home sauf la roue folle. Cet élément peut être remplacé par un montage utilisant une petite roue ou acheté en complément pour une dizaine d'euros.


