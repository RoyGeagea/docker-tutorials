# Liaison de conteneur

La liaison de conteneurs permet à plusieurs conteneurs de se lier les uns aux autres. C'est une meilleure option que d'exposer les ports. Allons-y étape par étape et apprenons comment cela fonctionne.

## Étape 1
Téléchargez l'image Jenkins, si elle n'est pas déjà présente, à l'aide de la commande Pull Jenkins.
```sh
$ sudo docker pull jenkins
```

## Étape 2 
Une fois l'image disponible, exécutez le conteneur, mais cette fois-ci, vous pouvez spécifier un nom pour le conteneur à l'aide de l'option –-name. Ce sera notre conteneur source.
```sh
$ sudo docker run --name=jenkinsa -d jenkins
```

## Étape 3
Ensuite, il est temps de lancer le conteneur de destination, mais cette fois-ci, nous allons le lier à notre conteneur source. Pour notre conteneur de destination, nous utiliserons l'image standard Ubuntu.
```sh
$ sudo docker run --name=reca --link=jenkinsa:alias-src -it ubuntu:latest /bin/bash
```



