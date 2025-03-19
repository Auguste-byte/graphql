# GraphQL Profile Page

## Description
Ce projet a pour objectif d'apprendre le langage de requête **GraphQL** en créant une page de profil utilisateur. L'application permet d'afficher les informations scolaires de l'utilisateur en interrogeant l'API **GraphQL** fournie par la plateforme Zone01 Normandie.

## Fonctionnalités

- **Authentification** :
  - Connexion avec `username:password` ou `email:password`.
  - Récupération d'un JWT via l'endpoint `https://zone01normandie.org/api/auth/signin`.
  - Déconnexion avec suppression du token.

- **Affichage du Profil** :
  - Identification de base de l'utilisateur.
  - Niveau de l'utilisateur
  - Ratio d'audit.
  - Compétences.

- **Graphiques Statistiques (SVG)** :
  - Compétences en %.
  - Ratio des audit.

## Installation et Exécution

### Prérequis
- Node.js installé
- Un compte sur [Zone01 Normandie](https://zone01normandie.org)

### Installation

1. Cloner le projet :
   ```bash
   git clone https://github.com/Auguste-byte/graphql
   ```

2. Installer les dépendances :
   ```bash
   npm install
   ```

3. Démarrer le serveur :
   ```bash
   npm run dev
   ```

## Utilisation

1. **Connexion** :
   - Saisir vos identifiants (username/email + password).
   - Le JWT est stocké et utilisé pour les requêtes GraphQL.

2. **Affichage du Profil** :
   - Les données sont récupérées et affichées dynamiquement.

3. **Visualisation des Statistiques** :
   - Des graphiques SVG interactifs affichent vos performances scolaires.

4. **Déconnexion** :
   - Bouton permettant de supprimer le JWT et revenir à l'écran de connexion.

## Technologies Utilisées
- **Frontend** : JavaScript
- **Authentification** : JWT (Bearer Token)
- **Graphiques** : SVG

## API GraphQL

- **Endpoint** : `https://zone01normandie.org/api/graphql-engine/v1/graphql`
- **Exemple de requête GraphQL** :
  ```graphql
  query GetUserInfo {
    user {
      id
      login
      xp
      skills {
        name
        level
      }
    }
  }
  ```
- **Headers nécessaires** :
  ```json
  {
    "Authorization": "Bearer <TOKEN>"
  }
  ```



## Auteur
- Louis PLEINTEL (https://github.com/Auguste-byte/)