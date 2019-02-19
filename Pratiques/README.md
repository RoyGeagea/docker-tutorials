# Travailler avec des conteneurs

Dans ce chapitre, nous explorerons en détail ce que nous pouvons faire avec les conteneurs.

## docker top:
Avec cette commande, vous pouvez voir les principaux processus dans un conteneur.
```sh
$ sudo docker top ContainerID
```
* ContainerID - Il s'agit de l'ID de conteneur pour lequel vous souhaitez voir les principaux processus.

## docker stop:
Cette commande est utilisée pour arrêter un conteneur en cours d'exécution.
```sh
$ sudo docker stop ContainerID 
```

## docker rm:
Cette commande est utilisée pour supprimer un conteneur.
```sh
$ sudo docker rm ContainerID  
```

## docker stats:
Cette commande est utilisée pour fournir les statistiques d'un conteneur en cours d'exécution.
```sh
$ sudo docker stats ContainerID  
```

output:

![](stats.png)

## docker attach:
Cette commande est utilisée pour attacher à un conteneur en cours d'exécution.
```sh
$ sudo docker attach ContainerID   
```

## docker pause:
Cette commande est utilisée pour suspendre les processus dans un conteneur en cours d'exécution.
```sh
$ sudo docker pause ContainerID    
```

## docker unpause:
Cette commande permet de suspendre les processus dans un conteneur en cours d'exécution.
```sh
$ sudo docker unpause ContainerID    
```

## docker kill:
Cette commande est utilisée pour tuer les processus dans un conteneur en cours d'exécution.
```sh
$ sudo docker kill ContainerID    
```

## Container Lifecycle:
L'illustration suivante explique le cycle de vie complet d'un conteneur Docker.

![](lifecycle.png)















