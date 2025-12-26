# 🤖 Prompt : Générateur de Pages Admin (Assemblage)

Ce prompt est destiné à assembler les pages d'administration finales de la maquette à partir des fragments HTML unitaires.

## Contexte
Nous utilisons une architecture statique. Le but est de fusionner le squelette global (contenant la sidebar et le header) avec les composants de contenu.

## Instructions d'Assemblage

1. **Sélectionner le Squelette** : Commencer par le fichier de base (ex: `dashboard-admin.html` servant de référence).
2. **Identifier les Zones** : Repérer les emplacements pour la Sidebar, la Navbar (Header) et le Main Content.
3. **Fusionner les Composants** :
   - Remplacer la Sidebar par le contenu de `components/Side-bar/`.
   - Remplacer le Header par le contenu de `components/Navbar/`.
   - Injecter les sections spécifiques (KPIs, Tables, Formulaires) dans la zone `<main>`.
4. **Vérifier les Chemins** : S'assurer que les liens vers les images et les icônes Lucide sont fonctionnels.
5. **Adapter le "Title"** : Mettre à jour la balise `<title>` de la page HTML.

## Exemple de Flux (Dashboard)
- **Injection 1** : `Side-bar/sidebar.html` -> `<nav class="sidebar">`
- **Injection 2** : `Navbar/navbar.html` -> `<header>`
- **Injection 3** : `KPI Cards/stats.html` -> `<div class="grid-stats">`
- **Injection 4** : `Recent Articles/list.html` -> `<section class="recent-articles">`

## Règle d'Or
Le code final doit être **100% statique**. Pas d'appels serveurs, pas de logique Blade, uniquement du HTML pur avec les classes Tailwind.
