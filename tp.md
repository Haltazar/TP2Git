
# Mini Cours : Git Flow, Gitmoji, et Plan Type README

## 1. Git Flow

**Git Flow** est une méthodologie de gestion de branches pour Git. Elle structure le processus de développement et est souvent utilisée par des équipes pour organiser les versions et les déploiements.

### Branches principales :

- **master/main** : C'est la branche de production. Le code ici est stable et prêt à être livré.
- **develop** : C'est la branche de développement principal où toutes les nouvelles fonctionnalités sont intégrées.

### Branches de support :

- **feature** : Une branche pour chaque nouvelle fonctionnalité. Elle part de `develop` et fusionne dans `develop` une fois la fonctionnalité terminée.

  ```bash
  git checkout develop
  git checkout -b feature/nouvelle-fonctionnalité

- **bugfix** : Une branche pour chaque correction de bug. Elle part de `develop` et fusionne dans `develop` une fois la correction terminée.

  ```bash
  git checkout develop
  git checkout -b bugfix/correction-de-bug
  ```

- **hotfix** : Une branche pour chaque correction de bug urgente. Elle part de `master` et fusionne dans `master` une fois la correction terminée.

  ```bash
  git checkout master
  git checkout -b hotfix/correction-de-bug-urgente
  ```

### Merge des branches :

- **Merge de la branche `develop` dans `master`**

  ```bash
  git checkout master
  git merge develop
  ```

- **Merge de la branche `feature/nouvelle-fonctionnalité` dans `develop`**

  ```bash
  git checkout develop
  git merge feature/nouvelle-fonctionnalité
  ```

- **Merge de la branche `bugfix/correction-de-bug` dans `develop`**

  ```bash
  git checkout develop
  git merge bugfix/correction-de-bug
  ```

- **Merge de la branche `hotfix/correction-de-bug-urgente` dans `master`**

  ```bash
  git checkout master
  git merge hotfix/correction-de-bug-urgente
  ```

## 2. Gitmoji

**Gitmoji** est une convention de code pour les commits Git. Elle permet de décrire clairement les changements dans le code en utilisant des emoji.

### Liste des emoji :

- :tada: Nouveau fonctionnalité
- :bug: Correction de bug
- :sparkles: Amélioration de la documentation
- :recycle: Refactoring du code
- :art: Amélioration de la qualité du code
- :blue_heart: Amélioration de la performance
- :white_check_mark: Test unitaire
- :lock: Sécurité
- :arrow_up: Mise à jour de la version
- :arrow_down: Mise à niveau de la version
- :shirt: Dépendance
- :pencil: Documentation
- :zap: Amélioration de la performance
- :fire: Suppression de code
- :wrench: Configuration
- :green_heart: Ajout de code
- :white_circle: Correction de code

## 3. Plan Type README

**Plan Type README** est un fichier Markdown qui décrit le projet et son environnement de développement. Il est utilisé pour expliquer le projet à des personnes qui ne connaissent pas le code source.

### Exemple de plan type README :

```markdown
# Titre du projet

## Description

Description du projet

## Installation

Instructions pour installer le projet

## Utilisation

Instructions pour utiliser le projet

## Contribuer

Instructions pour contribuer au projet
```

## 4. Exos

### Exo 1

Fixer une issue sur le projet

### Exo 2

Créer une branche de développement

### Exo 3

Ajout d'une fonctionnalité dans la branche de développement