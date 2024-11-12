Je SUIS ICI
Les commandes essentielles d’un container Docker :

# Inception

**Docker** 

```cpp
Docker est un outil qui te permet de créer, déployer et exécuter des applications dans des environnements isolés appelés conteneurs. Imagine Docker comme une sorte de boîte hermétique dans laquelle tu mets ton application et tout ce dont elle a besoin pour fonctionner (code source, bibliothèques, dépendances, etc.). Cela permet de s'assurer que ton application fonctionne de la même façon, que ce soit sur ton ordinateur, sur un serveur distant, ou dans le cloud.
```

Qu'est-ce qu'une image Docker ? 📦

```cpp
Une image Docker est un modèle (ou un "template") figé qui contient tout ce dont ton application a besoin pour fonctionner :
- Le code de l'application.
- Les bibliothèques et dépendances.
- Les fichiers de configuration.
- Un système d'exploitation minimal (comme Linux).

Une image est statique et ne change pas une fois créée.
```

**Le cycle d'utilisation du Docker** 

```cpp
1. Construire une image :
Tu crées une image à partir d'un fichier appelé Dockerfile.
2. Lancer un conteneur :
Une fois que tu as une image, tu peux lancer un conteneur avec la commande docker run.
3. Gérer les conteneurs :
Tu peux démarrer, arrêter, ou supprimer des conteneurs selon tes besoins.
```

**Guide**

1. Création d'un machine virtuel.
2. 
3. Utiliser Docker Compose.


**Creation du container NGINX**

```c
Chemin :
- srcs/nginx/Dockerfile
```

FROM debian:buster

**Crédit** 

https://tuto.grademe.fr/inception/#sujet
