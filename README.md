# LibraryHub 📚

LibraryHub is a **static, multi-page bookstore web application** that allows users to browse, purchase, and rent books through a browser-based interface. It is built using **HTML, CSS, and vanilla JavaScript** and deployed as a **GitHub Pages static site** with automated CI/CD.

---

## ✨ Features

- Browse a catalog of **32 books** across multiple genres
- Dual pricing model: **Buy or Rent** each book
- Search and filter books by genre
- Shopping cart with quantity and total price calculation
- Client-side authentication (User / Admin roles)
- Featured books on the home page
- About & contact pages
- Fully static deployment (no backend required)

---

## 🛠 Tech Stack

### Frontend
- **HTML5** – Multi-page application structure
- **CSS3** – Global and page-specific stylesheets
- **JavaScript (ES6)** – Modular client-side logic
- **Font Awesome** – Icons (CDN)

### Data Layer
- **Static JavaScript data** (`DB/books.js`)
- No backend or server-side database

### Infrastructure
- **GitHub Pages** – Static hosting
- **GitHub Actions** – Automated deployment
- **HTTPS** – Enabled by default

---

## 🧱 Architecture Overview

LibraryHub follows a **traditional Multi-Page Application (MPA)** architecture:

- Each major screen has its own HTML file
- Navigation uses standard browser routing
- Dynamic behavior is handled with vanilla JS modules
- Book data is statically defined and imported via ES6 modules

There is **no backend server** — all logic runs client-side.

---

## 🚀 Setup & Installation

### Option 1: Run Locally (Recommended for Development)

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/libraryhub.git
   cd libraryhub
   ```

2. **Serve the project using a local server**

   Because ES6 modules are used, you must use a local server.

   **Using VS Code Live Server** (easiest):
   - Install the *Live Server* extension
   - Right-click `index.html` → *Open with Live Server*

   **Using Python**:
   ```bash
   python -m http.server 5500
   ```

3. **Open in browser**
   ```text
   http://localhost:5500
   ```

---

### Option 2: GitHub Pages Deployment

1. Push the repository to GitHub
2. Ensure `.github/workflows/static.yml` exists
3. Enable **GitHub Pages** (if not already enabled)
4. Every push to `main` triggers automatic deployment

---

## 📁 Project Structure

```text
.
├── index.html          # Landing page
├── catalog.html        # Book catalog
├── cart.html           # Shopping cart
├── about.html          # About & team info
├── contact.html        # Contact page
├── signIn.html         # Login
├── signUp.html         # Registration
├── dashboard.html      # User dashboard (referenced)
├── DB/
│   └── books.js        # Static book & cart data
├── JS/
│   ├── aut.js          # Authentication logic
│   ├── catalog.js      # Catalog functionality
│   ├── cart.js         # Cart logic
│   └── main.js         # Shared utilities
├── CSS/
│   ├── styel.css       # Global styles
│   └── page-specific CSS
└── .github/workflows/
    └── static.yml      # GitHub Pages deployment
```

---

## 📚 Book Data Model

Books are defined statically in `DB/books.js`:

```js
{
  name: "Atomic Habits",
  author: "James Clear",
  genre: "Self-help",
  page: 320,
  published: 2018,
  purchasedPrice: 20,
  rentPrice: 3,
  decription: "Atomic Habits is a guide...",
  image: "Assets/IMG/atomic_habit.jpg",
  Id: 1
}
```

---

## 🔐 Authentication (Client-Side)

- Implemented entirely in JavaScript (`JS/aut.js`)
- Sign In / Sign Up pages
- Role selection: **User** or **Admin**
- Session checks handled client-side
- No server-side validation (demo/academic purpose)

---

## 🧪 Development Notes

- Designed for **learning and demonstration**
- No build step or bundler required
- Works entirely as static files
- Easily extensible with a backend in the future

---

## 📄 License

This project is intended for academic, learning, and portfolio use. Add a license if publishing publicly.

---

**LibraryHub – Static Bookstore Web App**

