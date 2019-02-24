# Fonctionnement de Kubernetes

Dans ce chapitre, nous verrons comment installer Kubernetes via kubeadm. C'est un outil qui aide à l'installation de Kubernetes. Allons-y étape par étape pour apprendre à installer Kubernetes.

## Étape 1
Assurez-vous que la version du serveur Ubuntu sur laquelle vous travaillez est 16.04.

## Étape 2
Assurez-vous de générer une clé ssh pouvant être utilisée pour la connexion ssh. Vous pouvez le faire en utilisant la commande suivante.
```sh
$ ssh-keygen 
```

## Étape 3
Ensuite, en fonction de votre version d’Ubuntu, vous devrez ajouter le site correspondant au fichier docker.list pour le gestionnaire de paquets apt, afin qu’il puisse détecter les paquets Kubernetes sur le site kubernetes et les télécharger. en conséquence.

Nous pouvons le faire en utilisant les commandes suivantes.
```sh
$ curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add -  
echo "deb http://apt.kubernetes.io/ kubernetes-xenial main” | sudo tee /etc/apt/sources.list.d/docker.list 
```

## Étape 4
Nous publions ensuite une mise à jour d'apt-get pour nous assurer que tous les paquets sont téléchargés sur le serveur Ubuntu.

## Étape 5
Installez le package Docker comme indiqué dans les chapitres précédents.

## Étape 6
Il est maintenant temps d’installer kubernetes en installant les packages suivants:
```sh
$ apt-get install –y kubelet kubeadm kubectl kubernetes-cni 
```

## Étape 7
Une fois tous les packages kubernetes téléchargés, il est temps de démarrer le contrôleur kubernetes à l’aide de la commande suivante:
```sh
$ kubeadm init 
```

Une fois cela fait, vous obtiendrez un message indiquant que le maître est opérationnel et que les nœuds peuvent maintenant rejoindre le cluster.