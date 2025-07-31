# Projet E-puck: Suivi de ligne et navigation autonome
Ce dépôt contient deux programmes développés en langage C pour le robot E-puck, dans le cadre d’un projet universitaire en automatique et robotique. Ces programmes exploitent les capteurs infrarouges et de proximité du robot pour simuler des comportements de navigation dans un environnement virtuel sous Webots.

## Contenu du dépôt
### Autonomous_Navigation_IR_And_Proximity.c
Ce programme met en œuvre un comportement de navigation autonome combinant deux fonctionnalités :
- le suivi de ligne via trois capteurs infrarouges (gauche, milieu, droite),
- l’évitement d’obstacles via les capteurs de proximité (ps0, ps5, ps6, ps7).

Le robot suit une ligne noire tracée au sol tout en surveillant son environnement. Lorsqu’un obstacle est détecté en face ou sur le côté, il adapte sa trajectoire en tournant ou en s’arrêtant temporairement. Si la ligne est détectée sous le capteur central, le robot effectue un ajustement directionnel en fonction des capteurs gauche et droit.
Ce comportement permet de simuler une navigation robuste dans un environnement semi-structuré, avec des obstacles fixes.

### Basic_Line_Following_Infrared_Sensors.c
Ce programme plus simple met en œuvre un suivi de ligne basé uniquement sur les capteurs infrarouges. Il ne prend pas en compte les obstacles.
Le fonctionnement est basé sur la détection de la ligne noire sous le capteur central. Si la ligne est détectée, le robot ajuste sa trajectoire vers la gauche ou la droite en fonction de la différence de lecture entre les capteurs gauche et droit. En l’absence de détection, il avance tout droit.
Ce code est particulièrement adapté aux environnements de test linéaires ou à des circuits simples sans interférence extérieure.

### Epuck_Track_Simulation.png
Image illustrant l’environnement de simulation utilisé sous Webots. Elle montre un circuit au sol avec une ligne noire à suivre, des murs simulés, et le robot E-puck placé en position de départ.

## Prérequis
- Webots installé avec le contrôleur E-puck actif
- Projet configuré pour détecter les capteurs de distance et infrarouges
- Fichiers `.c` intégrés dans le contrôleur de robot

## Auteur
Mehdi Rouissi  
Master 1 Automatique  
