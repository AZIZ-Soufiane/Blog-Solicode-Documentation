# ➕ Spécifications : Création d’Article

**Fichier :** `form-article.html`  
*(ou organisation via `components/form/article/`)*  

**Rôle :**  
Formulaire permettant la **création d’un article** dans le dashboard admin du blog **SolicodeBlog**.

---

## 1. Structure du Formulaire (Mise en page complexe)

### A. Section Contenu (Gauche / Centre)

#### Titre
- Champ input large destiné à la saisie du titre de l’article.
- Implémenté sous forme de **composant réutilisable** avec **Tailwind CSS** et **Preline UI**.

#### Contenu
- Zone d’édition intégrant un **éditeur de texte riche (CKEditor)**.
- Fonctionnalités principales :
  - Mise en forme du texte (gras, italique, listes, liens, code).
  - **Upload et insertion d’images directement dans le contenu**.
  - Respect de l’ordre des images insérées.
- Simulation d’un éditeur WYSIWYG professionnel.

#### Galerie / Vidéos
- Zone d’upload de médias de type **Dropzone**.
- Permet le dépôt de fichiers vidéo (MP4, WebM).
- Zone cliquable et stylisée avec Tailwind et Preline.

---

### B. Barre Latérale  (Droite)

#### Publication
- Sélecteur de statut (ex. : Brouillon).
- Option **« À la une »** via un composant switch Preline.

#### Taxonomie
- Sélection d’une catégorie via un menu déroulant.
- Composant réutilisable basé sur Preline UI.

#### Tags
- Champ de saisie permettant l’ajout de plusieurs tags.
- Les tags sont séparés par des virgules.

#### Image de Couverture
- Zone de sélection de l’image principale de l’article.
- Possibilité de prévisualisation de l’image sélectionnée.

---

## 2. Action de Formulaire

- **Bouton unique :**
  - Libellé : **« Créer un article »**
  - Bouton principal stylisé avec **Tailwind CSS** (accent bleu) et **Preline UI**.
  - Déclenche la soumission du formulaire (simulation frontend uniquement).

---

## 3. Règles d’Interaction

### Validation Visuelle
- Simulation d’états d’erreur sur les champs requis (ex. : titre vide).
- Indications visuelles : bordures colorées et messages d’erreur.

---

## 4. Approche Technique

- Utilisation de **Tailwind CSS** pour la mise en page et le responsive design.
- Utilisation de **Preline UI** pour les composants (cards, inputs, boutons, switch).
- Architecture basée sur une **approche component-based** pour faciliter la réutilisation et la maintenance.
- Interface **frontend uniquement**, sans logique backend.
