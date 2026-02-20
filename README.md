# 📘 CreatorIQ — AI-Powered YouTube Analytics & Content Intelligence Platform

![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-Typed-3178C6?style=flat&logo=typescript)
![Tailwind](https://img.shields.io/badge/Tailwind-CSS-38B2AC?style=flat&logo=tailwind-css)
![Clerk](https://img.shields.io/badge/Clerk-Auth-6C47FF?style=flat&logo=clerk)
![Inngest](https://img.shields.io/badge/Inngest-Background%20Jobs-E46C2A?style=flat)
![Neon](https://img.shields.io/badge/Neon-PostgreSQL-00E699?style=flat)
![BrightData](https://img.shields.io/badge/BrightData-Scraping-FF6B35?style=flat)
![Vercel](https://img.shields.io/badge/Deployed-Vercel-000000?style=flat&logo=vercel)

> An AI SaaS platform that helps YouTubers, creators, and marketers analyze channels, generate thumbnails, track keyword trends, and gain deep content insights — powered by **Next.js 14, Inngest, BrightData, Neon DB, and Clerk Auth**.

🐙 **GitHub:** [DishaDewangan/CreatorIQ](https://github.com/DishaDewangan/CreatorIQ)

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Project Pipeline](#project-pipeline)
- [Setup & Installation](#setup--installation)
- [Database Setup](#database-setup-drizzle--neon)
- [Key Implementations](#key-implementations)

---

## 📖 Overview

**CreatorIQ** is a production-grade AI SaaS platform built with Next.js 14 App Router and TypeScript. It provides YouTube creators with AI-generated thumbnails, channel analytics via BrightData scraping, content idea generation using LLMs, and trending keyword exploration — all backed by Neon PostgreSQL, Drizzle ORM, and Inngest background job processing.

---

## ✨ Features

### 🎨 AI Thumbnail Generator
- Generates high-quality YouTube thumbnails using AI models
- Stores and displays complete thumbnail history
- Thumbnail search functionality
- Optimized for YouTube aspect ratio (95%+ accuracy)

### 📊 YouTube Channel Analytics
- Fetch video metadata using BrightData scraping (1K+ videos daily)
- Analyze outlier videos and detect high-performing patterns
- Engagement and performance insights
- Trend detection across channels

### 💡 AI Content Generator
- AI-powered video script ideas
- Title and description suggestions with SEO scoring
- Topic breakdown and niche analysis

### 🔎 Trending Keyword Explorer
- Fetch trending search queries by niche
- Keyword difficulty scoring
- Competitor comparison and keyword gap analysis

### 🧾 Billing & Usage
- Usage-based billing system
- Tiered subscription plans
- Usage limits integrated with Clerk

### 🔒 Authentication
- Secure login via Clerk
- Role-based workflows
- Session and token management

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | Next.js 14 (App Router), React 18, TypeScript, Tailwind CSS, ShadCN UI |
| **Backend** | Next.js Server Actions, Inngest (background jobs), BrightData API, OpenAI / Gemini API |
| **Database** | Neon PostgreSQL, Drizzle ORM |
| **Auth** | Clerk |
| **Deployment** | Vercel |

---

## 📂 Project Structure

```
CreatorIQ/
│
├── app/                   # Next.js App Router pages & layouts
├── components/
│   └── ui/                # ShadCN UI components
├── configs/               # App configuration & env setup
├── hooks/                 # Custom React hooks
├── lib/                   # Utility functions & DB client
├── public/                # Static assets
├── drizzle.config.ts      # Drizzle ORM config
├── next.config.ts         # Next.js config
├── tailwind.config.ts     # Tailwind config
├── tsconfig.json          # TypeScript config
└── README.md
```

---

## 🔄 Project Pipeline

```
User signs in via Clerk
        ↓
Dashboard loads (Next.js App Router)
        ↓
     ┌──────────────────────────────────────────┐
     │ Thumbnail Gen  │  Channel Analytics       │
     │ AI Models      │  BrightData Scraping     │
     │ History Store  │  1K+ videos/day          │
     ├────────────────┼─────────────────────────-┤
     │ Content Ideas  │  Keyword Explorer        │
     │ LLM (OpenAI /  │  Trending queries        │
     │ Gemini API)    │  Competitor analysis     │
     └──────────────────────────────────────────┘
        ↓
Inngest handles 100+ concurrent background tasks
        ↓
Neon PostgreSQL ← Drizzle ORM → Next.js Server Actions
        ↓
Vercel Deployment
```

---

## ⚙️ Setup & Installation

**1. Clone the repository**
```bash
git clone https://github.com/DishaDewangan/CreatorIQ.git
cd CreatorIQ
```

**2. Install dependencies**
```bash
npm install
```

**3. Create environment file**
```bash
cp .env.example .env
```

Fill in the following values in your `.env`:
```env
CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
BRIGHTDATA_API_KEY=your_brightdata_api_key
INNGEST_API_KEY=your_inngest_api_key
OPENAI_API_KEY=your_openai_api_key
NEON_DB_URL=your_neon_database_url
```

**4. Start the development server**
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the app.

---

## 🗄️ Database Setup (Drizzle + Neon)

**Push schema to Neon:**
```bash
npx drizzle-kit push
```

**Generate migration files:**
```bash
npx drizzle-kit generate
```

---

## ✅ Key Implementations

| Feature | Status |
|---------|--------|
| AI thumbnail generation (95%+ accuracy) | ✅ |
| BrightData web scraping (1K+ videos/day) | ✅ |
| Inngest background jobs (100+ concurrent tasks) | ✅ |
| YouTube channel analytics & outlier detection | ✅ |
| AI content idea & script generation | ✅ |
| Trending keyword explorer | ✅ |
| Neon PostgreSQL + Drizzle ORM | ✅ |
| Clerk authentication & role-based workflows | ✅ |
| Usage-based billing & tiered plans | ✅ |
| Next.js 14 App Router + Server Actions | ✅ |
| TypeScript throughout | ✅ |
| Vercel deployment | ✅ |

---

## 👩‍💻 Author

**Disha Dewangan**  
[![GitHub](https://img.shields.io/badge/GitHub-DishaDewangan-black?style=flat&logo=github)](https://github.com/DishaDewangan)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Disha%20Dewangan-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/disha-dewangan-9a0071291/)
[![LeetCode](https://img.shields.io/badge/LeetCode-DishaDewangan-orange?style=flat&logo=leetcode)](https://leetcode.com/DishaDewangan/)

---

If this project helped you, consider giving it a ⭐!
