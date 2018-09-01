# Installation d'un environnement de dev (x64) sur Windows 10

## Installer linux ubuntu sur Windows 10
![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/01.PNG?raw=true)
---------
![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/02.PNG?raw=true)
-------------
![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/03.PNG?raw=true)

#### Windows 10 :
- Si erreur 0x80070002, installer un [utilitaire de résolution de problème de Windows Update](https://support.microsoft.com/fr-fr/help/10164/fix-windows-update-errors) : https://aka.ms/wudiag
- Installer linux selon les étapes montrées ci-dessus et redémarrer l'ordinateur
- Si l'ordinateur ne détecte plus la carte wifi, ouvrir la console en mode administrateur : executer > cmd puis désactiver le parefeu avec la commande ci-dessous et redémarrer l'ordinateur
```shell
netsh advfirewall set allprofiles state off
```
- réactiver le parefeu dans le options windows ou avec la commande précédente en remplaçant off par on

## Installation de python

### Python 2.7 : https://www.python.org/downloads/
1. Exécutable python-2.7.6.amd64 : installer Python27 à la racine de C:/ 
2. Installer pip
```shell
ctith@L50T-036:/mnt/c/Python27$ sudo apt install python-pip
ctith@L50T-036:/mnt/c/Python27$ pip install --upgrade pip
```

### Python 3.6.4 : https://www.python.org/downloads/
1. Exécutable python-3.6.4 : installer Python36
2. Choisir une installation manuelle pour bien définir le chemin d'installation 
(Par défaut, il installe Python36 dans un environnement temporaire)
![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/py01.PNG?raw=true)
![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/py02.PNG?raw=true)

## Installer Git
1. Executable Git pour Windows x64 : https://git-scm.com/download/win
2. Cloner un dossier git
```shell
ctith@L50T-036:/mnt/c/Users/Fitec/Desktop$ git clone https://github.com/ctith/Kafka
```

## Installer Java JDK
1. Executable pour windows x64 : http://www.oracle.com/technetwork/java/javase/downloads/jdk9-downloads-3848520.html
2. rajouter une variable JAVA_HOME dans les variables utilisateurs en précisant le chemin pointant vers le JDK C:\Program Files\Java\jdk1.8.0_161

![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/env01.PNG?raw=true)

## Utiliser IntelliJ entreprise
Installer IntelliJ

Installer IDE Python sur IntelliJ :
settings > plugins > install jetbrains plugins > plugin python community

![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/env03.PNG?raw=true)

## Installer dépendance Maven
Utilisation de projet maven pour inclure des dépendances automatiquement : 
on utilise le maven extérieur à intelliJ pour pouvoir lancer plusieurs projets donc :
1. télécharger et dézipper la dépendance apache-maven - 3.5.3 où on veut https://maven.apache.org/download.cgi
2. récupérer le chemin du dossier et le rajouter dans la variable système path C:\Program Files\JetBrains\apache-maven-3.5.3\bin

![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/env02.PNG?raw=true)

### Installation de Kafka 
#### Sous windows

[https://kafka.apache.org/downloads](https://kafka.apache.org/downloads)
télécharger la version correspondant à la version qu’on a de scala, puis décompresser en local

#### Sous linux
```
ctith@L50T-048:/mnt/c/Users/Fitec$ wget http://apache.mindstudios.com/kafka/1.0.1/kafka_2.11-1.0.1.tgz

ctith@L50T-048:/mnt/c/Users/Fitec$ tar -xf kafka_2.11-1.0.1.tgz
```
## Installer environnement développement web

### Installer Wampserver
Télécharger l'exécutable wampserver et l'installer dans c:/wamp64
https://sourceforge.net/projects/wampserver/

Suivre le tuto : https://openclassrooms.com/fr/courses/918836-concevez-votre-site-web-avec-php-et-mysql/4237816-preparer-son-environnement-de-travail

Vérifier que wamp a bien été installé : https://openclassrooms.com/fr/courses/3619856-developpez-votre-site-web-avec-le-framework-symfony/3620140-symfony-un-framework-php#/id/r-3620139
