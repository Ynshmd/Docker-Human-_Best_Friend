# Projet "Humans Best Friend" ![icons8-chien-48](https://github.com/Ynshmd/Docker-Human-_Best_Friend/assets/118398845/8439c07b-6397-4693-b762-bd3f80a5054b)


## Description

Bienvenue dans le projet "Humans Best Friend", une application distribuée simple s'exécutant sur plusieurs conteneurs Docker. Cette solution utilise Python,   Redis pour la messagerie, et PostgreSQL pour le stockage.

## Prérequis![icons8-docker-48](https://github.com/Ynshmd/Docker-Human-_Best_Friend/assets/118398845/89e4cbb0-651f-4a49-9c7d-d2afe568488c)


Assurez-vous d'avoir installé Docker et Docker Compose sur votre machine. Suivez la documentation Docker pour les instructions d'installation si vous ne l'avez pas déjà fait.

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Structure du Projet

Le projet est composé de plusieurs services Docker :

- `backend-api` : Service API pour la gestion des données.
- `vote` : Service Python écoutant sur le port 80.
- `worker` : Service .NET dépendant de Redis et de la base de données.
- `seed-data` : Service Python pour générer des données initiales.
- `result` : Service Node.js exposé sur le port 5001.

## Instructions d'Installation

1. Clonez le dépôt sur votre machine.

    ```bash
    git clone https://github.com/Ynshmd/ynov-resources.git
    cd 2023/m2/dataeng/humans-best-friend
    ```

2.Installation de redis et postgre
    ```bash
   docker pull redis
    ````

````bash
    docker pull postgres:15-alpine
   ````
3.  TAG

```bash
   docker tag postgres:15-alpine localhost:5000/postgres:15-alpine
````

```bash
 docker tag redis:latest localhost:5000/redis:latest
````

4. Créez un fichier `docker-compose.build.yml` pour construire les images des applications à partir des Dockerfiles.

    ```yaml
    docker compose  -f docker-compose.build.yml up -d
    ```



5. Créez un fichier `docker-compose.yml` pour déployer l'application.

    ```yaml
    docker-compose.yml
    ```

6. Déployez l'application.

    ```bash
    docker compose up -d
    ```

## Accès aux Services


- Vote Service : [http://localhost:5005](http://localhost:5005)
- Worker Service : Intégré dans le réseau humansbestfriend-network
- Seed Data Service : Intégré dans le réseau humansbestfriend-network
- Result Service : [http://localhost:5004](http://localhost:5004)





## Auteurs

- [FAHEM WASSIL , HAMDAOUI YANIS](https://github.com/votre-utilisateur)


