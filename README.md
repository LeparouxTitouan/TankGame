# TankGame

## Présentation
L’objectif de ce projet est de réaliser en langage C, Un jeu de **bataille de tanks**. Le but étant d’éliminer tous les tanks ennemis tout en protégeant le petit oiseau qu’on appellera le « Titi ».

#### Lancer le jeu

Le projet sera sous forme de zip qu’il faudra décompresser sur son espace de travail. Ce fichier zip contient un makefile et ce rapport. Pour lancer le projet, il faut se rendre sur le terminal, se placer sur le dossier `Projet/src` et taper la commande `make`. Ainsi, le projet s’exécutera.

Le projet est très facile à exécuter grâce au makefile. Lorsque la commande make est entrée, l’ordinateur cherche un fichier intitulé makefile qui va contenir les instructions pour compiler et exécuter le programme automatiquement. Le makefile va exécuter les fichiers exécutables grâce à la commande gcc.

> **NB :** Ce projet est susceptible de mal s’afficher sur quelques écrans à cause des soucis de pixels. On l’a donc programmé de façon à ce qu’il s’affiche bien sur les ordinateurs de l’école ESIEAParis. 

## Prérequis

Ce projet nécessite des connaissances en langage C pour pouvoir y intégrer des couleurs, déplacer un char, générer des tanks ennemis en fonction du niveau de difficulté, détruire les murs de l’environnement grâce à l’utilisation de missiles et gérer les niveaux à l’aide de menus. 

- Les listes chainées
- Les tableaux
- Les structures
- La librairie SDL
- Les entrées clavier
- Le Makefile
  
## Le Jeu

#### Environnement

La carte est générée à partir d’un fichier texte `.txt` permettant ainsi de pouvoir facilement modifier la carte. 

#### Affichage

Pour réaliser l’affichage nous avons préféré utiliser la **librairie SDL** à l’affichage en console. Cela nous a permis d’afficher des éléments en pixels au lieu de simplement se limiter aux caractères ascii. Ainsi l’affichage d’image nous a permis de réaliser un design plus complexe.

#### Déplacement

Les déplacements ont été implémenté à l’aide de la librairie SDL. Ainsi nous avons récupéré les entrées des flèches directionnelles, du bouton entré et de la barre d’espace.

#### Tank Ennemis

Les tanks ennemis sont générés en début de partie, et leurs déplacements sont réalisés à l’aide d’une **fonction aléatoire**. Nous avons cependant privilégié certains mouvements afin de rendre ces déplacements plus fluides et logiques pour le joueur. 

#### Missiles / Rockets

Les tanks (joueur/ennemis) peuvent réaliser des tirs de missiles afin de pouvoir détruire les murs et les tanks.

#### Niveau de vie 

Les tanks possèdent 3 vies, ainsi ils peuvent subir 3 percutions de missile avant de mourir. La couleur du tank varie en fonction de son niveau de vie (Joueur : <img src="https://github.com/LeparouxTitouan/TankGame/blob/master/src/img/tank/tankB_3_up.png" width="15" /> → <img src="https://github.com/LeparouxTitouan/TankGame/blob/master/src/img/tank/tankB_2_up.png" width="15" /> → <img src="https://github.com/LeparouxTitouan/TankGame/blob/master/src/img/tank/tankB_1_up.png" width="15" /> / Ennemis : <img src="https://github.com/LeparouxTitouan/TankGame/blob/master/src/img/tank/tankG_3_up.png" width="15" /> → <img src="https://github.com/LeparouxTitouan/TankGame/blob/master/src/img/tank/tankG_2_up.png" width="15" /> → <img src="https://github.com/LeparouxTitouan/TankGame/blob/master/src/img/tank/tankG_1_up.png" width="15" />) même avec les murs qui eux n’ont que deux vies (<img src="https://github.com/LeparouxTitouan/TankGame/blob/master/src/img/wall/wall.png" width="15" /> → <img src="https://github.com/LeparouxTitouan/TankGame/blob/master/src/img/wall/wall_used.png" width="15" /> → <img src="https://github.com/LeparouxTitouan/TankGame/blob/master/src/img/wall/deep_durt.png" width="15" />)

#### Niveau de jeu 

Comme dit précédemment, il y a plusieurs niveaux de jeu : 
- **Facile :** il y a un tank ennemi à éliminer et le « Titi » à protéger
- **Intermédiaire :** il y a deux tanks ennemis à éliminer et le « Titi » à protéger 
- **Difficile :** il y a quatre tanks ennemis à éliminer et le « Titi » à protéger

## Conclusion

Le problème majeur que nous avons rencontré durant l’écriture du code du jeu fut l’implémentation des listes chainées. En effet, il s’agit d’un stockage d’informations que nous n’avions jamais utilisé.  
 
Ce projet fut très instructif, il nous a permis d’implémenter une bonne étendue des fonctionnalités du C ainsi que de la librairie SDL qui permet de réaliser de bonnes interfaces graphiques. Le choix de faire un projet de création d’un jeu était motivant dans l’écriture du code et dans l’inspiration pour créer les designs et les fonctionnalités.  
