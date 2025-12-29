# 🔐 Spécifications : Authentification

> **Fichiers :** `login.html` & `register.html`
> **Statut :** [PLANNED] Spécifications pour la création des pages.
> **Rôle :** Sécuriser l'accès aux fonctionnalités Membre et Admin.

## 1. Page de Connexion (`login.html`)

### A. Structure
*   **Layout :** Centré verticalement et horizontalement (`flex items-center justify-center`).
*   **Carte :** Container blanc avec ombre légère (`max-w-md`).
*   **En-tête :**
    *   Titre H1 "Connexion".
    *   Lien "Pas encore de compte ? S'inscrire ici" (vers `register.html`).

### B. Formulaire
*   **Social Login :** Bouton "Continuer avec Google" (Haut du formulaire).
*   **Champs :**
    1.  **Email :** `type="email"`, Required.
    2.  **Mot de passe :** `type="password"`, Required.
        *   Lien "Mot de passe oublié ?" aligné à droite du label.
*   **Options :**
    *   Checkbox "Se souvenir de moi" (Non présent sur la maquette actuelle, mais standard).
*   **Action :**
    *   Bouton primaire "Se connecter" (Largeur 100%, avec ombre).

### C. Pied de page
*   Lien retour "← Retour à l'accueil" (vers `index.html`) ou logo cliquable.

---

## 2. Page d'Inscription (`register.html`)

### A. Structure
*   **Layout :** Identique à Login.
*   **En-tête :**
    *   Titre H1 "Créer un compte".
    *   Lien "Déjà inscrit ? Se connecter" (vers `login.html`).

### B. Formulaire
*   **Social Login :** Bouton "S'inscrire avec Google".
*   **Champs :**
    1.  **Nom complet :** `type="text"`, Required.
    2.  **Adresse email :** `type="email"`, Required.
    3.  **Mot de passe :** `type="password"`, Min 8 chars.
    4.  **Confirmer le mot de passe :** `type="password"`.
*   **Action :**
    *   Bouton primaire "Créer mon compte" (Largeur 100%).

## 3. Règles Communes
*   **Feedback Visuel :**
    *   Focus sur les champs (Bordure bleue).
    *   Hover sur les boutons (Bleu plus foncé).
*   **Responsive :** La carte prend toute la largeur sur mobile avec un padding.
