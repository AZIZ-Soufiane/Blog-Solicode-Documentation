# 📝 Spécifications : Liste des Articles

> **Fichier :** `admin-articles.html` (ou via `components/articles/`)
> **Rôle :** Interface de gestion et de visualisation des articles existants.

## 1. Structure de la Page

### A. En-tête de Table
*   **Recherche :** Champ de saisie pour filtrer les articles par titre.
*   **Filtres :** Dropdowns pour Catégories et Statuts.
*   **Action :** Bouton "Ajouter un article" (Lien vers le formulaire).

### B. Tableau des Articles -> `components/articles/`
*   **Colonnes :**
    *   Image de couverture (miniature).
    *   Titre (Lien vers l'édition).
    *   Auteur (Nom + Avatar).
    *   Catégories (Badges labelisés).
    *   Statut (Badge couleur : Vert pour Publié, Gris pour Brouillon).
    *   Actions : Icônes Lucide (Éditer, Supprimer, Voir).

## 2. Règles d'Interaction
*   **Pagination :** Navigation entre les pages de résultats en bas de table.
*   **Tri :** Possibilité de cliquer sur les en-têtes de colonnes (Théorique en maquette).
*   **Style :** Table aérée, fond blanc, lignes zébrées ou séparées par des lignes grises fines.
