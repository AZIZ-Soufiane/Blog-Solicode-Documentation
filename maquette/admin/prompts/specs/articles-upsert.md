# ➕ Spécifications : Création / Édition d'Article

> **Fichier :** `form-article.html` (ou via `components/form Article/`)
> **Rôle :** Formulaire complet pour la saisie de nouveaux articles ou la modification d'existants.

## 1. Structure du Formulaire (Mise en page complexe)

### A. Section Contenu (Gauche/Centre)
*   **Titre :** Input large.
*   **Contenu :** Zone simulant un éditeur de texte riche (WYSIWYG).
*   **Galerie/Vidéos :** Zone d'upload (Dropzone) pour les médias.

### B. Barre Latérale de Paramètres (Droite)
*   **Publication :** Sélecteur de statut, date de publication, option "À la une".
*   **Taxonomie :** Liste de cases à cocher ou menu multi-sélection pour les Catégories.
*   **Tags :** Zone de saisie dynamique.
*   **Image de Couverture :** Zone de sélection et prévisualisation de l'image principale.

## 2. Actions de Formulaire
*   **Bouton Principal :** "Publier" ou "Enregistrer les modifications".
*   **Bouton Secondaire :** "Enregistrer comme brouillon" ou "Annuler".

## 3. Règles d'Interaction
*   **Validation Visuelle :** Simulation d'états d'erreur sur les champs requis vides.
*   **Navigation :** Lien de retour vers la liste des articles.
