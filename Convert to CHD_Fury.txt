@echo off
setlocal enabledelayedexpansion

REM Demander à l'utilisateur de saisir le répertoire racine
echo Veuillez entrer le chemin du répertoire racine à scanner (par exemple C:\Fullset PSX) :
set /p root_dir=

REM Vérifier si le dossier existe
if not exist "%root_dir%" (
    echo Le répertoire spécifié n'existe pas. Veuillez vérifier le chemin et réessayer.
    pause
    exit /b
)

REM Parcours récursif des fichiers .cue et .gdi
for /r "%root_dir%" %%i in (*.cue *.gdi) do (
    REM Définir le chemin de sortie pour le fichier .chd dans le même dossier que le fichier source
    set output_file=%%~dpi%%~ni.chd

    REM Vérifier si le fichier .chd existe déjà
    if exist "!output_file!" (
        echo Le fichier .chd existe déjà : !output_file!. Ignoré.
    ) else (
        REM Afficher le fichier en cours de traitement
        echo Traitement de : %%i

        REM Conversion du fichier en .chd
        chdman createcd -i "%%i" -o "!output_file!"

        REM Vérifier si la conversion a réussi
        if errorlevel 1 (
            echo Erreur lors de la conversion de %%i
        ) else (
            echo Conversion réussie : !output_file!
        )
    )
)

echo Conversion terminée.
pause
