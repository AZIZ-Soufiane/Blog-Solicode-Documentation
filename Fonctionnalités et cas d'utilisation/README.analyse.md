---
etape: "03"
module: "Analyse & Conception"
role: "Documentation des Diagrammes de Cas d'Utilisation"
---




<!-- TODO : Diviser en deuxd fichier README.md et prompt.md -->


# 🕵️ Analyse Fonctionnelle — Cas d'Utilisation

Ce dossier contient la modélisation des interactions entre les utilisateurs et le système. Pour une meilleure compréhension par l'IA et les développeurs, nous distinguons **deux niveaux de granularité**.



---

## 1. Définitions & Relations (UML)

### Les Acteurs
*   **Visiteur :** Utilisateur non authentifié (Lecture seule).
*   **Auteur / Membre :** Utilisateur authentifié.
*   **Administrateur :** Gestionnaire du Back-Office.

> **Note sur l'Héritage :** Nous utilisons `Guest <|-- Author`. Cela signifie que l'Auteur **EST UN** Visiteur : il hérite de toutes ses capacités de consultation sans qu'on ait besoin de redessiner les traits.

### Les Relations
| Type | Symbole | Signification | Contexte d'usage (Niveau 2) |
| :--- | :---: | :--- | :--- |
| **Association** | `—` | Interaction directe | L'acteur lance le cas d'utilisation. |
| **Héritage** | `<|--` | "Est un" | Un acteur possède les droits de son parent. |
| **Include** | `..> <<include>>` | "Nécessite" | **Obligatoire.** A ne peut pas se faire sans B (ex: Login pour Commenter). |
| **Extend** | `.> <<extend>>` | "Peut être suivi de" | **Optionnel.** B est une suite possible de A (ex: Filtrer après avoir Listé). |

---

## 2. Règles d'Or & Conventions Solicode

Ces règles doivent être appliquées à **tous** les nouveaux diagrammes créés.

### 4.1 Acteurs & Relations
*   **Pas de flèches orientées :** L'association Acteur-Usecase se fait avec un trait simple (`--`). Jamais de `-->`.
*   **Héritage systématique :** Ne jamais dupliquer les liens communs. Utiliser `<|--` pour signifier qu'un Acteur hérite des droits d'un autre (ex: `Visiteur <|-- Auteur`).

### 4.2 Logique d'Inclusion & Extension (Vue Détaillée)
*   **Extend (Optionnel) :** Tout ce qui n'est pas le flux principal ou obligatoire est une extension.
    *   *Ex :* Lire les commentaires `.> extend` Lire article.
    *   *Ex :* Filtrer `.> extend` Rechercher.
*   **Include (Obligatoire) :** Tout pré-requis technique ou fonctionnel incontournable.
    *   *Ex :* Poster commentaire `..> include` Se connecter.
