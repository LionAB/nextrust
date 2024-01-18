# Project Title


## Tech Stack

**Client:** NEXT.JS

**Server:** RUST,SERDE (serialize)

**DB:** POSTGRES

**AUTRE** DOCKER,DOCKER COMPOSE




Une simple application FullStack en full découverte


# SETUP


```bash
    git init
    touch .gitignore
    *node_modules
    touch compose.yaml
```
## DB
  1. Construire la DB
```bash
    docker compose up -d
```
  2. Check container 
```bash
    docker ps -a
```
3. Rentrer dans le container
```bash
    docker exec -it db psql -U postgres
```
4. Entrer 
```bash
    \l
    \dt
```
## BACKEND
1. Créer Backend app
```bash
    cargo new backend
```
2. Ajouter les dépendances dans Cargo.toml
```bash
    postgres = "0.19"
    serde = "1.0"
    serde_json = "1.0"
    serde_derive = "1.0"
```
Postgres est le pilote Postgres pour Rust.
Serde est une bibliothèque pour la sérialisation et la désérialisation.
Serde_json est une bibliothèque spécifique pour JSON.
Serde_derive est une bibliothèque pour dériver les traits Serialize et Deserialize (macro).

3. 🐳 Dockerize the backend
```bash
touch .dockerignore rust.dockerfile
```
4. Builder l'image 
```bash
docker compose build
```

## FRONTEND

## Installation

Install with npm

```bash
  npm install my-project
  cd my-project
```
Dockerize Front
