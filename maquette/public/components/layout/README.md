# 🏗️ Layouts de l'Interface

Ce dossier contient les structures globales des pages de la maquette.

## 1. Description des Layouts

| Fichier | Cible | Structure |
| :--- | :--- | :--- |
| `layout-base.html` | Accueil, Recherche, Article | Navbar Sticky + Main Content + Footer |
| `layout-simple.html` | Login, Register, Error | Centré Flex + Background uni |

## 2. Utilisation
Ces fichiers servent de modèles (squelettes) pour la création des pages HTML finales. Ils permettent de visualiser comment les composants (Navbar, Footer, etc.) s'imbriquent dans le layout global.

### Points Clés
- **Navbar** : Toujours présente et `sticky` sur le layout de base.
- **Main** : Utilise `flex-grow` pour pousser le footer en bas si le contenu est court.
- **Tailwind** : Configuration centralisée incluant les polices `Inter` et `Outfit`.
