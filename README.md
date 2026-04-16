# 🛒 TP CRUD EJS - Product Management

## 📌 Description

This project is a simple web application for **product management** built using:

* Node.js
* Express.js
* MongoDB
* EJS (Template Engine)

It allows performing basic CRUD operations:

* ➕ Add a product (CREATE)
* 📋 View products (READ)
* ✏️ Update a product (UPDATE)
* ❌ Delete a product (DELETE)

---

## ⚙️ Installation

### 1️⃣ Clone the project

```bash
git clone <repo-url>
cd tp-crud-ejs
```

### 2️⃣ Install dependencies

```bash
npm install
```

### 3️⃣ Start MongoDB

Make sure MongoDB is running:

```bash
mongod
```

### 4️⃣ Run the server

```bash
node server.js
```

📍 The application will be available at:

```
http://localhost:3000
```

---

## 📁 Project Structure

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

## 🧠 Model (Product)

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

## 🚀 Features

### 🔍 READ (Display)

* Route: `/`
* Displays all products in a table

### ➕ CREATE (Add)

* GET `/add` → show form
* POST `/add` → add product

### ✏️ UPDATE (Edit)

* GET `/edit/:id` → edit form
* PUT `/edit/:id` → update product

### ❌ DELETE (Remove)

* DELETE `/delete/:id` → delete product

---

## 🛠️ Technologies Used

* Node.js
* Express.js
* MongoDB + Mongoose
* EJS
* Body-parser
* Method-override

---

## 📌 Notes

* MongoDB must be running before starting the project
* Make sure port **27017** is available
* Connection URL:

```
mongodb://127.0.0.1:27017/tpcrud
```

---

## 👨‍💻 Author

* Project created as part of **Full Stack Web Development training**

---

## ⭐ Bonus

You can improve this project by adding:

* Bootstrap for styling 🎨
* Form validation ✅
* Authentication system 🔐
* REST API 🌐

---
