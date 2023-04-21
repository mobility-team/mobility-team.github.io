---
layout: post
title: 'Estimer l'empreinte carbone associée à la mobilité d'un habitant'
subtitle: 'Par Louise Gontier'
date: '2023-04-21 15:00:00 +0200'
---

## Estimer l'empreinte carbone mobilité d'un habitant
L’outil Mobility permet d’estimer les déplacements de courte et longue distance d’une personne selon son lieu de vie (catégorie urbaine) et ses caractéristiques (catégorie socio-professionnelle (CSP) de la personne et de la personne de référence de son ménage, de sa possession ou non d’une voiture, et nombre de personnes du ménage).
Les déplacements obtenus sont décrits par un motif de déplacement, un mode de déplacement, une distance en km (via l’origine et la destination) ainsi que le nombre de personnes partageant ce déplacement.
Ainsi, il est possible d’estimer les émissions carbone associées à la mobilité, annuelle par exemple, d’une personne en y intégrant les facteurs d’émissions des différents modes de transports utilisés : c’est ce que permet la fonction carbon_computation.py.
En effet, grâce aux données de la Base Empreinte de l’ADEME[^1], il est possible de récupérer les facteurs d’émission moyen des modes de transport en France

![logigramme_empreinte](https://user-images.githubusercontent.com/105421514/233650259-69d2499f-9e05-483b-8d3c-2a180ffc6c2f.png)<br>
*Figure 1 : logigramme du fonctionnement de population x mobility*

Ainsi, l’application de Mobility peut permettre de calculer les émissions carbone associées à la mobilité des habitants d’un territoire. Par exemple, si l’on cherche à estimer l’empreinte carbone annuelle moyenne de la mobilité des habitants d’une commune, il est possible de suivre ces étapes : 
1.	Echantillonnage d’une population représentative de la commune sur la base des données de l’INSEE par exemple. Le package Population, développé par elioth, permet de le faire pour la commune de son choix sur la base d’un nombre de ménages ou d’un programme de logements. Le package permet ainsi d’obtenir un groupe d’habitants de la commune et ses caractéristiques, notamment leur CSP, leur possession d’une voiture, le nombre de personnes du ménages
2.	Allocation de la catégorie urbaine de la commune (Code R, B, C, I en fonction du type de commune)
3.	Estimation des déplacements annuels de chaque individu échantillonné en utilisant le trip_sampler.py de Mobility. La table obtenue contient, par déplacement et pour chaque habitant, les km parcourus par mode et le nombre de personnes accompagnant le déplacement.
4.	Allocation d’un facteur d’émission [kgCO2e/pers.km] selon le mode de transport utilisé pour chaque déplacement de chaque individu via Mobility et la fonction carbon_computation.py. Pour les déplacements en voiture individuelle, le facteur d’émission associé est recalculé en fonction du taux de remplissage du véhicule. Il est possible de préciser des facteurs d’émission, et ainsi remplacer les facteurs d’émission génériques de l’ADEME, dans le cas où ils sont connus et différents de la moyenne, par exemple si la commune dispose de bus électriques.
5.	Sur cette base, il est possible d’évaluer les émissions annuelles moyennes de chaque individu échantillonné mais également de le détailler par courte/ longue distance, par motif, par type d’habitant, etc.


[^1]: ADEME, Base Empreinte




