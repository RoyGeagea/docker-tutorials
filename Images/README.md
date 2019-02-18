# Images

![](docker-flow.png)

Dans Docker, tout est basé sur Images. Une image est une combinaison d'un système de fichiers et de paramètres. Prenons un exemple de la commande suivante dans Docker.
```sh
$ docker run hello-world 
```
* La commande Docker est spécifique et indique au programme Docker du système d’exploitation qu’il faut faire quelque chose.
* La commande run est utilisée pour indiquer que nous voulons créer une instance d'une image, qui s'appelle alors un conteneur.
* Enfin, "hello-world" représente l'image à partir de laquelle le conteneur est fabriqué.

## Exemple:
Voyons comment utiliser l’image CentOS disponible dans Docker Hub pour exécuter CentOS sur notre ordinateur Ubuntu. Nous pouvons le faire en exécutant la commande suivante sur notre machine Ubuntu:
```sh
$ sudo docker run centos –it /bin/bash
```
* Nous utilisons la commande sudo pour nous assurer qu’elle fonctionne avec un accès root.
* Centos est le nom de l'image que nous voulons télécharger depuis Docker Hub et installer sur notre machine Ubuntu.
* Il est utilisé pour mentionner que nous voulons fonctionner en mode interactif.
* /bin/bash est utilisé pour exécuter le shell bash une fois que CentOS est opérationnel.

## Displaying Docker Images:
Pour voir la liste des images Docker sur le système, vous pouvez exécuter la commande suivante.
```sh
$ sudo docker images
```
* Output:

![](dockerimages.png)

Chaque image a les attributs suivants:
* TAG − This is used to logically tag images.
* Image ID − This is used to uniquely identify the image.
* Created − The number of days since the image was created.
* Size − The size of the image.
