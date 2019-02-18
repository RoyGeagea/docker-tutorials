# Installation

Nous allons utiliser une instance Ubuntu

* Étape 1:
  * Avant d’installer Docker, vous devez d’abord vérifier que vous avez la bonne version du noyau Linux en cours d’exécution. Docker est uniquement conçu pour fonctionner sur les versions 3.8 et supérieures du noyau Linux. Nous pouvons le faire en exécutant la commande suivante.
```sh
uname -a
```

* Étape 2:
  * Vous devez mettre à jour le système d’exploitation avec les derniers packages, ce qui peut être fait à l’aide de la commande suivante
```sh
sudo apt-get update
```

* Étape 3:
  * L'étape suivante consiste à installer les certificats nécessaires pour pouvoir utiliser le site Docker ultérieurement afin de télécharger les packages Docker nécessaires. Cela peut être fait avec la commande suivante.
```sh
sudo apt-get install apt-transport-https ca-certificates
```
