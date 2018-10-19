# Unsecure project
Le site Unsecure est un projet de site internet Russe

Vous pouvez récupérer ce projet en clonant ce repository sur votre environnement de développement local:
```bash
git clone https://github.com/ESGI-IW1-GROUPE3/Unsecure.git
```
Vous pourrez contribuer en effectuant un fork de ce projet directement vers votre compte github, pour cela cliquez sur le bouton fork présent en haut à gauche du projet.

## Lancer l'environnement

Pour vos développement, vous pouvez tester les modifications sur le projet en l'exécutant directement via un environnement docker.

Après avoir cloné le projet, lancez la commande suivante à la racine de votre projet:

```bash
docker-compose up
```

Vous devriez obtenir un environnement fonctionnel accessible depuis l'URL localhost:8080 (ou 192.168.99.100:8080 si vous utilisez docker toolbox).

Vous pouvez accéder à la base de données via l'interface adminer à l'adresse localhost:8081 (ou 192.168.99.100:8081 si vous utilisez docker toolbox).

Pour l'accès à la base de donnée, vous pouvez depuis adminer utiliser les accès suivants:

```
id: docker
password: docker
host: mysql
```

Il sera nécessaire avant de pouvoir accéder au site, de lancer l'installation des dépendences composer en exécutant la commande suivante à la racine du projet:
```bash
composer install
```

Enfin, pour que le site puisse communiquer avec la base de données, il nous faudra configurer le fichier app/config/parameters.yml et définir la configuration suivante:
```bash
parameters:
    database_host: mysql
    database_port: 3306
    database_name: docker
    database_user: root
    database_password: docker
    mailer_transport: smtp
    mailer_host: 127.0.0.1
    mailer_user: null
    mailer_password: null
    secret: ThisTokenIsNotSoSecretChangeIt
```
