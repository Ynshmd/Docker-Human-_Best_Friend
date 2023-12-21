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
    git clone https://github.com/pascalito007/ynov-resources.git
    cd 2023/m2/dataeng/humans-best-friend
    ```

2. Créez un fichier `docker-compose.build.yml` pour construire les images des applications à partir du Dockerfile.

    ```yaml
    # Votre contenu pour docker-compose.build.yml
    ```

3. Construisez les images sans exécuter de conteneurs.

    ```bash
    docker-compose -f docker-compose.build.yml build
    ```

4. Créez un fichier `docker-compose.yml` pour déployer l'application.

    ```yaml
    # Votre contenu pour docker-compose.yml
    ```

5. Déployez l'application.

    ```bash
    docker-compose up -d
    ```

## Accès aux Services

- Backend API : [http://localhost:3000](http://localhost:3000)
- Vote Service : [http://localhost:5002](http://localhost:5002)
- Worker Service : Intégré dans le réseau back-tier
- Seed Data Service : Intégré dans le réseau front-tier
- Result Service : [http://localhost:5001](http://localhost:5001)

## Personnalisation

Vous pouvez personnaliser le projet en modifiant les fichiers de configuration et les Dockerfiles selon vos besoins.

## Contributions

Les contributions sont les bienvenues! Avant de contribuer, veuillez lire notre [guide de contribution](CONTRIBUTING.md).

## Auteurs

- [FAHEM WASSIL , HAMDAOUI YANIS](https://github.com/votre-utilisateur)


