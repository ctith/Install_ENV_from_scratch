# Installation d'un environnement de dev (x64) sur Windows 10

## Installer linux ubuntu sur Windows 10
![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/01.PNG?raw=true)
---------
![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/02.PNG?raw=true)
-------------
![](https://github.com/ctith/Install_ENV_from_scratch/blob/master/Env_screenshot/03.PNG?raw=true)

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

## Installer IntelliJ entreprise
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
