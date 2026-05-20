# CBT and ERP App - Setup Guide

## Project Overview
Building a full-stack application to monitor MDD, OCD, and other mental illnesses from scratch for a production-ready GitHub portfolio.

---

## 🛠️ The Architecture & Setup Blueprint

### System Architecture

```
+---------------------------------------+
|         CLIENT (Next.js Frontend)     |
|   React Components + Tailwind UI      |
+-------------------+-------------------+
                    |
        POST / GET (JSON Payload)
                    |
+-------------------v-------------------+
|          SERVER (Next.js API Routes)  |
|   Prisma Client / Controller Filters  |
+-------------------+-------------------+
                    |
             Object Mapping
                    |
+-------------------v-------------------+
|         DATABASE (Local SQLite)       |
|   Isolated, Encrypted relational tables|
+---------------------------------------+
```

---

## 📋 Initial Terminal Setup

### Step 1: Prerequisites
Go to your local storage or browser and install **Node.js** and give permissions to Windows Shell.

Open your machine's **terminal** (Windows PowerShell), find your working directory, and run these commands:

### Step 2: Install create-next-app Globally

**Run this once globally:**

```powershell
npm install -g create-next-app
```

### Step 3: Create Your Next.js Project

**Then you can run:**

```powershell
create-next-app mind-console --typescript --tailwind --app --src-dir=false --yes
```

> **Note:** Without waiting for npx to fetch it each time, the global install lets you use the command directly.

### Step 4: Verify npm Cache

**Make sure your npm cache is healthy:**

```powershell
npm cache verify
```

### Step 5: Navigate to Project & Install Dependencies

**Run only once after the project is created:**

```powershell
cd mind-console
```

**Install required packages:**

```powershell
npm install lucide-react @prisma/client
```

**Install Prisma as dev dependency:**

```powershell
npm install prisma --save-dev
```

**Initialize Prisma with SQLite:**

```powershell
npx prisma init --datasource-provider sqlite
```

---

## ✅ Setup Complete!

Your project structure is now ready with:
- ✨ Next.js with TypeScript
- 🎨 Tailwind CSS for styling
- 📦 Prisma ORM for database management
- 💾 SQLite for local database
- 🎭 Lucide React for icons

You're all set to start building your mental health monitoring application!
