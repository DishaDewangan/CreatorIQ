# 📘 **CreatorIQ – AI-Powered YouTube Analytics & Content Intelligence Platform**

CreatorIQ is a full-stack AI SaaS platform that helps YouTubers, creators, and marketers analyze channels, generate video ideas, create AI thumbnails, track keyword trends, and gain deep insights — all powered by **Next.js, TypeScript, Inngest, BrightData, Neon DB, Clerk Auth, and OpenAI**.

This project is built following *TubeGuruji's "Build & Deploy AI Full Stack App"* tutorial with enhancements and modular architecture.

---

## 🚀 **Features**

### 🎨 **AI Thumbnail Generator**

* Generates high-quality YouTube thumbnails using AI
* Stores & displays thumbnail history
* Thumbnail search functionality
* Fully optimized for YouTube aspect ratio

### 📊 **YouTube Channel Analytics**

* Fetch video metadata using BrightData
* Analyze outlier videos
* Engagement & performance insights
* Detect high-performing patterns & trends

### 💡 **AI Content Generator**

* AI-powered script ideas
* Title + description suggestions
* Topic breakdown with SEO scoring

### 🔎 **Trending Keyword Explorer**

* Fetch trending search queries
* Niche keyword suggestions
* Difficulty scoring
* Competitor comparison

### 🧾 **Billing / Pricing**

* Usage-based billing
* Tiered subscription plans
* Limits integrated with Clerk

### 🔒 **Authentication**

* Secure login via **Clerk**
* Role-based workflows
* Session management

---

## 🏗️ **Tech Stack**

### **Frontend**

* **Next.js 14 (App Router)**
* **React 18**
* **TypeScript**
* **Tailwind CSS**
* **ShadCN UI**

### **Backend**

* **Next.js Server Actions**
* **Inngest** (background jobs, workflows)
* **BrightData API** (YouTube data)
* **OpenAI / Gemini** (LLM content generation)
* **Neon PostgreSQL**
* **Drizzle ORM**

### **Infrastructure**

* **Vercel Deployment**
* **Neon for Database**
* **Inngest for event-driven tasks**
* **BrightData for scraping APIs**

---

## 📂 **Project Structure**

```
CreatorIQ/
│── app/
│── components/
│── configs/
│── hooks/
│── lib/
│── public/
│── drizzle.config.ts
│── next.config.ts
│── postcss.config.mjs
│── tailwind.config.ts
│── tsconfig.json
└── README.md
```

---

## ⚙️ **Setup Instructions**

### 1️⃣ Clone the Repo

```bash
git clone https://github.com/DishaDewangan/CreatorIQ.git
cd CreatorIQ
```

### 2️⃣ Install Dependencies

```bash
npm install
```

### 3️⃣ Create Environment File

```bash
cp .env.example .env
```

Fill in values for:

* `CLERK_PUBLISHABLE_KEY`
* `CLERK_SECRET_KEY`
* `BRIGHTDATA_API_KEY`
* `INNGEST_API_KEY`
* `OPENAI_API_KEY`
* `NEON_DB_URL`

### 4️⃣ Start the Dev Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the app.

---

## 🔧 **Running Database (Drizzle + Neon)**

Push schema:

```bash
npx drizzle-kit push
```

Generate migration:

```bash
npx drizzle-kit generate
```


---

## 📚 **Resources**

* **BrightData**: [https://dcmk.short.gy/brightdata](https://dcmk.short.gy/brightdata)
* **Inngest**: [https://innge.st/yt-tg5](https://innge.st/yt-tg5)
* **Neon**: [https://fyi.neon.tech/tg9](https://fyi.neon.tech/tg9)
* **Clerk**: [https://go.clerk.com/zIDA7q9](https://go.clerk.com/zIDA7q9)
* **Source Tutorial**: TubeGuruji


---

## 📜 **License**

MIT License.

---

**Built with ❤️ by [Disha Dewangan](https://github.com/DishaDewangan)**
