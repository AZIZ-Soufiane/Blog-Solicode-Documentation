# 📊 Spécifications : Dashboard Admin

> **Fichier :** `dashboard-admin.html`
> **Rôle :** Vue d'ensemble de l'activité du blog pour l'administrateur.

## 1. Structure de la Page

### A. Navigation Latérale -> `components/Side-bar/`
*   **Menu :** Liens vers Dashboard, Articles, Catégories, Tags, Utilisateurs.
*   **Style :** Sidebar foncée ou claire avec icônes Lucide à gauche du texte.

### B. Barre de Navigation Supérieure -> `components/Navbar/`
*   **Recherche :** Barre de recherche globale.
*   **Profil :** Avatar utilisateur et menu déroulant (Notifications, Logout).

### C. Statistiques Clés -> `components/KPI Cards/`
*   **KPIs (4) :**
    *   Total Articles
    *   Total Vues
    *   Total Commentaires
    *   Utilisateurs Actifs
*   **Style :** Cartes blanches avec bordures subtiles, icônes circulaires.

### D. Articles Récents -> `components/Recent Articles/`
*   **Liste :** Les 5 derniers articles.
*   **Champs :** Titre, Auteur, Statut (Badge), Date.

### E. Activités -> `components/Activity List/`
*   **Flux :** Chronologie des dernières actions sur le CMS.

## 2. Règles d'Interaction
*   **Responsive :** La sidebar se replie sur les petits écrans.
*   **Hover :** Effets de survol sur les items de menu et les cartes KPIs.
