---
layout: post
title: 'Estimer l'empreinte carbone associée à la mobilité d'un habitant'
subtitle: 'Par Louise Gontier'
date: '2023-04-21 15:00:00 +0200'
---

## Introduction
L’outil Mobility permet d’estimer les déplacements de courte et longue distance d’une personne selon son lieu de vie (catégorie urbaine) et ses caractéristiques (catégorie socio-professionnelle (CSP) de la personne et de la personne de référence de son ménage, de sa possession ou non d’une voiture, et nombre de personnes du ménage).
Les déplacements obtenus sont décrits par un motif de déplacement, un mode de déplacement, une distance en km (via l’origine et la destination) ainsi que le nombre de personnes partageant ce déplacement.
Ainsi, il est possible d’estimer les émissions carbone associées à la mobilité, annuelle par exemple, d’une personne en y intégrant les facteurs d’émissions des différents modes de transports utilisés : c’est ce que permet la fonction carbon_computation.py.
En effet, grâce aux données de la Base Empreinte de l’ADEME[^1], il est possible de récupérer les facteurs d’émission moyen des modes de transport en France


*Figure 1 : logigramme du fonctionnement de population x mobility*


[^1]: ADEME, Base Empreinte




