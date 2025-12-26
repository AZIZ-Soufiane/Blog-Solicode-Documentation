# 🏗️ Architecture des Maquettes

Ce document définit la structure globale et l'organisation des fichiers pour l'interface publique SoliCode.

## 📂 Organisation des Dossiers

```bash
maquette/public/
│
├── index.html              # 🏠 Accueil (Assemblé)
├── search.html             # 🔍 Recherche (Assemblé)
├── article.html            # 📖 Détail Article (Assemblé)
│
├── components/             # 🧱 Briques Réutilisables
│   ├── layout/             # 🏗️ Squelettes de pages
│   ├── navigation/         # 🧭 Header/Footer
│   ├── contenu-cards/      # 🖼️ Cartes et Hero
│   └── recherche-filtres/   # 🧪 Filtres UI
│
└── prompts/                # 🤖 Documentation & Prompts
    ├── 00-architecture.md  # (Ce fichier)
    ├── 01-generator-prompt.md # Instructions d'assemblage
    └── specs/              # Détailles par page
```

## 🛠️ Principes de Développement

1. **Modularité** : Chaque élément visuel est un composant HTML indépendant dans `components/`.
2. **Layout First** : On utilise les squelettes de `components/layout/` pour garantir la cohérence des polices et des couleurs.
3. **Zéro Redondance** : Les composants ne doivent pas inclure les balises `<head>` ou `<body>`, seulement le fragment HTML nécessaire.
4. **Conventions** :
   - `kebab-case` pour les fichiers.
   - Tailwind CSS pour tout le style.
   - Lucide Icons pour l'iconographie.

## 📖 Sommaire des Spécifications
- [🏠 Accueil](specs/accueil.md)
- [🔍 Recherche](specs/recherche.md)
- [📖 Détail Article](specs/article.md)
- [🔐 Authentification](specs/auth.md)
