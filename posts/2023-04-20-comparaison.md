---
layout: post
title: 'ENTD 2008 / EMP 2019 : comparaison des bases de données de mobilité'
date: '2023-04-20 13:37:42 +0200'
---

## Introduction
L’enquête « Mobilité des personnes » de 2019 (EMP-2019) succède à l’enquête nationale transport et déplacements de 2008 (ENTD-2008). S’appuyant sur des méthodologies similaires, elles permettent de comprendre les évolutions de la mobilité des Français au cours du temps. Ce type d’enquête est effectuée tous les dix ans environ par le SDES[^1] . L’enquête de 2019 a été réalisée en amont de l’épidémie de Covid-19, les résultats éclairent donc le comportement des Français juste avant la crise sanitaire. Les bases de données des deux enquêtes sont disponibles dans mobility-tools ainsi qu'une analyse de leurs résultats. Voyons ici les principaux changements dans les habitudes de mobilité des Français et comment Mobility permet de les approfondir et de mieux les comprendre.

## Composition des bases de données
Chaque personne participant à l’enquête devait répondre à des questions relatives à leurs véhicules, abonnements pour les transports, motifs de déplacements, etc. pour leurs déplacements quotidiens et longues distances (supérieurs à 80 km). Les personnes interrogées sont assez homogènes entre les deux enquêtes, le graphique suivant présente par exemple la répartition relative des trajets quotidiens en fonction des catégories socio-professionnelles (csp) des personnes interrogées :
 
![image](https://user-images.githubusercontent.com/19514464/233441020-c947b272-84bb-4fb5-881f-a5ed8f23c56f.png)
*Figure 1 : répartition des trajets quotidiens en fonction de la catégorie socio-professionnelle*

De manière similaire, la répartition des trajets par catégorie urbaine (R, I, B, C)[^2], par mode de transport et motif de déplacement est assez proche entre les deux enquêtes. Néanmoins, le même graphique que précédemment en absolu donne un écart conséquent entre les deux enquêtes :
![image](https://user-images.githubusercontent.com/19514464/233442337-401dd98c-0ad8-4049-b98f-08cee4d184ec.png)
*Figure 2 : nombre de trajets quotidiens par catégorie socio-professionnelle*

Ce graphique montre que la base de données de 2008 possède beaucoup plus de trajets que celle de 2019 pour les trajets de courte distance (environ 3 fois plus). 
![image](https://user-images.githubusercontent.com/19514464/233442535-caa872ca-0100-4072-b778-d2ff0e0b035b.png)
*Figure 3 : répartition des trajets quotidiens par mode*

La répartition des trajets en fonction des modes de déplacement met en évidence un léger recul de l’automobile au profit de la marche et des transports en communs pour les déplacements de courte distance. Même si la base de données de 2008 est plus fournie, il semble plus intéressant de se baser sur celle de 2019 pour prendre en compte ces évolutions de la mobilité.

## Indicateurs mobilité
Par la suite, nous avons voulu caractériser plus en détail la mobilité des Français avec un ensemble d’indicateurs. Nous avons commencé par étudier la distance moyenne par trajet, qui est assez homogène entre 2008 et 2019 pour les trajets quotidiens, que ce soit en fonction de la catégorie urbaine ou de la catégorie socio-professionnelle.
![image](https://user-images.githubusercontent.com/19514464/233442800-5fcf0da1-da4b-4cad-bdfa-44346d3bd4f0.png)
*Figure 4 : distance moyenne par trajet quotidien*
