# ⚡ TaskForge - Full-Stack Task & Project Management Web App

A modern, high-performance Full-Stack Web Application built with **Node.js**, **Express.js**, **EJS Templates**, **Mongoose (MongoDB ODM)**, and **Nodemon**.

Designed with a sleek obsidian glassmorphism UI, real-time status switching, advanced search & filtering, and full CRUD capabilities.

---

## 🚀 Tech Stack

- **Runtime**: Node.js
- **Backend Framework**: Express.js
- **Database & ODM**: MongoDB & Mongoose
- **View Engine**: EJS (Embedded JavaScript Templates)
- **Styling**: Modern Vanilla CSS (Custom Design Tokens, Glassmorphism, Dark Mode)
- **Frontend Interactivity**: Vanilla JavaScript (Async Fetch API, DOM manipulation)
- **Dev Tooling**: Nodemon (Auto-reloading on code & template changes)

---

## 📁 Project Structure

```
BackendProject/
├── config/
│   └── db.js                 # MongoDB connection & reconnection handler
├── models/
│   └── Task.js               # Mongoose schema, enums, virtuals & validations
├── controllers/
│   └── taskController.js     # MVC controller handling CRUD, stats & search
├── routes/
│   └── taskRoutes.js         # RESTful & API routes
├── views/
│   ├── partials/
│   │   ├── head.ejs          # HTML <head>, Google Fonts & CSS link
│   │   ├── navbar.ejs        # Responsive top navbar with online indicator
│   │   └── footer.ejs        # Footer and toast containers
│   ├── index.ejs             # Main Dashboard: Analytics cards, search & task grid
│   ├── new.ejs               # Form to create new task
│   ├── edit.ejs              # Form to edit existing task
│   ├── show.ejs              # Detailed single-task view
│   └── 404.ejs               # Custom 404 Error page
├── public/
│   ├── css/
│   │   └── style.css         # Modern design system & animations
│   └── js/
│       └── main.js           # Client-side AJAX status toggles, toasts, modals
├── .env.example              # Example environment configuration
├── .env                      # Local environment configuration
├── .gitignore                # Git ignore rules
├── package.json              # Project dependencies & scripts
├── server.js                 # Server entry point
└── README.md                 # Project documentation
```

---

## 🛠️ Getting Started

### 1. Prerequisites
- [Node.js](https://nodejs.org/) (v16+ recommended)
- [MongoDB](https://www.mongodb.com/) (Local instance or MongoDB Atlas cluster)

### 2. Installation
Dependencies are already installed. If running afresh:
```bash
npm install
```

### 3. Environment Configuration
Check `.env` (pre-configured with defaults):
```env
PORT=3000
NODE_ENV=development
MONGODB_URI=mongodb://127.0.0.1:27017/taskforge_db
```
*(If using MongoDB Atlas, replace `MONGODB_URI` with your connection string).*

### 4. Running the Application

#### Development Mode (with Nodemon auto-restart):
```bash
npm run dev
```

#### Production / Standard Mode:
```bash
npm start
```

Visit **[http://localhost:3000](http://localhost:3000)** in your browser.

---

## ✨ Features & Capabilities

- 📊 **Dynamic Analytics Dashboard**: Live metrics for Total, In Progress, Pending, Completed, and Overdue tasks.
- 🔍 **Search & Multi-Filter**: Search titles, descriptions, and tags in real-time, plus filter by Category, Priority, and Status.
- ⚡ **Instant Status Switcher**: Update task statuses directly from cards without refreshing the entire page via asynchronous API calls.
- 🗓️ **Deadline & Overdue Tracking**: Automatic visual indicators for overdue tasks.
- 🎨 **Sleek Aesthetic**: Glowing obsidian glassmorphism cards, Google Inter font, vibrant status badges, responsive mobile layout.
- 🛡️ **Graceful Fault Tolerance**: Informative UI warnings if the database server is offline.

---

## 📡 RESTful Endpoints & Routes

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/` or `/tasks` | Dashboard with stats, search & filters |
| `GET` | `/tasks/new` | Render task creation form |
| `POST` | `/tasks` | Create new task in MongoDB |
| `GET` | `/tasks/:id` | View task details & metadata |
| `GET` | `/tasks/:id/edit`| Render task editing form |
| `PUT` | `/tasks/:id` | Update task data (`method-override`) |
| `DELETE` | `/tasks/:id` | Delete task from database |
| `PATCH` | `/api/tasks/:id/status` | AJAX endpoint for instant status update |
# Backend-project-
# Backend-project-
# Backend-project-
