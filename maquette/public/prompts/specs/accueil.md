# 🏠 Spécifications : Page d'Accueil

> **Fichier :** `index.html`
> **Rôle :** Point d'entrée principal. Doit séduire et orienter immédiatement.

## 1. Structure de la Page

### A. Navbar (Sticky) -> `components/navigation/navbar.html`
*   **Logo :** Image `solicode-logo.png` (Cliquable -> `index.html`).
*   **Menu Bureau :** Accueil, Laravel, PHP, Mobile.
*   **Menu Mobile :** Burger menu (Collapse).
*   **Actions :**
    *   `Connexion` (Lien vers `login.html`).
    *   `S'inscrire` (Bouton CTA, vers `register.html`).

### B. Hero Section -> `components/contenu-cards/hero.html`
*   **Titre :** H1 impactant avec span coloré ("Solicode").
*   **Sous-titre :** Description de la plateforme de ressources.
*   **Composants :**
    *   **Badge :** Label "Formation & Développement".
    *   **CTA Principal :** "Explorer" (Lien `search.html`).
    *   **CTA Secondaire :** "En savoir plus" (Lien ancre `#about`).
    *   **Illustration :** Image `banner2.jpg` à droite (Desktop).

### C. Section "Articles Récents"
*   **En-tête :** Titre H2 "Articles Récents".
*   **Grille :** 3 colonnes (Desktop) / 1 colonne (Mobile).
*   **Bouton :** "Voir tous les articles" (Lien `search.html`).
*   **Cartes Article (Composant) :** -> `components/contenu-cards/card-article.html`
    *   **Image :** Cover (Height ~160px).
    *   **Badge (Sur l'image) :** Catégorie principale (ex: Laravel).
    *   **Tags :** Liste de hashtags grisés (ex: #API).
    *   **Titre :** H3.
    *   **Extrait :** ~3 lignes (line-clamp).
    *   **Méta Footer :** Avatar Auteur, Nom, Date, Nombre de commentaires (Icon bulle).

### D. Statistiques -> `components/contenu-cards/statistics.html`
*   **Chiffres clés :** Articles, Étudiants, Formateurs (Animation au scroll).

### E. Footer -> `components/navigation/footer.html`
*   **Colonnes :**
    1.  **Brand :** Logo + Pitch court.
    2.  **Ressources :** Liens vers Articles, Tutos...
    3.  **Légal :** Mentions légales, Politique confidentialité.
*   **Bottom :** Copyright + Réseaux Sociaux (FB, Twitter, Github).

## 2. Règles d'Interaction
*   **Hover Cartes :** Légère élévation (`shadow-md`) + Scale image.
*   **Responsive :** Navbar devient burger < `sm`. Grille passe de 1 à 3 col.
