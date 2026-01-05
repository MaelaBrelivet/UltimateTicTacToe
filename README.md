# Ultimate Tic-Tac-Toe – IA Minimax & Mode en ligne

## Description
Ce projet implémente le jeu Ultimate Tic-Tac-Toe avec une interface graphique et plusieurs modes de jeu :
- Joueur contre joueur
- Joueur contre IA
- Jeu en ligne (client/serveur)
- IA basée sur l’algorithme Minimax

L’interface est développée avec Pygame, et le jeu peut être joué localement ou à distance via des sockets.

## Fonctionnalités principales
- Ultimate Tic-Tac-Toe (règles complètes)
- IA utilisant Minimax
- Interface graphique avec Pygame
- Mode multijoueur en ligne (host / guest)
- IA jouable en local ou en ligne
- Optimisation via mémoïsation

## Intelligence Artificielle
L’IA est implémentée dans le fichier `AIminimaxV1.py`.  
Caractéristiques :
- Algorithme Minimax récursif
- Gestion de la profondeur de recherche
- Fonction d’évaluation des états du plateau
- Mémoïsation pour optimiser les calculs

Elle peut être utilisée :
- en mode local (`mainAI.py`)
- comme joueur distant (guest ou host)

## Installation et exécution
1. Installer les dépendances :
pip install pygame pygame_gui numpy

2. Lancer le menu principal :
python menu.py

Depuis le menu, il est possible de :
- Jouer en local
- Jouer contre l’IA
- Héberger une partie en ligne
- Rejoindre une partie en ligne

### Mode en ligne
Fichiers principaux :
- `server.py` : serveur du jeu
- `client.py` : client
- `tictactoe_online_host.py` et `tictactoe_online_guest.py` : modes en ligne
- Versions IA disponibles (`*_AI.py`)

Le mode en ligne repose sur une communication via sockets TCP.

## Règles du jeu
- Le plateau principal contient 9 sous-plateaux
- Le coup joué détermine le sous-plateau où le prochain joueur doit jouer
- Un sous-plateau gagné est verrouillé
- Le premier joueur à aligner 3 sous-plateaux gagnés remporte la partie

## Auteur
Maëla Brelivet, Lucas Delhommeau, Wissam Mecherfi, Nour El Habib – Étudiants ingénieurs à EURECOM

## Licence
Ce projet est sous licence MIT (voir le fichier LICENSE)

## Améliorations possibles
- Fonction heuristique améliorée
- IA avec niveaux de difficulté
- Sauvegarde et reprise de parties
- Mode tournoi
