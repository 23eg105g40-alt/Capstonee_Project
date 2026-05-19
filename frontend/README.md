
# BlogApp WriteArc — Frontend

This is the **frontend** of the *BlogApp WriteArc* — a blogging platform built with **React**. It connects with the backend API to enable users, authors, and admins to interact with blog posts and comments.

---

## 📌 Table of Contents

1. [About](#about)  
2. [Tech Stack](#tech-stack)  
3. [Folder Structure](#folder-structure)  
4. [Installation](#installation)  
5. [Available Scripts](#available-scripts)  
6. [Environment Variables](#environment-variables)  
7. [Features](#features)  
8. [Component Overview](#component-overview)  
9. [API Interaction](#api-interaction)  
10. [Contributing](#contributing)  
11. [License](#license)

---

## 🧠 About

This React app serves as the **user interface** for the blogging platform.  
Users can register, login, view articles, comment, while authors can create/edit their posts.

---

## 🛠️ Tech Stack

- React (JSX + Functional components)  
- Vite for fast development & build  
- React Router for client-side routing  
- Zustand as store  
- Tailwind CSS for styling
- Axios for HTTP calls

---

## 📁 Folder Structure

```

frontend
├── public/
│   ├── index.html
│   └── vite.svg
├── src/
│   ├── assets/
│   ├── components/
│   ├── store/
│   ├── styles/
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── .gitignore
├── eslint.config.js
├── package.json
├── package-lock.json
├── README.md
├── vercel.json
└── vite.config.js

````
:contentReference[oaicite:0]{index=0}

---

## 🚀 Installation

1. Navigate to the frontend folder:

```bash
cd blogapp-WriteArc/frontend
````

2. Install dependencies:

```bash
npm install
```

---

## ▶️ Available Scripts

In the frontend directory, you can run:

### Start development server

```bash
npm run dev
```

* Runs the React app in development mode with live reload.

### Create production build

```bash
npm run build
```

* Bundles and optimizes the app for deployment.

### Preview production build

```bash
npm run preview
```

* Locally preview the production build.

*Note: These commands are provided by **Vite**.*

---

## 🔐 Environment Variables

Create a `.env` file in `frontend/` (optional, if you use environment variables):

```
VITE_API_BASE_URL=http://localhost:5000
```

* `VITE_API_BASE_URL`: Backend base URL for API calls.

---

## ✨ Features

* Responsive UI built with Tailwind CSS
* API communication using Axios
* Role-based pages for User and Author
* Authentication with httpOnly cookie session
* Dynamic article and comment rendering
* Navigation between pages

---

🔗 API Interaction

All API calls are handled using Axios.

Example pattern used in the project:

axios.get(`${import.meta.env.VITE_API_BASE_URL}/user/articles`, {
  withCredentials: true,
});
withCredentials: true is required because authentication uses httpOnly cookies.

🎨 Styling

The entire UI is styled using Tailwind CSS utility classes, making the design responsive and clean without writing custom CSS for most components.

---

## 🧩 Component Overview

Below is a *general overview* of how the components are likely organized based on the folder structure:

```
src/
├── assets/          ← Images, icons, static media
├── components/      ← All reusable UI components
│   ├── Navbar.jsx   ← Top navigation bar
│   ├── Footer.jsx   ← App footer
│   ├── ArticleCard.jsx ← Displays article preview
│   ├── CommentCard.jsx ← Renders a comment
│   ├── LoginForm.jsx ← Login UI
│   ├── RegisterForm.jsx ← Register UI
│   └── ...others
├── store/           ← Zustand or global store setup
├── styles/          ← CSS / global styling
├── App.jsx          ← App routes and layout
├── main.jsx         ← React DOM render + context providers
└── index.css        ← Global CSS
```

*(Adjust names based on your actual component files.)*

---

## 🔗 API Interaction

The frontend communicates with the backend APIs (from your backend server):

* **Login** — `/common/login`
* **Logout** — `/common/logout`
* **Register (User/Author)** — `/user/users`, `/author/users`
* **Fetch all articles** — `/user/articles`
* **Fetch own author articles** — `/author/articles/:id`
* **Create / Edit / Comment** → appropriate protected endpoints

👉 These calls are typically made through **axios** or **fetch** inside service/helper functions.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create your branch (`git checkout -b feature/my-ui-feature`)
3. Commit your changes
4. Push (`git push origin feature/my-ui-feature`)
5. Create a Pull Request

---


### Using Toast in React app

    - npm install react-hot-toast
    - Add Toaser component at Root
        <Toaster position="top-center" reverseOrder={false} /> in App.jsx

    - Use toast with custom messages
        Eg:
            import toast from "react-hot-toast";

            if (resObj.status === 201) {
                toast.success("Account created successfully");
                navigate("/login");
            }

### From UserProfile component,

    - Read articles of all AUthors
    - Display them in the form of Grid of cards
                1 card for extra  small
                2 cards for small
                3 cards for medium
                4 cards from large screen onwards

### From AuthorProfile component,

    - Read articles of his own
    - Display them in the form of Grid of cards
                1 card for extra  small
                2 cards for small
                3 cards for medium
                4 cards from large screen onwards

### When User /Author click on specific article from Articles list

    - Navigate to "ArticleByID" component along with selected article
    - Display the  article title, category, content along with author title & time stamps in IST format


## 📄 License
    **MIT** 
