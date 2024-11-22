# Convert-to-CHD

Présentation du script
Ce script est un fichier batch Windows (.bat) permettant de convertir des fichiers .cue et .gdi en fichiers .chd dans un répertoire spécifié par l'utilisateur. Il utilise l'outil chdman pour effectuer la conversion.


## Fonctionnalités principales


### Recherche récursive :

Le script parcourt tous les sous-dossiers du répertoire spécifié à la recherche de fichiers .cue et .gdi.

### Conversion automatique :

Les fichiers trouvés sont convertis en .chd (un format compressé pour les images de disques).

### Ignorer les doublons :

Si un fichier .chd correspondant existe déjà, le fichier source est ignoré.

### Gestion des erreurs :

Le script vérifie le succès ou l'échec de chaque conversion et informe l'utilisateur.


## Prérequis :

L'outil chdman doit être installé et accessible depuis la ligne de commande (ajouté au PATH ou dans le même répertoire que le script).
Un environnement Windows avec support des scripts batch.
