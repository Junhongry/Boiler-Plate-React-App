# 🚀 Fullstack Template (React + Node + Prisma)

A clean, scalable, and production-ready fullstack template built with:

* React + TypeScript (Vite)
* Node.js + Express
* PostgreSQL + Prisma
* Monorepo structure

This template is designed to help you **ship fast**, **stay organized**, and **leverage AI tools efficiently** without sacrificing code quality.

---

# 📦 Tech Stack

## Frontend

* React (Vite)
* TypeScript

## Backend

* Node.js
* Express
* Prisma ORM

## Database

* PostgreSQL

---

# 📁 Project Structure

```
my-app/
  client/        # Frontend (React)
  server/        # Backend (Node + Prisma)
  shared/        # Shared types (optional)
```

### Backend Structure

```
server/src/
  controllers/   # HTTP layer
  services/      # Business logic
  repositories/  # Database access (Prisma only)
  middleware/    # Express middleware
  lib/           # Shared utilities (e.g., prisma client)
```

---

# ⚙️ Setup

## 1. Clone the repo

```
git clone <your-repo-url>
cd my-app
```

## 2. Setup environment variables

```
cd server
cp .env.example .env
```

Update `.env`:

```
DATABASE_URL="postgresql://USER:PASSWORD@localhost:5432/YOUR_DB"
```

---

## 3. Start PostgreSQL locally

Make sure PostgreSQL is installed and running.

Create a database:

```
psql postgres
CREATE DATABASE your_db;
\q
```

---

## 4. Run migrations

```
cd server
npx prisma migrate dev
```

---

## 5. Start the app

From root:

```
npm run dev
```

* Frontend: [http://localhost:5173](http://localhost:5173)
* Backend: [http://localhost:4000](http://localhost:4000)

---

# 🧠 Architecture Principles

## 1. Separation of Concerns

```
Route → Controller → Service → Repository → Database
```

* Controllers: handle request/response
* Services: business logic
* Repositories: database queries only

---

## 2. Prisma Usage

* Prisma is only used inside repositories
* No direct DB access in controllers or services

---

## 3. Feature-Based Frontend

Group logic by feature instead of file type:

```
features/
  auth/
  meals/
```

---

# 💡 Best Practices

## ✅ Keep AI usage efficient

* Use AI for small, focused tasks
* Avoid large prompts
* Work file-by-file

## ✅ Keep business logic out of controllers

* Controllers should stay thin

## ✅ Use migrations consistently

* Never manually modify DB schema

## ✅ Use environment variables

* Never commit `.env`

---

# 🚫 What NOT to do

* ❌ Don’t mix Prisma calls in services
* ❌ Don’t commit `.env`
* ❌ Don’t generate entire apps with AI in one prompt

---

# 🔁 Reusing This Template

```
git clone <template-repo> new-project
cd new-project
```

Then:

```
cd server
cp .env.example .env
npx prisma migrate dev
npm run dev
```

---

# 📈 Future Improvements

* Add authentication (JWT)
* Add validation (Zod)
* Add logging
* Add testing (Jest / Vitest)

---

# 🧑‍💻 Author Notes

This template is optimized for:

* rapid prototyping
* clean architecture
* AI-assisted development workflows

---

# ⭐ License

MIT
