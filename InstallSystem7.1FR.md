# Comment préparer un disque System 7 français pour minivMac ?

Ce document décrit les étapes à suivre et les fichiers nécessaires pour créer un disque de taille 20 Mo pour la programmation HYPERCARD sous System 7.1 français

1. Création d'un HD vierge
1. Installer System 7.1 FR
1. Installer Hypercard 2.4
1. Installer Clip-IN, Clip-OUT
1. Installer Stuffit 4.0.1 et Dropstuff 4.0

dd if=/dev/zero of=HD32Hypercard.dsk count=40960

1. Création d'un HD vierge

La stack ddSyntax permet d'obtenir la ligne de commande à lancer dans le Terminal sous MacOS :

dd if=/dev/zero of=HD32Hypercard.dsk count=40960

Le fichier obtenu doit être initialisé. C'est réalisé à la première ouverture du .dsk dans minivMac.

![test](Images/initHD-1.png)
![test](Images/initHD-2.png)
![test](Images/initHD-3.png)



2. Installer System 7.1 FR
Pour cette étape, le dossier /installers/ sera nécessaire.

Quitter minivMac s'il est lancé.

* Aller dans le dossier /Installers/7.1FR
  
* Démarrer minivMac avec le disque "Install 1.img"

* Arrivé sur cet écran, faire glisser le disque préparé en 1 sur minivMac. Il ne se passe rien visuellement mais le disque a été monté et sera proposé sur l'écran suivant.

![Installation](Images/System7FR-Install-1.png)

* Vérifier que le disque HD est bien proposé en destination

![Installation](Images/System7FR-Install-2.png)



* Installer. À chaque demande de disquette, faire glisser le fichier correspondant sur minivMac. L'installation utilise les noms français pour désigner chaque disquette, mais les fichiers sur disque ont le nom anglais.

![Installation](Images/System7FR-Install-3.png)
  

* Petit piège : Les disquettes "Imprimantes" et "Polices" sont inversées. Quand "Polices" sera demandé, utilisez "Printers" et vice-versa.

![Installation](Images/System7FR-Install-4.png)

* Fin de l'installation

![Installation](Images/System7FR-Install-5.png)

3. Installer Hypercard 2.4

Cette installation requiert 3000 Ko de RAM, c'est normalement le cas à ce stade de l'installation. On utilisera les fichiers suivants :
- HyperCard241.img
- HyperProgramming.image
- Cooking with HyperTalk.dsk

![Installation](Images/3000Ko.png)

ATTENTION, ne pas utiliser l'installeur proposé sur l'écran initial.

![Installation](Images/HCbadInstaller.png)


Aller dans le dossier "Software Installers", puis dans "Hypercard Installer" et cliquer sur "Installer"

![Installation](Images/HyperCardInstaller.png)

Les deux autres fichiers s'installent par simple copie :

- HyperProgramming.image
- Cooking with HyperTalk.dsk

Ils sont facultatifs mais vivement conseillés.

4. Installer Clip-IN, Clip-OUT

Pour cette installation, utilisez le disque "MinivMac.dsk" :
- copier le contenu du disque sur le disque dur
![Installation](Images/MinivMacFolder.png)
- copier les fichier Clip-In et Clip-Out dans le dossier 
![Installation](Images/ClipIn-ClipOut.png)

5. Installer Stuffit 4.0.1 et Dropstuff 4.0

Cette installation se réalise avec les disquettes :

- stuffit_expander_40.dsk
- dropstuff_40.dsk

Il est requis de démarrer miniVmac sans charger les extensions (touche SHIFT enfoncée au démarrage).

## Ressources
Liste des modules nécessaires.

- ddSyntax.dsk
- /installers/
- HyperProgramming.image
- HyperCard241.img
- Cooking with HyperTalk.dsk
- MinivMac.dsk
- stuffit_expander_40.dsk
- dropstuff_40.dsk