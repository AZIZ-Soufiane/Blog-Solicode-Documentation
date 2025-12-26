# 🤖 Prompt : Générateur de Pages (Assemblage)

Ce prompt est destiné à un agent IA ou un développeur pour assembler les pages finales à partir des briques modulaires.

## Contexte
Nous utilisons une architecture à base de composants statiques. Le but est de fusionner les squelettes de layouts avec les fichiers HTML unitaires.

## Instructions d'Assemblage

1. **Sélectionner le Layout** : Commencer par le fichier approprié dans `components/layout/` (ex: `layout-base.html`).
2. **Identifier les Zones** : Repérer les placeholders visuels comme `[Composant NavBar ici]` ou les commentaires comme `<!-- [INCLUDE: ...] -->`.
3. **Fusionner les Composants** :
   - Remplacer le placeholder Navbar par le contenu de `components/navigation/navbar.html`.
   - Remplacer le placeholder Footer par le contenu de `components/navigation/footer.html`.
   - Injecter les sections spécifiques définies dans les fichiers de `specs/` (ex: Hero, Grid, Features).
4. **Adapter le "Title"** : Mettre à jour la balise `<title>` selon la page.
5. **Vérifier les Chemins** : S'assurer que les liens vers les images (`../../images/...`) et les pages (`index.html`, `search.html`) sont corrects une fois à la racine.

## Exemple de Flux (Accueil)
- **Source** : `layout-base.html`
- **Injection 1** : `navbar.html` -> `<header>`
- **Injection 2** : `hero.html` -> `<main>`
- **Injection 3** : `statistics.html` -> `<main>`
- **Injection 4** : `card-article.html` (x3) -> `<div class="grid">`
- **Injection 5** : `footer.html` -> `<footer>`

## Règle d'Or
Le code final doit être **100% statique**, sans dépendances JS complexes autres que celles déjà incluses dans les layouts (Tailwind, Lucide, Preline).
