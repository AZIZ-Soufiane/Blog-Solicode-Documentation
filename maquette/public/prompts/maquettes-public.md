# Liste et Spécifications des Maquettes Publiques

### 🏠 Accueil (`./index.html`)
Vitrine principale du site.
*   **Objectif :** Accueillir le visiteur et présenter les contenus phares.
*   **Composants clés :**
    *   **Hero Section :** Titre accrocheur + CTA.
    *   **Featured Articles :** Grille des 3 articles "À la une".
    *   **Latest News :** Liste des derniers articles publiés.

### 🔍 Recherche & Liste (`./search.html`)
Page de navigation transverse.
*   **Objectif :** Permettre de trouver des articles par mots-clés ou filtres.
*   **Composants clés :**
    *   **Search Bar :** Champ de recherche large avec bouton.
    *   **Sidebar Filtres :** Checkbox Catégories, Nuage de Tags.
    *   **Grid Results :** Cartes articles paginées.

### 📖 Détail Article (`./article.html`)
Cœur de l'expérience lecteur.
*   **Objectif :** Lecture immersive d'un contenu.
*   **Composants clés :**
    *   **Article Header :** Titre, Auteur, Date, Catégorie, Temps de lecture.
    *   **Content Body :** Typographie optimisée pour la lecture (Prose).
    *   **Comment Section :** Liste des avis et formulaire de dépôt.
    *   **Related Posts :** "Vous aimerez aussi".

### 🔐 Authentification
Pages d'accès membre (Design prévu, intégration en cours).
*   **Login (`./login.html`) :** [TODO] Formulaire de connexion.
*   **Register (`./register.html`) :** [TODO] Formulaire d'inscription.

# 📂 Architecture des Dossiers

Ce document valide la structure des fichiers pour la partie Publique.

## Arborescence

```bash
maquettes-public/
│
├── index.html              # 🏠 Page d'Accueil
├── search.html             # 🔍 Page Recherche / Liste
├── article.html            # 📖 Page Détail Article
├── login.html              # 🔐 [TODO] Connexion
├── register.html           # 📝 [TODO] Inscription
│
├── components/             # 🧱 Briques Réutilisables
│   ├── contenu-cards/      # Contenus et Blocs
│   │   ├── article-detail.html
│   │   ├── card-article.html
│   │   ├── hero.html
│   │   └── statistics.html
│   ├── navigation/         # Navigation site
│   │   ├── footer.html
│   │   └── navbar.html
│   └── recherche-filtres/   # Recherche et Filtres UI
│       ├── filters.html
│       ├── pagination.html
│       └── search-bar.html
│
├── images/                 # Ressources d'images
│   ├── solicode-logo.png
│   ├── banner.jpg
│   └── banner2.jpg
```

## Conventions
*   **Racine :** Les pages principales sont à la racine pour simuler un routage simple.
*   **Composants :** Isolés dans `components/` pour être inclus (mentalement ou via script) dans les pages.
*   **Noms :** `kebab-case` strict.
