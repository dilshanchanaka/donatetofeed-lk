# DonateToFeed.lk 🍲

A full-stack web platform connecting surplus food donors with charities, NGOs, and individuals facing food insecurity across Sri Lanka — turning excess food into meals instead of waste.

> Final Year Computing Project (CSE5015) — HD in Computing & Software Engineering, ICBT Campus (Cardiff Metropolitan University)

---

## 📖 Overview

In Sri Lanka, tons of edible food is wasted daily by restaurants, hotels, supermarkets, and households, while thousands of people struggle with food insecurity. DonateToFeed.lk bridges this gap with a centralized, real-time platform where donors can list surplus food and recipients — including NGOs, shelters, and individuals — can find, request, and coordinate pickup of that food quickly and transparently.

The project was led as Project Manager across a 5-member team, following Agile methodology from requirements gathering through deployment.

---

## ✨ Features

- **Role-based accounts** — Donor, Receiver, and Admin, each with tailored dashboards and permissions
- **Food listing management** — donors create, update, and remove listings with type, quantity, expiry date, pickup location, and photos
- **Search & filter** — receivers browse available donations by category, location, and expiry
- **Request workflow** — receivers request listings; donors approve or reject, with status tracking
- **Real-time in-app chat** — donors and receivers coordinate pickup directly via Socket.IO-powered messaging
- **Feedback & ratings** — receivers rate food quality and upload photos after pickup
- **Admin dashboard** — manage users, moderate listings, view platform-wide statistics and analytics
- **Secure authentication** — JWT-based login with bcrypt password hashing

---

## 🛠️ Tech Stack (MERN)

| Layer | Technology |
|---|---|
| Frontend | React 19, Vite, React Router v7, React Icons |
| Backend | Node.js, Express 5 |
| Database | MongoDB, Mongoose |
| Real-time | Socket.IO |
| Auth | JWT (jsonwebtoken), bcrypt/bcryptjs |
| File Uploads | Multer |
| Config | dotenv, CORS |

---

## 📂 Project Structure

```
DonateToFeed.lk/
└── donateTofeed01/
    ├── backend/
    │   ├── middleware/       # Auth middleware (JWT verification)
    │   ├── models/            # Mongoose schemas (User, Donation, FeedRequest, Feedback, ChatMessage, etc.)
    │   ├── routes/             # API routes (donations, requests, feedback, chat, stats, users)
    │   ├── uploads/              # User-uploaded images (gitignored)
    │   ├── server.js               # Express app entry point
    │   └── .env                      # Environment variables (gitignored — see setup below)
    └── frontend/
        └── src/
            ├── components/     # React components (Dashboard, Chat, DonationForm,
            │                   #   AvailableDonations, Admin, Feedback, etc.)
            ├── App.jsx
            └── main.jsx
```

---

## ⚙️ Setup & Installation

### Prerequisites
- [Node.js](https://nodejs.org/) (v18+)
- A [MongoDB Atlas](https://www.mongodb.com/atlas) cluster (or local MongoDB instance)

### Backend Setup

```bash
cd donateTofeed01/backend
npm install
```

Create a `.env` file in `donateTofeed01/backend/` with:
```env
MONGO_URI=your_mongodb_connection_string
PORT=5000
JWT_SECRET=your_own_secret_key
```

Run the server:
```bash
npm start
```

### Frontend Setup

```bash
cd donateTofeed01/frontend
npm install
npm run dev
```

The app will be available at `http://localhost:5173`.

---

## 🔒 Security Note

This is an academic project. `.env` files containing database credentials and JWT secrets are excluded from version control via `.gitignore` — you'll need to supply your own values to run the project locally. Never commit real credentials to a public repository.

---

## 🌍 Alignment with Sustainable Development Goals

DonateToFeed.lk supports:
- **SDG 2 — Zero Hunger**
- **SDG 12 — Responsible Consumption and Production**

---

## 📌 Status

This project was developed as a final year computing capstone project and is not actively maintained for production use.

---

## 👤 Author

**H.M. Chanaka Dilshan Jayarathna**
Project Manager & Developer
HD in Computing & Software Engineering, ICBT Campus (Cardiff Metropolitan University)
