#  Référentiel Technique & Stack

Ce document définit **l'environnement technique strict** du projet fil rouge MVP.

## 1. Vue générale

Le projet est une **application complète** comprenant :

- **Web Public** : Consultation des contenus (Laravel Blade).
- **Web Admin** : Gestion des données (Laravel Blade + Authentification).
- **API JSON** : Interface pour le mobile (RESTful).
- **App Mobile** : Client Android natif (Kotlin / Compose).
- **Base de Données** : Stockage relationnel partagé (MySQL).

---

## 2. Stack Technique Détaillée

### Back-end & Architecture

- **Framework :** Laravel 12.
- **Architecture :** N-Tiers (Controller -> Service -> Model).
- **Sécurité :**
  - Authentification : Laravel UI avec Tailwind CSS.
  - Autorisation : **Spatie Laravel Permission**.
- **API :** Resources JSON, Sanctum (Tokens).
- **Internationalisation :** Laravel Lang.

### Front-end (Web)

- **Moteur de template :** Blade (Components, Layouts).
- **CSS :** Tailwind CSS.
- **UI Kit :** Preline UI.
- **Interactivité :** Alpine.js / AJAX (Fetch).
- **Admin Dashboard :** One Page CRUD (Recherche/Filtres dynamiques).
- **Icons :** Lucide Library

### Mobile (Android)

- **Langage :** Kotlin.
- **UI :** Jetpack Compose.
- **Réseau :** Retrofit (Consommation API REST).
- **Architecture :** MVVM.

### Base de Données

- **SGBD :** MySQL 8.0+.
- **ORM :** Eloquent (Relations, Scopes, Accessors).

### Infrastructure & Outils

- **Versionning :** Git (GitHub Flow) : Develop, main, une branche pour chaque Sprint, et Version.
- **Serveur :** Linux (Ubuntu, Nginx/Apache).
- **Test API :** Postman.
