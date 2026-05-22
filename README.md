# TP Docker POZOS - 2026

## Auteur
Marieme1123

## Description
Dockerisation de l'application student_list pour POZOS.
L'application permet d'afficher la liste des étudiants avec leur âge.
Elle est composée de deux modules : une API REST (Flask) et une application web (PHP/Apache).

## Architecture
- **API** : Flask Python (port 5000)
- **Website** : PHP Apache (port 80)
- **Registry** : Registre Docker privé (port 5001)
- **Registry UI** : Interface web du registre (port 8080)

## Structure du projet
student_list/
├── simple_api/
│   ├── Dockerfile
│   ├── student_age.py
│   ├── student_age.json
│   └── requirements.txt
├── website/
│   └── index.php
├── registry/
│   └── docker-compose.yml
└── docker-compose.yml
## Étapes réalisées

### ÉTAPE 1 — Clonage des repos
Clonage du repo du prof pour récupérer les fichiers sources :
```bash
git clone https://github.com/diranetafen/student-list.git
```
Clonage de notre repo de rendu :
```bash
git clone https://github.com/Marieme1123/student_list.git
```

### ÉTAPE 2 — Modification de index.php
Mise à jour de l'URL de l'API dans index.php :
```php
$url = 'http://api:5000/pozos/api/v1.0/get_student_ages';
```

### ÉTAPE 3 — Création du Dockerfile
Construction de l'image API basée sur python:3.13-slim.

### ÉTAPE 4 — Build et test de l'API seule


### ÉTAPE 5 — Test sur le navigateur


### ÉTAPE 6 — Déploiement avec Docker Compose


### ÉTAPE 7 — Application web


### ÉTAPE 8 — Registre Docker privé

