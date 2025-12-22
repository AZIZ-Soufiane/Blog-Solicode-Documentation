---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
style: |
  section {
    font-size: 24px;
  }
  h1, h2 {
    color: #333;
  }
---

![bg left:40% 80%](https://via.placeholder.com/300x200?text=Logo+Solicode)
# **Projet Blog Solicode**
## Sprint 1
Présentation réalisée avec Marp  
Date : 22 décembre 2025  
Équipe : [Votre Nom/Équipe]

---

# Besoins
Les besoins du projet "Blog Solicode" visent à créer une plateforme simple et accessible pour partager des connaissances en programmation au sein de la communauté Solicode.

- **Besoins fonctionnels** : Permettre aux utilisateurs de publier des articles, commenter et rechercher du contenu.
- **Besoins non fonctionnels** : Site responsive, sécurisé (authentification basique), performant (chargement rapide).
- **Contrainte** : Focus sur Sprint 1 pour les fonctionnalités de base, sans intégrations avancées comme les réseaux sociaux.

Exemples de besoins prioritaires :
1. Un utilisateur doit pouvoir s'inscrire et se connecter.
2. Publication d'articles avec titres, corps et tags.
3. Affichage d'une liste d'articles récents.

---

# Fonctionnalités (Use Cases du Sprint 1)
Le Sprint 1 implémente les use cases essentiels pour un MVP (Minimum Viable Product).



---

# Labs (Ateliers Pratiques Réalisés)
Pour finaliser le projet, nous avons suivi plusieurs labs (ateliers ou sessions pratiques) couvrant les technologies clés. Ces labs ont été essentiels pour surmonter les défis techniques et itérer sur le code.

- **Lab 1 : Initiation HTML/CSS/JS** (Durée : 4h)  
  Construction de la structure de base du site, avec focus sur le responsive design via Bootstrap.

- **Lab 2 : Backend avec Node.js/Express** (Durée : 6h)  
  Mise en place du serveur, routes API pour les articles.

- **Lab 3 : Base de Données MongoDB** (Durée : 5h)  
  Modélisation et requêtes basiques, résolution d'erreurs de connexion.

- **Lab 4 : Tests et Débogage** (Durée : 3h)  
  Utilisation de Jest pour tester les use cases, correction de bugs (ex. : validation des formulaires).

Défis rencontrés : Intégration frontend-backend, résolus via des itérations en groupe. Ces labs ont permis d'achever le Sprint 1 en respectant les délais.

Tableau des Labs :

| Lab | Technologies | Objectifs Atteints | Défis |
|-----|--------------|--------------------|-------|
| 1 | HTML/CSS/JS | Interface basique | Compatibilité navigateurs |
| 2 | Node.js | API REST | Gestion des erreurs |
| 3 | MongoDB | Stockage données | Schéma optimisé |
| 4 | Jest | Tests unitaires | Couverture 80% |

---

# Maquette (Mockup Utilisé)
La maquette définit l'interface utilisateur pour une expérience intuitive. Nous avons utilisé Figma pour le design initial.

**Description Générale** :  
- Page d'accueil : Liste d'articles en cards, barre de recherche.  
- Page Article : Contenu détaillé, section commentaires.  
- Dashboard : Boutons pour nouveau post, édition.

Représentation Visuelle :


---

# Diagramme de Classe 
Le diagramme de classe modélise la base de données. Il définit les entités principales et leurs relations.

**Entités Clés** :  
- User : id, email, password, role.  
- Article : id, title, content, author (ref User), tags[], date.  
- Comment : id, content, author (ref User), article (ref Article), date.


---

# Réalisation
La réalisation du Sprint 1 a implémenté les fonctionnalités avec:

* 
* 
* 


Résultats : Application fonctionnelle avec 3 use cases implémentés, tests passés à 85%. Améliorations futures : Authentification JWT pour Sprint 2.


---

# Conclusion
Ce Sprint 1 pose les fondations solides pour "Blog Solicode". Prochains sprints : Intégrations avancées et optimisations. Questions ?
