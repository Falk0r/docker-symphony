# Server Nginx with Symphony 5

## Monter l’image
```bash
docker-compose up -d
docker ps
docker exec -ti id-image-symfony5_php-fpm bash
```

## Télécharger Symfony
Dans l’image Docker, via le bash :
```bash
clear && ls
git config --global user.email "your@email.fr"
git config --global user.name "your name"
symfony new mon_projet --full # https://symfony.com/doc/current/setup.html
```
Lancer le serveur interne de Symfony
Dans l’image Docker, via le bash :
```bash
cd mon_projet
symfony server:start
```
Connexion Symfony – MySQL : fichier .env
```env
DATABASE_URL=mysql://root:root@mysql:3306/test?serverVersion=5.7
```
## PhpMyAdmin
Pour accéder à phpMyAdmin :
- url : [8080](http://localhost:8080)
- login : root
- mot de passe : root

## Page d’accueil projet Symfony
Pour accéder au projet Symfony :
- url : [5000](http://localhost:5000)