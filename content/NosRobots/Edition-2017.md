---
title: "Edition 2017"
featured_image: '/robots/Edition2017.png'
type: page
date: 2017-04-10T11:00:59-04:00
robot_footage: "/robots/Edition2017.png"

---



# Bornibus

{{< illustration-right src=/robots/2017/Bornibus-rotation.gif width="40%" >}}

## Présentation générale

Bornibus est un robot conçu uniquement pour ramasser et déposer les modules lunaires. Il est capable de prendre et stocker jusqu'à 4 modules simultanément. 



Le robot est constitué de 4 parties. La base roulante en aluminium contient les moteurs, les roues codeuses, ainsi que 2 capteurs ultrasons. La partie au dessus correspond à la zone d'action des différents mécanismes (manipulation des modules ...). La partie supérieure du robot contient la majorité des cartes électroniques (carte moteur, raspberry pi 3 pour l'intelligence, ...). Enfin, le support balise surplombe le robot, en incluant 4 capteurs ultrasons permettant de détecter les robots adverses.


## L'intelligence et les déplacements

L'odométrie, ou le positionnement du robot, est réalisé uniquement via des roues codeuses. Ce système nous permet d'être assez précis sur des courtes distances, mais dérive en fonction des trajectoires parcourues. Un recalage de l'odométrie au moment de la dépose des modules nous permet de compenser cette dérivation et d'être suffisamment précis pendant les 90s du match pour aller chercher tous les modules lunaires. Pour détecter les problèmes de patinage, les roues codeuses ne sont pas solidaires des arbres moteurs. Cette détection permet à l'intelligence de comprendre que le robot est coincé et qu'il faut trouver une autre trajectoire / un moyen pour se recaler.


{{< illustration-center src=/robots/2017/trajectoire.gif width="50%" >}}

## Les actionneurs

La réussite d'un actionneur repose essentiellement sur un mot : la fiabilité. Un actionneur fiable nous permet d'être sûr que l'action pour laquelle il a été conçu sera réalisée à chaque fois. C'est sur ce principe qu'ont été pensés les actionneurs de Bornibus : des actionneurs simples, mais robustes. De par leur simplicité, les actionneurs nécessiteront cependant une bonne précision dans les déplacements du robot.




| Le ramassage des modules          | Le système de dépose       |
|-------------------------|------------------------|
| Bornibus est équipé d'une pince capable de saisir les modules lunaire. Un système pignon / crémaillère lui permet de monter le module en haut de son réservoir. On peut remarquer que la pince est intelligemment conçu pour qu'à son ouverture en position haute, elle bascule immédiatement le module dans le réservoir.  | Le réservoir est capable de contenir jusqu'à 4 modules. La partie basse du réservoir est une sorte de "tiroir creux coulissant". Ce tiroir peut se déployer pour laisser tomber un module à la fois. Lorsque le système est déployé, le module déposé peut toujours être translaté pour faire de la place et déposer encore plus de modules.  |
| {{< illustration-center src=/robots/2017/Bornibus-drop.gif width="30%" >}}  |  {{< illustration-center src=/robots/2017/Bornibus-grab.gif width="30%" >}} |


## La détection des adversaires 

Bornibus est équipé de 6 capteurs ultrasons pour détecter les robots adverses : 4 capteurs sont situés dans le support de balise, et 2 autres se trouvent au niveau de la base roulante. Les capteurs scannent en permanence le terrain et envoient les données à la partie intelligence. L'intelligence du robot déduit, grâce à la position courante du robot, si les obstacles rencontrés sont des éléments de jeu, des robots adverses, ou encore des objets en dehors de la zone de jeu.

Bien que ce système soit fonctionnel et nous permette d'éviter la plupart des collisions, la détection reste assez bruitée, notamment lorsqu'un robot adverse utilise également des capteurs ultrasons. Pour palier à ce bruit, nous sommes actuellement en train de développer un système de localisation des robots adverses par balise.


# Muray


{{< illustration-right src=/robots/2017/Murray-rotation.gif width="40%" >}}


## Présentation générale

Murray est un robot conçu uniquement pour ramasser les roches lunaires (boules en polystyrène) et les déposer dans le panier ou dans la zone de départ. Il est capable de récupérer et stocker une vingtaine de boules simultanément. 

Le robot est constitué de 4 parties. La base roulante en aluminium contient les moteurs et les roues codeuses. Pour pouvoir stocker un nombre important de boules, un réservoir télescopique prend la majorité de l'espace disponible. Les cartes électroniques (carte moteur, carte actionneurs, ...), ainsi que la batterie, sont positionnées sous le réservoir. Enfin, le support balise surplombe le robot, en incluant 4 capteurs ultrasons permettant de détecter les robots adverses.

## L'intelligence et les déplacements

Une attention particulière a été apportée aux déplacements des robots. Grâce à un système ingénieux, Murray est capable d'effectuer des trajectoires courbes et de se faufiler entre les éléments du terrain. Son intelligence peut lui permettre de prendre ses propres décisions en temps réel et de changer ses trajectoires si nécessaire.


L'odométrie, ou le positionnement du robot, est réalisé uniquement via des roues codeuses. Ce système nous permet d'être assez précis sur des courtes distances, mais dérive en fonction des trajectoires parcourues. Le gabarit de ce robot ne nous permet pas d'effectuer un recalage au cours du match, mais comme le ramassage des boules ne demande pas une très grande précision, la position estimé par les roues codeuses nous sera suffisante. Pour détecter les problèmes de patinage, les roues codeuses ne sont pas solidaires des arbres moteurs. Cette détection permet à l'intelligence de comprendre que le robot est coincé et qu'il faut trouver une autre trajectoire / un moyen pour se recaler.



## Les actionneurs

La réussite d'un actionneur repose essentiellement sur un mot : la fiabilité. Un actionneur fiable nous permet d'être sûr que l'action pour laquelle il a été conçu sera réalisée à chaque fois. C'est sur ce principe qu'ont été pensés les actionneurs de Murray : des actionneurs simples, mais robustes. La robustesse des actionneurs est ici essentielle puisque la position de Murray pourra dévier de plusieurs millimètres au cours du match (pas de recalage d'odométrie possible).


| Le ramassage des Roches          | Le système de dépose   |
|-------------------------|------------------------|
| Avec son rouleau en mousse et son réservoir télescopique, Murray est capable d'ingérer les roches présentes dans les cratères.  |   Quand son réservoir est plein, Murray se dirige en direction de la zone de départ. Il est équipé d'un système de percuteurs lui permettant d'éjecter les boules par dessus la zone de départ, jusque dans le panier.   |
|  {{< illustration-center src=/robots/2017/Murray-grab.gif width="55%" >}} | {{< illustration-center src=/robots/2017/Murray-fire.gif width="60%" >}}  |


## La détection des adversaires 

Murray est équipé de 4 capteurs ultrasons pour détecter les robots adverses. Les capteurs scannent en permanence le terrain et envoient les données à la partie intelligence. L'intelligence du robot déduit, grâce à la position courante du robot, si les obstacles rencontrés sont des éléments de jeu, des robots adverses, ou encore des objets en dehors de la zone de jeu.

Bien que ce système soit fonctionnel et nous permette d'éviter la plupart des collisions, la détection reste assez bruitée, notamment lorsqu'un robot adverse utilise également des capteurs ultrasons. Pour palier à ce bruit, nous sommes actuellement en train de développer un système de localisation des robots adverses par balise.