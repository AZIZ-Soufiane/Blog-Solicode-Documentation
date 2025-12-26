# 🔍 Spécifications : Recherche & Liste

> **Fichier :** `search.html`
> **Rôle :** Permettre de trouver du contenu via mots-clés ou filtres thématiques.

## 1. Structure de la Page

### A. Recherche & Filtres -> `components/recherche-filtres/`
*   **Barre de Recherche (`search-bar.html`) :** Input premium avec icône loupe intégré à un dropdown de catégories.
*   **Filtre Catégories (`filters.html`) :** Dropdown de sélection rapide avec icônes Lucide.

### B. Grille de Résultats
*   **Layout :** Grid 3 cols.
*   **Cards :** Composant `card-article.html` standard.

### C. Pagination -> `components/recherche-filtres/pagination.html`
*   **Style :** Boutons Précédent/Suivant + Numéros de page.

## 2. Règles d'Interaction
*   **Filtres :** Au clic sur un badge, la grille se met à jour (simulation ou rechargement).
*   **Input :** La recherche se lance à `Enter` ou au clic sur l'icône loupe (si bouton présent).
*   **Pagination :** Navigation numérotée avec états actif/inactif.
