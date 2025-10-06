# 🌍 World Capital Quiz

<p align="center">
  <img src="https://redeem-innovations.com/wp-content/uploads/2025/10/Screenshot-2025-10-04-at-10.49.15-PM.png" alt="World Capital Quiz Screenshot" />
</p>

---

## 📖 Overview

**World Capital Quiz** is a simple quiz game built with **Node.js**, **Express**, and **PostgreSQL**, where users test their knowledge of world capitals.  
Each time you load the page, a random country is selected from a database, and you try to guess its capital city.

---

## ✨ Features

- 🎲 Randomly selects a country from the `capitals` table in PostgreSQL
- ✅ Tracks total correct answers for the session
- 📄 Displays questions and results dynamically using **EJS templates**
- 🗄️ Connected to a **PostgreSQL** database instead of hardcoded quiz data
- 🎨 Serves static assets from a `public` folder

---

## ⚙️ Tech Stack

| Layer              | Technology                               |
| ------------------ | ---------------------------------------- |
| **Backend**        | Node.js, Express                         |
| **Database**       | PostgreSQL (`pg` client)                 |
| **Templating**     | EJS                                      |
| **Middleware**     | body-parser                              |
| **Styling/Assets** | Static files served from `public` folder |

---

## 🚀 Getting Started

### 1️⃣ Clone the repository

```bash
git clone https://github.com/mina-y-khalil/world_capital_quiz.git
cd world_capital_quiz
```

### 2️⃣ Install dependencies

```bash
npm install
```

### 3️⃣ Set up PostgreSQL

Create a new database named **world** and a table named **capitals**:

```sql
CREATE DATABASE world;

\c world;

CREATE TABLE capitals (
  id SERIAL PRIMARY KEY,
  country VARCHAR(255) NOT NULL,
  capital VARCHAR(255) NOT NULL
);

```

---

### 4️⃣ Run the server

```bash
nodemon index.js
```

### 5️⃣ Open the app

Visit 👉 [http://localhost:3000](http://localhost:3000)

---

## 🧭 Project Structure

```
world-capital-quiz/
├── public/          # Static assets (CSS, images, etc.)
├── views/           # EJS templates
├── index.js         # Main Express server file
├── package.json
└── README.md
```

---

## 💡 Example Code Snippet

```js
db.query("SELECT * FROM capitals", (err, res) => {
  if (err) {
    console.error("Error executing query", err.stack);
  } else {
    quiz = res.rows;
  }
  db.end();
});
```

This dynamically replaces the static quiz data with data from your PostgreSQL database.

---

## 🧩 Future Improvements

- Add more countries and capitals
- Show hints or multiple-choice options
- Track high scores across sessions
- Add user login for personalized gameplay

---

## 🪪 License

This project is licensed under the **MIT License**.  
You’re free to use, modify, and share it for educational or personal use.

---

## 🌐 Connect with Me

Let’s connect and share ideas!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mina%20Y.%20Khalil-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/mina-y-khalil/)
