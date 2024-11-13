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

1.Installer docker 
https://docs.docker.com/engine/install/debian/
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

puis faire le test
sudo docker run hello-world

Si cela fonctionne tu devrais voir ceci : 

Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
c1ec31eb5944: Pull complete 
Digest: sha256:d211f485f2dd1dee407a80973c8f129f00d54604d2c90732e8e320e5038a0348
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly. 

--------------------------------

si tu as cette erreur 
ERROR: permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied

sudo usermod -aG docker <user>
newgrp docker
docker ps
docker build -t nginx .

ps : chaque modification du Dockerfile tu dois faire un docker build -t nginx .
 (comme pour un make re)

------------
recuperer la config de base 
cd /etc/nginx/nginx.conf
fais un copier

aller dans le dossier conf puis dans le fichier nginx.conf 
fais le coller.

-------------
 
