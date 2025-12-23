# 📘 LAB – Upload des fichiers & médias (Images & Vidéos) avec Laravel

---

## 1. Objectif du LAB

Ce LAB a pour objectif de comprendre et pratiquer :
- Le principe de l’upload des fichiers dans Laravel

- L’upload d’une image et d’une vidéo

- L’affichage des fichiers uploadés


---

## 2. Partie théorique

### 2.1 Définition de l’upload de fichiers

L’upload de fichiers consiste à envoyer un fichier depuis le navigateur vers le serveur afin de le stocker et l’utiliser dans une application web.

Les fichiers les plus utilisés sont :
- Images (jpg, png)
- Vidéos (mp4)
- Documents (pdf)

---

### 2.2 Fonctionnement général dans Laravel

Laravel gère l’upload en suivant ces étapes :

1. L’utilisateur choisit un fichier  
2. Le formulaire envoie la requête  
3. Le controller reçoit les données  
4. Laravel valide le fichier  
5. Laravel stocke le fichier dans `storage`  
6. Le chemin du fichier est sauvegardé  

⚠️ Important :  
Le fichier n’est jamais stocké dans la base de données, seul son chemin est enregistré.

---

### 2.3 Différence entre image et vidéo

| Image | Vidéo |
|------|------|
| Fichier léger | Fichier lourd |
| jpg, png | mp4 |
| Taille limitée | Taille plus grande |

---

## 3. Partie pratique

---

## 3.1 Préparation du stockage
Laravel utilise le dossier `storage` pour stocker les fichiers.

Organisation recommandée :
- storage/app/public/images
- storage/app/public/videos

```bash
php artisan storage:link
```
**Explication :**
Cette commande permet d’accéder aux fichiers uploadés depuis le navigateur, ainsi créer le lien entre `storage` et `public` :


## 3.2 Création du formulaire d’upload
 📍 Fichier : resources/views/upload.blade.php
```bash
<form method="POST"
      action="{{ route('upload.store') }}"
      enctype="multipart/form-data">

    @csrf

    <label>Image</label>
    <input type="file" name="image">

    <label>Vidéo</label>
    <input type="file" name="video">

    <button type="submit">Envoyer</button>
</form>
```
**Explication :**
- multipart/form-data : obligatoire pour envoyer des fichiers
- type="file" : permet de choisir un fichier
- name="image" et name="video" : utilisés dans le controller

## 3.3 Traitement dans le controller
📍 Fichier : app/Http/Controllers/UploadController.php
-  Méthode : store()
```bash
public function store(Request $request)
{
    $request->validate([
        'image' => 'nullable|image|mimes:jpg,png,webp|max:2048',
        'video' => 'nullable|mimes:mp4|max:20000',
    ]);
```
**Explication :**
- Vérifie le type des fichiers
- Limite la taille
- Sécurise l’application

## 3.3.2 Upload de l’image
```bash
    $imagePath = null;

    if ($request->hasFile('image')) {
        $imagePath = $request->file('image')
                             ->store('images', 'public');
    }
```
**Explication :**
- $imagePath = null : valeur par défaut
- hasFile('image') : vérifie si une image est envoyée
- file('image') : récupère le fichier
- store() : stocke l’image dans storage/app/public/images

## 3.3.3 Upload de la vidéo
```bash
    $videoPath = null;

    if ($request->hasFile('video')) {
        $videoPath = $request->file('video')
                             ->store('videos', 'public');
    }
```
**Explication :**
- Même logique que pour l’image
- Dossier différent car les vidéos sont plus lourdes

## 3.3.4 Sauvegarde des chemins
```bash
    // Exemple de sauvegarde
    Model::create([
        'image' => $imagePath,
        'video' => $videoPath,
    ]);
}
```
**Explication :**
- Seuls les chemins sont enregistrés
- Les fichiers restent dans storage

## 3.4 Affichage des fichiers uploadés
 Fichier : resources/views/show.blade.php
 - Affichage de l’image
```bash
 <img src="{{ asset('storage/' . $imagePath) }}" width="300">
```
 - Affichage de video
 ```bash
 <video controls width="400">
    <source src="{{ asset('storage/' . $videoPath) }}" type="video/mp4">
</video>
```
**Explication :**
- asset() génère l’URL du fichier
- storage/ correspond au lien créé avec storage:link

## 5. Conclusion
Ce LAB permet de comprendre :
- Le principe de l’upload des fichiers
- Les étapes pratiques dans Laravel


Il constitue une base solide pour tout projet Laravel utilisant des fichiers ou des média
