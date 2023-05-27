# CYSHOP

Damien FERNANDES
Deo ZANTOKO
Tristan DELALONDE

MEF1 Readme Projet CY-SHOP

Notre projet CY-SHOP est un programme C qui permet à l'utilisateur de gérer les stocks et les clients. Pour commencer, nous avons créé un dossier "shop" contenant tous les fichiers de différentes fonctions. L'utilisateur doit ouvrir l'invite de commande et se placer dans le répertoire "Shop" où se trouvent tous les fichiers du dossier "shop". Ensuite, il doit exécuter la commande suivante : "make && shop" pour compiler et exécuter le programme.

La commande "make" compile le projet en exécutant le contenu du fichier "Makefile" et produit un programme exécutable nommé "shop.exe". Ensuite, la commande "shop" permet simplement d'exécuter le programme exécutable "shop.exe", d'où la commande "make && shop".

Le système de gestion de magasin se compose des fichiers suivants :
- "main.c" : fichier principal du programme qui contient le point d'entrée de l'application.
- "fonctions.c" : fichier contenant diverses fonctions utilisées dans le programme.
- "fonction.h" : fichier d'en-tête déclarant les prototypes de fonction et les définitions de structure.

Le programme offre deux modes de fonctionnement :
1. Mode Gestion :
   Ce mode permet à l'utilisateur de gérer l'inventaire de la boutique. Dans ce mode, l'utilisateur verra automatiquement les produits en rupture de stock (stock égal à 0) ainsi que les 5 produits dont les stocks sont les plus bas (supérieurs à 0). L'utilisateur pourra également voir la charge actuelle du magasin, ce qui lui permet de connaître l'espace restant en magasin pour le réapprovisionnement. Le mode Gestion offre également les options suivantes :
   - Afficher la liste complète des produits : permet à l'utilisateur de voir la liste de tous les produits disponibles en magasin.
   - Augmenter le stock d'un produit : l'utilisateur peut augmenter la quantité de stock d'un produit en spécifiant son numéro de référence.
   - Chercher un produit par son nom : l'utilisateur peut rechercher un produit spécifique en utilisant son nom.
   - Chercher un produit par sa référence : l'utilisateur peut rechercher un produit en utilisant son numéro de référence.
   - Quitter le mode Gestion : permet à l'utilisateur de revenir au menu principal du programme.

2. Mode Achat :
   Ce mode permet à l'utilisateur de gérer les achats des clients. Dans ce mode, l'utilisateur verra automatiquement la liste complète de tous les produits disponibles, incluant leur quantité, leur numéro de référence, leur taille et leur prix. Le mode Achat offre les options suivantes :
   - Faire un achat : l'utilisateur peut effectuer un achat en fournissant son nom, son prénom, le numéro de référence du produit et la quantité souhaitée. Si le fichier de l'utilisateur n'existe pas au moment où il renseigne ses informations, un nouveau fichier sera créé et sauvegardé directement dans les fichiers CSV (Comma-Separated Values) qui seront expliqués ultérieurement.
   - Afficher les informations d'un client : l'utilisateur peut consulter l'historique des achats d'un client en spécifiant simplement son nom et son prénom.
   - Quitter le mode Achat : permet à l'utilisateur de revenir au menu principal.

Le programme lit et enregistre les informations sur les produits à partir/vers un fichier CSV nommé "produits.csv" dans le répertoire "produits". De même, les informations client sont lues et enregistrées dans des fichiers CSV individuels en fonction du nom du client dans le répertoire "client". Il est important de s'assurer que les fichiers CSV sont correctement formatés avec des colonnes correspondant aux définitions de structure dans le code, car tout écart peut entraîner un comportement anormal du programme.
