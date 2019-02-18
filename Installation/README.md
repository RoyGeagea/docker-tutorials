# Installation

![](containers.jpeg)

## Conditions préalables
Pour suivre ce tutoriel, vous aurez besoin des éléments suivants:

* Un serveur Ubuntu 16.04 configuré avec un utilisateur non root avec des privilèges sudo et un pare-feu de base, comme expliqué dans [le Guide de configuration initiale pour Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-16-04)
* Un compte sur [Docker Hub](https://hub.docker.com/) si vous souhaitez créer vos propres images et les transférer sur Docker Hub.

## Étape 1:
Avant d’installer Docker, vous devez d’abord vérifier que vous avez la bonne version du noyau Linux en cours d’exécution. Docker est uniquement conçu pour fonctionner sur les versions 3.8 et supérieures du noyau Linux. Nous pouvons le faire en exécutant la commande suivante.
```sh
$ uname -a
```

## Étape 2:
Vous devez mettre à jour le système d’exploitation avec les derniers packages, ce qui peut être fait à l’aide de la commande suivante
```sh
$ sudo apt-get update
```

## Étape 3:
L'étape suivante consiste à installer les certificats nécessaires pour pouvoir utiliser le site Docker ultérieurement afin de télécharger les packages Docker nécessaires. Cela peut être fait avec la commande suivante.
```sh
$ sudo apt-get install apt-transport-https ca-certificates
```

## Étape 4:
Le package d'installation de Docker disponible dans le référentiel officiel Ubuntu 16.04 peut ne pas être la dernière version. Pour obtenir cette dernière version, installez Docker à partir du référentiel officiel de Docker. Cette section vous montre comment faire exactement cela.

Tout d'abord, afin de vous assurer que les téléchargements sont valides, ajoutez la clé GPG du référentiel officiel Docker à votre système:
```sh
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
Ajoutez le référentiel Docker aux sources APT:
```sh
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```
Assurez-vous que vous êtes sur le point d'installer à partir du référentiel Docker au lieu du référentiel par défaut Ubuntu 16.04:
```sh
$ apt-cache policy docker-ce
```
Vous devriez voir une sortie similaire à celle-ci:
```sh
docker-ce:
  Installed: (none)
  Candidate: 18.06.1~ce~3-0~ubuntu
  Version table:
     18.06.1~ce~3-0~ubuntu 500
        500 https://download.docker.com/linux/ubuntu xenial/stable amd64 Packages
```
Enfin, installez Docker:
```sh
$ sudo apt-get install -y docker-ce
```
Docker should now be installed, the daemon started, and the process enabled to start on boot. Check that it's running:
```sh
$ sudo systemctl status docker
```
The output should be similar to the following, showing that the service is active and running:
```sh
Output
● docker.service - Docker Application Container Engine
   Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
   Active: active (running) since Thu 2018-10-18 20:28:23 UTC; 35s ago
     Docs: https://docs.docker.com
 Main PID: 13412 (dockerd)
   CGroup: /system.slice/docker.service
           ├─13412 /usr/bin/dockerd -H fd://
           └─13421 docker-containerd --config /var/run/docker/containerd/containerd.toml
```
L'installation de Docker vous donne maintenant non seulement le service Docker (démon), mais également l'utilitaire de ligne de commande Docker ou le client Docker. Nous verrons comment utiliser la commande docker plus loin dans ce tutoriel.