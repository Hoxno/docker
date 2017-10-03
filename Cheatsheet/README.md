# Pense bête des commandes Docker

* Créer une image en utilisant le fichier Dockerfile
```
docker build -t friendlyname .
```
* Lance `friendlyname` en le port 4000 vers 80
```
docker run -p 4000:80 friendlyname
```
* Même chose, mais en mode détacher
```
docker run -d -p 4000:80 friendlyname
```
* Liste tous les containers lancer
```
docker container ls
```
* Liste tous les container, même ce qui ne sont pas démmarrer
```
docker container ls -a
```
* Arrêter un container spécifique
```
docker container stop <hash>
```
* Forcer l'arrêt d'un container spécifique
```
docker container kill <hash>
```
* Supprimer un container spécifique de sa machine
```
docker container rm <hash>
```
* Supprimer tous les containers
```
docker container rm $(docker container ls -a -q)
```
* Liste tous les images sur sa machine
```
docker image ls -a
```
* Supprimer une image spécifique de sa machine
```
docker image rm <image id>
```
* Supprimer tous les images de sa machine
```
docker image rm $(docker image ls -a -q)
```
* Se connecter à son compte Docker
```
docker login
```
* Tagger une <image> pour l'uploader vers le Docker hub
```
docker tag <image> username/repository:tag
```
* Uploader l'image tagger vers le Docker Hub
```
docker push username/repository:tag
```
* Lancer une image depuis le Docker Hub
```
docker run username/repository:tag
```
***
# Pense bête pour docker-compose
* Demarrer des containers
```
docker-compose up
```
* Démmarer des container en arrière plan
```
docker-compose up -d
```
* Arrêter des containers
```
docker-compose stop
```
