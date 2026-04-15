
# 🛒 TP CRUD EJS - Gestion des Produits

## 📌 Description

Ce projet est une application web بسيطة pour **Gestion des produits** باستخدام:

* Node.js
* Express.js
* MongoDB
* EJS (Template Engine)

كاتدير العمليات الأساسية:

* ➕ Ajouter un produit (CREATE)
* 📋 Afficher les produits (READ)
* ✏️ Modifier un produit (UPDATE)
* ❌ Supprimer un produit (DELETE)

---

## ⚙️ Installation

### 1️⃣ Cloner le projet

```bash
git clone <repo-url>
cd tp-crud-ejs
```

### 2️⃣ Installer les dépendances

```bash
npm install
```

### 3️⃣ Lancer MongoDB

تأكد أن MongoDB خدام:

```bash
mongod
```

### 4️⃣ Lancer le serveur

```bash
node server.js
```

📍 L’application sera disponible sur :

```
http://localhost:3000
```

---

## 📁 Structure du projet

```
tp-crud-ejs/
│
├── models/
│   └── Product.js
│
├── views/
│   ├── index.ejs
│   ├── add.ejs
│   └── edit.ejs
│
├── server.js
└── package.json
```

---

## 🧠 Modèle (Product)

```js
const mongoose = require("mongoose");

const ProductSchema = new mongoose.Schema({
  name: String,
  price: Number,
  quantity: Number
});

module.exports = mongoose.model("Product", ProductSchema);
```

---

## 🚀 Fonctionnalités

### 🔍 READ (Afficher)

* Route : `/`
* Affiche tous les produits dans un tableau

### ➕ CREATE (Ajouter)

* GET `/add` → afficher formulaire
* POST `/add` → ajouter produit

### ✏️ UPDATE (Modifier)

* GET `/edit/:id` → formulaire modification
* PUT `/edit/:id` → update produit

### ❌ DELETE (Supprimer)

* DELETE `/delete/:id` → supprimer produit

---

## 🛠️ Technologies utilisées

* Node.js
* Express.js
* MongoDB + Mongoose
* EJS
* Body-parser
* Method-override

---

## 📌 Remarques

* MongoDB doit être actif avant de lancer le projet
* Vérifier que le port **27017** est disponible
* URL de connexion :

```
mongodb://127.0.0.1:27017/tpcrud
```

---

## 👨‍💻 Auteur

* Projet réalisé dans le cadre de la formation **Développement Digital Full Stack**

---

## ⭐ Bonus

يمكنك تطوير المشروع بإضافة:

* Bootstrap للتصميم 🎨
* Validation des formulaires ✅
* Authentification 🔐
* API REST 🌐

---
