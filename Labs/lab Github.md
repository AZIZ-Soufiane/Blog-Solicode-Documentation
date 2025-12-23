
# 🧪 LAB : Branch Roles, Branch Rules & Pull Requests in GitHub

## Realise Par : Abdelhay Mallouli

## 🎯 Objectif du Lab

Comprendre :

* Les **rôles des branches**
* Le fonctionnement des **Pull Requests**
* Les **Branch Rules (règles de protection)** dans GitHub
  afin de travailler en équipe de manière **professionnelle et sécurisée**.

---

## 🧠 Concepts Clés

* Une **branch** permet de développer une fonctionnalité sans affecter le code stable.
* Une **Pull Request (PR)** permet de proposer des changements pour révision avant fusion.
* Les **Branch Rules** empêchent les erreurs (push direct, fusion sans review, etc.).
* La branche `main` doit toujours contenir un **code stable**.

---

## 🔀 Rôles des Branches

| Branch      | Rôle                                  |
| ----------- | ------------------------------------- |
| `main`      | 🔒 Version finale / production        |
| `develop`   | 🧪 Intégration des fonctionnalités    |
| `feature/*` | 🛠 Développement d’une fonctionnalité |
| `bugfix/*`  | 🐛 Correction de bugs                 |

---

## 🧩 Scénario du Lab

Vous travaillez sur un projet en équipe.

### Règles du projet :

* ❌ Interdiction de pousser directement sur `main`
* ❌ Interdiction de fusionner sans Pull Request
* ✅ Chaque modification passe par une PR
* 👀 Les PR doivent être **revues et approuvées**

---

## 🧪 Partie 1 : Création d’une Feature Branch

Créer une branche pour une fonctionnalité :

```bash
git checkout -b feature/add-homepage
```

Modifier un fichier (ex: `README.md`).

```bash
git add .
git commit -m "Add homepage feature"
git push -u origin feature/add-homepage
```

---

## 🧪 Partie 2 : Créer une Pull Request

1. Aller sur **GitHub**
2. Cliquer sur **Compare & pull request**
3. Choisir :

   * **Base branch** : `develop`
   * **Compare branch** : `feature/add-homepage`
4. Cliquer sur **Create Pull Request**

---

## 🧪 Partie 3 : Rôles dans une Pull Request

| Rôle       | Description        |
| ---------- | ------------------ |
| Auteur     | Crée la PR         |
| Reviewer   | Vérifie le code    |
| Maintainer | Valide et fusionne |

### Actions obligatoires :

* Ajouter au moins **1 reviewer**
* Le reviewer clique sur **Approve**

---

## 🔐 Partie 4 : Branch Rules (Règles de Protection)

### 🎯 Pourquoi utiliser les Branch Rules ?

* Empêcher les erreurs humaines
* Forcer les bonnes pratiques
* Sécuriser la branche `main`

---

## ⚙️ Étapes pour ajouter une Branch Rule

1. Aller dans **Settings**
2. Cliquer sur **Branches**
3. Cliquer sur **Add branch protection rule**
4. Branch name pattern :

   ```text
   main
   ```

---

## 🛡️ Toutes les Branch Rules expliquées

### 1️⃣ Require a pull request before merging

✔ **Obligatoire**

👉 Empêche toute fusion directe sans PR.

---

### 2️⃣ Require approvals

✔ Activer
✔ Nombre : **1 ou 2**

👉 La PR doit être approuvée par un reviewer.

---

### 3️⃣ Dismiss stale pull request approvals

✔ Recommandé

👉 Si le code change après une approbation, la review est annulée.

---

### 4️⃣ Require review from Code Owners

✔ Optionnel

👉 Force la review par des personnes spécifiques.

---

### 5️⃣ Restrict who can push to matching branches

✔ Activer

👉 Seuls les **maintainers** peuvent pousser sur `main`.

---

### 6️⃣ Require status checks to pass before merging

✔ Optionnel (CI/CD)

👉 La PR doit passer les tests avant fusion.

---

### 7️⃣ Require linear history

✔ Optionnel

👉 Empêche les merge commits désorganisés.

---

### 8️⃣ Include administrators

✔ Recommandé

👉 Même les admins doivent respecter les règles.

---

### 🎯 Résultat

➡ Personne ne peut :

* Push directement sur `main`
* Fusionner sans review
* Ignorer les règles

---

## 🧪 Partie 5 : Pull Request vers `main`

Créer une PR :

* **From** : `develop`
* **To** : `main`

### Conditions obligatoires :

* Review requise
* Approval requise
* Fusion uniquement par le maintainer

---

## 🔁 Workflow Final du Projet

```text
feature/* → develop → main
```

---



