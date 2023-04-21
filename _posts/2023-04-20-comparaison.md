---
layout: post
title: 'ENTD 2008 / EMP 2019 : comparaison des bases de données de mobilité'
subtitle: 'Par Arthur Haulon'
date: '2023-04-20 13:37:42 +0200'
---

## Introduction
L’enquête « Mobilité des personnes » de 2019 (EMP-2019) succède à l’enquête nationale transport et déplacements de 2008 (ENTD-2008). S’appuyant sur des méthodologies similaires, elles permettent de comprendre les évolutions de la mobilité des Français au cours du temps. Ce type d’enquête est effectuée tous les dix ans environ par le SDES[^1] . L’enquête de 2019 a été réalisée en amont de l’épidémie de Covid-19, les résultats éclairent donc le comportement des Français juste avant la crise sanitaire. Les bases de données des deux enquêtes sont disponibles dans mobility-tools ainsi qu'une analyse de leurs résultats. Voyons ici les principaux changements dans les habitudes de mobilité des Français et comment Mobility permet de les approfondir et de mieux les comprendre.

## Composition des bases de données
Chaque personne participant à l’enquête devait répondre à des questions relatives à leurs véhicules, abonnements pour les transports, motifs de déplacements, etc. pour leurs déplacements quotidiens et longues distances (supérieurs à 80 km). Les personnes interrogées sont assez homogènes entre les deux enquêtes, le graphique suivant présente par exemple la répartition relative des trajets quotidiens en fonction des catégories socio-professionnelles (csp) des personnes interrogées :
 
![image](https://user-images.githubusercontent.com/19514464/233441020-c947b272-84bb-4fb5-881f-a5ed8f23c56f.png)<br>
*Figure 1 : répartition des trajets quotidiens en fonction de la catégorie socio-professionnelle*

De manière similaire, la répartition des trajets par catégorie urbaine (R, I, B, C)[^2], par mode de transport et motif de déplacement est assez proche entre les deux enquêtes. Néanmoins, le même graphique que précédemment en absolu donne un écart conséquent entre les deux enquêtes :

![image](https://user-images.githubusercontent.com/19514464/233442337-401dd98c-0ad8-4049-b98f-08cee4d184ec.png)<br>
*Figure 2 : nombre de trajets quotidiens par catégorie socio-professionnelle*

Ce graphique montre que la base de données de 2008 possède beaucoup plus de trajets que celle de 2019 pour les trajets de courte distance (environ 3 fois plus). 

![image](https://user-images.githubusercontent.com/19514464/233442535-caa872ca-0100-4072-b778-d2ff0e0b035b.png)<br>
*Figure 3 : répartition des trajets quotidiens par mode*

La répartition des trajets en fonction des modes de déplacement met en évidence un léger recul de l’automobile au profit de la marche et des transports en communs pour les déplacements de courte distance. Même si la base de données de 2008 est plus fournie, il semble plus intéressant de se baser sur celle de 2019 pour prendre en compte ces évolutions de la mobilité.

## Indicateurs mobilité
Par la suite, nous avons voulu caractériser plus en détail la mobilité des Français avec un ensemble d’indicateurs. Nous avons commencé par étudier la distance moyenne par trajet, qui est assez homogène entre 2008 et 2019 pour les trajets quotidiens, que ce soit en fonction de la catégorie urbaine ou de la catégorie socio-professionnelle.
![image](https://user-images.githubusercontent.com/19514464/233442800-5fcf0da1-da4b-4cad-bdfa-44346d3bd4f0.png)<br>
*Figure 4 : distance moyenne par trajet quotidien*

Pour les trajets de longue distance, on peut noter des distances moyennes plus importantes en 2019 (340 km par trajet pour 2008 contre plus de 410 km par trajet pour 2019).

![image](https://user-images.githubusercontent.com/19514464/233443631-785c1b7f-a779-4197-899e-543cea2bbd19.png)<br>
*Figure 5 : distance moyenne par trajet longue distance*

Pour les déplacements quotidiens, le Français moyen parcourt environ 30 km/jour (30,8 pour 2008 et 31 pour 2019). L’utilisation de la voiture est encore très importante pour les déplacements quotidiens et représente plus de 84 % de la part modale. On peut tout de même observer un léger report modal de la voiture vers les transports en commun notamment.

![image](https://user-images.githubusercontent.com/19514464/233443752-86651c96-6aeb-452f-9fcf-a91122e4d99c.png)<br>
*Figure 6 : distance journalière moyenne par mode*

On peut également filtrer nos bases de données pour uniquement calculer les distances quotidiennes pour une certaine catégorie urbaine, catégorie socio-professionnelle, ou si on est en semaine ou le week-end. Par exemple, en milieu rural, la voiture est, comme pressenti, prépondérante et les distances quotidiennes sont plus élevées qu’en centre-ville (plus de 15 km de différence chaque jour).

![image](https://user-images.githubusercontent.com/19514464/233443931-9ce20ba0-caf2-467f-b9f7-51eebc63ddae.png)<br>
*Figure 7 : comparaison de la mobilité quotidienne entre milieu rural (gauche) et centre-ville (droite)*

Il est également possible de tracer les distances quotidiennes en fonction des motifs de déplacement en ayant encore la possibilité de filtrer les bases de données pour restreindre l’étude. Par exemple, les graphiques ci-dessous présentent les distances moyennes journalière en fonction des motifs de déplacement, pour un jour de semaine et un jour du week-end. Ils mettent en évidence les différences d’activités entre la semaine et le week-end et leur part en termes de distance journalière.

![image](https://user-images.githubusercontent.com/19514464/233444064-0184c494-f1e1-4e08-923b-a17d599a86ca.png)<br>
*Figure 8 : distance journalière moyenne un jour de semaine ou de week-end*

Il est également intéressant de comparer les taux de remplissage des voitures en fonction des motifs de déplacement. Tous motifs confondus, le taux de remplissage est proche de 1,9. On peut remarquer que le covoiturage s’est peu développé en 10 ans pour les déplacements domicile/travail, avec des taux de remplissage proches de 1 mettant en lumière l’importance de l’autosolisme des déplacements pendulaires. 

![image](https://user-images.githubusercontent.com/19514464/233444186-76cb5936-2050-4859-a45e-b3651638be89.png)<br>
*Figure 9 : taux de remplissage moyen des voitures des déplacements quotidiens*

L’outil permet enfin de tracer les distances et émissions moyennes par trajet (courte distance) en fonction du motif de déplacement. Pour cela, nous avons affecté à chaque mode de déplacement un facteur d’émission en kgCO2e/passager.km. 

![image](https://user-images.githubusercontent.com/19514464/233444335-e0931e8e-4d19-4694-9270-513334a2ff06.png)<br>
*Figure 10 : émission de GES moyenne par déplacement quotidien*

Les variations d’émissions pour chaque motif relativement aux distances peuvent s’expliquer par la répartition modale de chaque motif ainsi que les différents taux de remplissages des voitures. On voit notamment que plus de 70 % des déplacements domicile-travail s’effectuent en voiture, avec un taux de remplissage faible expliquant l’émission moyenne relativement élevée. En comparaison, les déplacements de motif « Vacances » sont en moyenne plus élevés en distance mais émettent moins que les déplacements domicile-travail. On peut l’expliquer notamment par un taux de remplissage plus élevé (proche de 2 personnes par voiture).

![image](https://user-images.githubusercontent.com/19514464/233444473-f8db6eb8-dc11-4258-a120-189c21266274.png)
![image](https://user-images.githubusercontent.com/19514464/233444500-2a966120-5369-465d-9c20-08b81adb53c7.png)
![image](https://user-images.githubusercontent.com/19514464/233444517-d330eca7-f3a5-4297-a092-0b689bd09ec2.png)

## Conclusion

Pour aller plus loin, les articles suivants analysent d’autres indicateurs comme les pratiques de mobilités selon l’âge, le genre, ou encore les temps passés dans les transports :
* *[Mobilités du quotidien : comprendre les années 2010-2020 pour mieux appréhender demain](https://doc.cerema.fr/Default/doc/SYRACUSE/584812/mobilites-du-quotidien-comprendre-les-annees-2010-2020-pour-mieux-apprehender-demain)*, Cerema, 2022
* *[Comment les Français se déplacent-ils en 2019 ? Résultats de l'enquête mobilité des personnes](https://www.statistiques.developpement-durable.gouv.fr/comment-les-francais-se-deplacent-ils-en-2019-resultats-de-lenquete-mobilite-des-personnes)*

## Méthodologie
* Le code Python utilisé est disponible [en opensource](https://github.com/mobility-team/mobility/tree/main/examples/compare_db) au sein de la librairie [Mobility](https://github.com/mobility-team/mobility)
* Pour en savoir plus sur la méthodologie de l’enquête : [Enquête sur la mobilité des personnes 2018-2019](https://www.statistiques.developpement-durable.gouv.fr/enquete-sur-la-mobilite-des-personnes-2018-2019)
* Les données utilisées proviennent des tables des trajets courts et trajets longs des deux enquêtes. Plusieurs types de pondérations sont inclus dans l’enquête permettant de disposer de différents niveaux de représentativité : les pondérations relatives à la population (ménages et individus) et les pondérations relatives aux variables de l’enquête (déplacements, voyages, véhicules).
* L’unité urbaine est définie comme la « commune ou ensemble de communes présentant une zone de bâti continu (pas de coupure de plus de 200 mètres entre deux constructions) qui compte au moins 2 000 habitants ».<br> La classification RIBC de l’INSEE répartit les villes en quatre catégories, en fonction de leur unité urbaine d’appartenance :
   * Rurale : commune n’appartenant à aucune unité urbaine.
   * Isolée : commune étant seule au sein de son unité urbaine.
   * Centre et Banlieue : communes appartenant à une unité urbaine composées de plusieurs communes. L’unité urbaine est alors dénommée « agglomération multicommunale ». La distinction entre Centre et Banlieue se fait selon la taille relative de population au sein de la commune. Ainsi, « si une commune représente plus de 50 % de la population de l'agglomération multicommunale, elle est seule ville-centre. Sinon, toutes les communes qui ont une population supérieure à 50 % de celle de la commune la plus peuplée, ainsi que cette dernière, sont villes-centres. Les communes urbaines qui ne sont pas villes-centres constituent la banlieue de l'agglomération multicommunale. ».
* La mobilité locale est caractérisée par les trajets restreints à une zone de 80 km à vol d’oiseau du domicile de la personne interrogée. 
* Pour les modes et motifs de déplacement, nous avons défini des clés de répartition pour les grouper en un nombre restreint de typologies. Par exemple, le mode « Piéton » regroupe les modes :
   * 1.10 : Uniquement marche à pied
   * 1.11 : Porté, transporté en poussette
   * 1.12 : Rollers, trottinette
   * 1.13 : Fauteuil roulant (y compris motorisé)

[^1]: Service des Données et Etudes Statistiques du Ministère de la Transition Ecologique

[^2]: La classification RIBC de l’INSEE répartit les villes en quatre catégories, en fonction de leur unité urbaine d’appartenance (Rurale, Isolée, Banlieue, Centre)


