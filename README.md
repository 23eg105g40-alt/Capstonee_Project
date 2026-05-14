# 📝 MERN Blog Application

A full-stack Blogging Platform built with the MERN stack where users can create, read, update, and delete articles, upload images, comment, and receive real-time notifications.

---

## 🚀 Tech Stack

**Frontend**

* React
* Vite
* Axios
* React Router

**Backend**

* Node.js
* Express
* MongoDB
* Mongoose
* JWT
* Multer
* Cloudinary


---

## ✨ Features

* 👤 User & Author Authentication (JWT based)
* 📝 Create / Edit / Delete Articles
* 🖼️ Image Upload with Cloud Storage
* 💬 Comment System on Articles
* 🔐 Protected Routes & Role-based Access
* 📦 RESTful API Architecture
* 🌐 Responsive UI

---

## 📸 Image Upload Flow

1. Image received via Multer
2. Uploaded to Cloudinary
3. URL stored in MongoDB
4. Served to frontend

---

## 🔐 Authentication Flow

1. User logs in
2. Server generates JWT
3. Token stored in Cookies
4. Protected routes verified using middleware

---

## 🧪 Future Improvements

* 👍 Like / Bookmark articles
* 🔍 Search & filter by category
* 🧑‍💼 Author profiles
* 📨 Email notifications
* 📊 Admin dashboard

