# Convertisseur de fichiers `.cue` et `.gdi` en `.chd`

Ce script batch Windows permet de convertir des fichiers `.cue` et `.gdi` en fichiers `.chd` de manière automatique, tout en recherchant récursivement dans un répertoire et ses sous-dossiers.

## Fonctionnalités

- **Conversion en masse** : Convertit tous les fichiers `.cue` et `.gdi` trouvés dans un répertoire donné.
- **Gestion des doublons** : Ignore les fichiers déjà convertis.
- **Rapports** : Affiche les erreurs ou succès pour chaque fichier traité.

## Prérequis

1. **chdman** : Téléchargez et installez l'outil `chdman` (inclus avec les outils de MAME). Assurez-vous qu'il est accessible depuis la ligne de commande (soit en l'ajoutant au `PATH`, soit en le plaçant dans le même dossier que le script).
   - [Télécharger chdman](https://www.mamedev.org/release.html)
2. Windows avec un terminal compatible pour exécuter des scripts `.bat`.

## Utilisation

1. Téléchargez le script `convert_to_CHD.bat`.
2. Placez-le dans un dossier accessible.
3. Exécutez le script :
   - Double-cliquez sur le fichier `convert_to_CHD.bat` **ou**
   - Ouvrez un terminal, naviguez jusqu'au dossier contenant le script et exécutez :
     ```cmd
     convert_to_CHD.bat
     ```
4. Saisissez le chemin du répertoire contenant vos fichiers `.cue` et `.gdi`.

## Exemple

### Étapes typiques :

1. Vous avez un dossier contenant les fichiers `.cue` et `.gdi` :  



## Remarques

- Le script ignore les fichiers déjà convertis (présence de `.chd`).
- En cas d'erreur (ex : fichier corrompu ou problème de configuration), l'erreur sera affichée dans le terminal.
- `chdman` est obligatoire pour ce script.

## Licence

Ce script est fourni "tel quel", sans garantie. Vous pouvez l'utiliser, le modifier et le partager librement.

Le script utilise Chdman développé par MAME
