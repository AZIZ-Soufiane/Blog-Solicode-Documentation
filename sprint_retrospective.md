# Rétrospective de Sprint - Modifications Requises

Sur la base des retours recueillis lors de la phase Empathie ainsi que des validations Utilisateur/Formateur, voici la liste consolidée des changements à implémenter.

## 1. Interface Publique (UI/UX)

### Navigation & Mise en Page

* [x] **Barre de Navigation** : Ajouter une barre de recherche directement dans la navbar pour un accès rapide. (Youssef, Souklabi)
* [x] **Barre de Navigation** : Mettre en place un menu déroulant des catégories. (Ayoub)
* [ ] **Sidebar** : Ajouter une barre latérale dédiée avec filtres par catégorie (Cases à cocher) et recherche avancée. (Youssef, Apprenants)
* [ ] **Fil d’Ariane (Breadcrumbs)** : Ajouter des breadcrumbs pour améliorer la navigation et la compréhension du parcours utilisateur. (Yassir, Apprenants)
* [x] **Bouton Retour en Haut** : Ajouter un bouton pour remonter rapidement en haut de la page. (Ayoub)
* [x] **Logo** : Augmenter la taille du logo. (Ayoub)

### Page d’Accueil

* [x] **Section Hero** : Corriger le titre dans la section Hero. (Essarraj)
* [x] **Section Hero** : Remplacer l’image actuelle par une image liée à Solicode/vie de campus. (Yassir)

### Détail d’Article

* [ ] **Temps de Lecture** : Afficher une estimation du temps de lecture pour chaque article. (Yassir, Souklabi)
* [x] **Tags** : Rendre les tags cliquables. (Yassir, Safa)
* [x] **Tags & Catégorie** : Afficher les tags et la catégorie en bas du contenu de l’article. (Yassir)
* [ ] **Commentaires** : S’assurer que les commentaires sont chargés depuis la base de données. (Essarraj)

## 2. Authentification & Profil Utilisateur

* [ ] **Connexion** : Limiter l’authentification uniquement à la connexion via **Google**. (Youssef)
* [ ] **Profil** : Ajouter une page de gestion du profil utilisateur. (Ismail, Safa)
* [ ] **Notifications** : Ajouter une page de paramètres pour la gestion des notifications. (Ismail, Safa)

## 3. Administration & Tableau de Bord

### Administration Générale

* [x] **Recherche** : Ajouter une fonctionnalité de recherche dans le tableau de bord Admin. (Apprenants)
* [ ] **Rôles** : Permettre à l’Administrateur Principal d’attribuer le rôle "Admin" à d’autres utilisateurs (notamment les formateurs). (Hamouda)
* [ ] **Rôles** : L’Admin doit disposer de toutes les capacités d’un modérateur. (Fatine)

### Gestion des Articles

* [ ] **Formulaire** : Remplacer le champ "Statut" (actuellement Radio button) par une **Liste déroulante (Select)**. (Fatine)
* [ ] **Tableau** : Supprimer la colonne "Contenu" de la liste des articles pour éviter la surcharge visuelle. (Fatine)
* [ ] **Aperçu** : Ajouter un bouton "Voir l’article" pour permettre un aperçu avant/pendant l’édition. (Fatine)
* [ ] **Statistiques** : Ajouter des statistiques (Vues, Likes, Partages) par article et globales (Mois/Semaine/Année). (Apprenants)
* [ ] **Médias** : Permettre l’upload d’images et de vidéos. (Hamouda)

## 4. Fonctionnalités & Logique

* [ ] **Bot de Support** : Intégrer un bot d’assistance (mentionné pour la page "À propos" ou usage général). (Apprenants)
* [ ] **Communauté** : (Long terme) Créer un espace d’échange/Q&A similaire à Reddit/Stack Overflow. (Safa, Apprenants)
* [ ] **Gamification** : (Optionnel) Considérer des récompenses type "Meilleur Article" ou "Meilleur Auteur". (Persona Formateur)

## 5. Données de Contenu

* [ ] **Données de Test** : S’assurer que toutes les données d’articles soient réelles et authentiques (pas de "Lorem Ipsum"). (Fatine)
* [ ] **Catégories** : Simplifier les catégories en : Backend, Frontend, Frameworks, Outils/Technologies. (Souklabi)

## Résumé des Contributeurs

* **Apprenants** : Ayoub Faqihi, Ismail Founti, Safa El Gharras, Yassir El Mesbahi, Jalil Betroji.
* **Formateurs** : Abdelatif Souklabi, Youssef, Hamouda, Fatine, Essarraj Fouad.

