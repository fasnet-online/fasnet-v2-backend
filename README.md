# FASNet V2 - Core API & Backend

Welcome to the central nervous system of **FASNet V2**. This repository houses the backend engine built to handle the complex, relational data structures required for a full university ecosystem. 

Unlike standard dashboards, this backend is engineered around a Contextual Role-Based Access Control (CRBAC) matrix, allowing it to seamlessly manage overlapping student, batch, and society relationships for the Faculty of Applied Sciences.

## ⚙️ Tech Stack

* **Runtime:** Node.js
* **Framework:** Express.js v5 (RESTful API architecture)
* **Language:** TypeScript for strict data validation and type safety.
* **Database:** PostgreSQL for robust, relational data integrity.
* **ORM:** Prisma, providing a clean, type-safe database interaction layer.
* **Real-time:** Socket.io for instant society announcements and academic alerts.

## 🛠️ Local Development Setup

**1. Clone the repository:**
```bash
git clone [https://github.com/KasunHerath-dev/fasnet-v2-backend.git](https://github.com/KasunHerath-dev/fasnet-v2-backend.git)
cd fasnet-v2-backend
````

**2. Install dependencies:**

```bash
npm install
```

**3. Configure Environment Variables:**
Copy the template environment file and configure your PostgreSQL connection string, JWT secrets, and any cloud storage keys.

```bash
cp .env.example .env
```

**4. Database Setup (Prisma):**
Ensure your local PostgreSQL server is running, then push the schema and generate the Prisma Client.

```bash
npx prisma db push
npx prisma generate
```

**5. Run the development server:**

```bash
npm run dev
```

The server will start on `http://localhost:5000`.

## 📁 Key Directory Structure

  * `/prisma`: Contains `schema.prisma` (your database architecture) and migration files.
  * `/src/controllers`: Business logic handling the requests and responses.
  * `/src/routes`: Express route definitions mapping URLs to controllers.
  * `/src/middlewares`: Security layers, JWT authentication, and CRBAC validation.
  * `/src/services`: External integrations (e.g., AWS S3 uploads, email providers).
  * `/src/sockets`: WebSockets logic for real-time notification channels.

## 🤝 Contributing

We are building this to enterprise standards. Please read our Contribution Guidelines in the [FASNet Docs](https://www.google.com/search?q=https://github.com/KasunHerath-dev/fasnet-docs) repository before submitting a Pull Request.

  * Ensure all new endpoints are strictly typed with TypeScript interfaces.
  * Do not write raw SQL; use Prisma Client for all database transactions.
  * Feature branches must be created from `main` and require review before merging.

-----

*Initiated by the 23/24 Batch | Lead Maintainer: [@KasunHerath-dev](https://github.com/KasunHerath-dev) (Kasun Herath)*

```
