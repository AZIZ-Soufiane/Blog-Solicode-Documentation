# 📖 Spécifications : Détail Article

> **Fichier :** `article.html`
> **Rôle :** Page de lecture immersive. Doit être lisible et inciter à l'interaction.

## 1. Structure de la Page

### A. Corps de l'Article & Commentaires -> `components/contenu-cards/article-detail.html`
*   **Breadcrumb/Badge :** Catégorie (ex: "Dev Web") en haut à gauche.
*   **Titre :** H1 Large (3xl-5xl).
*   **Author Block :** Avatar, Nom, Date, Temps de lecture.
*   **Cover Image :** Large avec coins arrondis.
*   **Prose Content :** Typographie optimisée.
*   **Comment Section :** Formulaire de dépôt + Liste des commentaires (avec réponses).

### B. Cards "À la une" -> `components/contenu-cards/card-article.html`
*   (Optionnel) Utilisées pour une section "Vous aimerez aussi" en bas de page.

## 2. Règles d'Interaction
*   **Images :** Doivent être responsive et garder le ratio.
*   **Formulaire Commentaire :** Bouton désactivé si champ vide (optionnel).
*   **Liens Tags :** Clic sur un Tag -> Redirige vers `search.html?tag=XYZ`.
