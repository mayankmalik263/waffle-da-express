# 🧇 Waffle Da! Express

<p align="center">
  <img src="src/assets/waffle-da-logo.png" alt="Waffle Da Logo" width="160" />
</p>

<p align="center">
  <strong>Delicious handcrafted waffles, fluffy pancakes & creamy shakes — made fresh, served with love.</strong>
</p>

<p align="center">
  <a href="https://vite.dev/"><img src="https://img.shields.io/badge/Vite-6495ED?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" /></a>
  <a href="https://react.dev/"><img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" /></a>
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" /></a>
  <a href="https://tailwindcss.com/"><img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" /></a>
  <a href="https://supabase.com/"><img src="https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase" /></a>
  <a href="https://capacitorjs.com/"><img src="https://img.shields.io/badge/Capacitor-119EFF?style=for-the-badge&logo=capacitor&logoColor=white" alt="Capacitor" /></a>
</p>

---

## ✨ Overview

**Waffle Da!** is a premium, lightning-fast food ordering web application and companion mobile app designed specifically for ordering freshly made waffles, custom treats, and delicious quick bites. Initially conceptualized and powered by **vibe coding** on [lovable.dev](https://lovable.dev), this project offers a highly responsive customer-facing shop front coupled with a robust real-time administration panel. 

Perfect for campus hubs (like Bidholi, Dehradun), pop-up stalls, and late-night cravings (operating 5 PM to 5 AM!), Waffle Da! bridges premium visual aesthetics with robust full-stack state management.

---

## 🚀 Key Features

### 🛍️ Customer Experience
- **Interactive Multi-Category Menu:** Seamlessly browse through categories like *Waffles, Waffle Cakes, Spiral Potatoes, Hot Chocolate, French Fries, Veg/Chicken Burgers, Pastas, Shakes, Teas & Coffees*.
- **Gourmet Customization Pop-up:** Tailor waffle creations with premium add-ons (such as Oreo, Kitkat, Nutella, Ice cream, Sprinklers, Extra Chocolate) with dynamic pricing calculation.
- **Dynamic State Cart:** Persistent, real-time shopping cart context supporting instant volume adjustments and clear total calculations.
- **Seamless Order Checkout:** Quick checkout form collecting user details, phone number, delivery address, and preferences.
- **Live Order Progress Tracker:** Real-time step-by-step visual feedback of order processing from "Placed" to "Kitchen" to "Out for Delivery" to "Completed".
- **Dynamic Pop-Up Stall Interface:** Special dedicated stall scheduling banner and specialized `/stall-menu` layout for seasonal/event pop-ups.

### 🛡️ Real-Time Admin Dashboard (`/admin`)
- **Shop Status Manager:** Switch the primary shop state (Open/Closed) instantly with banners reflecting client-side immediately.
- **Live Order Monitoring Desk:** Dynamic live queue listing placed orders, update progress, cancel or complete them.
- **Stall Schedule Configurator:** Select custom dates, titles, and descriptions to deploy interactive event banners across the app.
- **Product Inventory Control:** Quickly toggle menu item availability so out-of-stock options are automatically hidden or disabled.
- **Analytical Insights Dashboard:** Interactive charts showing sales, revenue, and product distributions powered by Recharts.

---

## 🛠️ Technology Stack

- **Framework & Bundler:** Vite + React 18 (SPA with Client-Side Routing)
- **Language:** TypeScript
- **State Management & Async Queries:** React Query (TanStack Query) + React Context API
- **Styling & Theme:** Tailwind CSS + custom glassmorphism, warm waffle-themed color gradients, and fully responsive layout + built-in dark/light mode toggle.
- **Animations:** Framer Motion for smooth component entrance animations and page transitions.
- **Backend Integrations:** Supabase (for persistent database interactions, user-management, and real-time operations).
- **Icons:** Lucide React
- **Mobile Integration:** `@capacitor/android` configuration supporting deployment as a native mobile Android package.

---

## 📁 Project Structure

```
Waffle Da Website/
├── supabase/               # Supabase migrations, configurations & schema definition
├── public/                 # Static assets, icons, and configuration metadata
├── src/
│   ├── assets/             # Images, backgrounds, and brand logo
│   ├── components/         # Reusable UI widgets (CustomizePopup, Navbar, ThemeToggle)
│   │   └── ui/             # Radix primitives styled via shadcn/ui
│   ├── context/            # React Context providers (Cart, Orders, Menu, ShopStatus)
│   ├── data/               # Static dataset fallbacks (menuData.ts catalog)
│   ├── hooks/              # Custom reactive hooks
│   ├── integrations/       # Supabase client hooks and database schemas
│   ├── pages/              # Main routing pages (Index, Cart, Checkout, Admin, Menu)
│   ├── App.tsx             # Routing matrix & application wrapper
│   ├── index.css           # Global Tailwind directives & theme configuration
│   └── main.tsx            # Main DOM entrypoint
├── capacitor.config.ts     # Mobile compilation rules
├── package.json            # Node project configuration
└── vite.config.ts          # Vite build pipeline
```

---

## ⚙️ Getting Started

Follow these instructions to run Waffle Da! locally on your system:

### Prerequisites

Ensure you have **Node.js (v18+)** and **npm** or **Bun** installed.

### Setup Steps

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/mayankmalik263/waffle-da-express.git
   cd waffle-da-express
   ```

2. **Install Dependencies:**
   Using npm:
   ```bash
   npm install
   ```
   Or using Bun:
   ```bash
   bun install
   ```

3. **Configure Environment Variables:**
   Create a `.env` file in the root directory and configure your Supabase keys:
   ```env
   VITE_SUPABASE_URL=your_supabase_project_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **Fire Up the Development Server:**
   Using npm:
   ```bash
   npm run dev
   ```
   Using Bun:
   ```bash
   bun run dev
   ```
   Open `http://localhost:5173` to view the application in your browser!

---

## 📱 Mobile Build (Capacitor)

This app supports packaging as a native Android application using Capacitor:

```bash
# 1. Build the production web bundle
npm run build

# 2. Sync web assets into the Android native project
npx cap sync

# 3. Open the native project in Android Studio
npx cap open android
```

---

## 🧠 Vibe Coding Credits

This project was fully **vibe coded** with absolute speed and elegance using [Lovable.dev](https://lovable.dev) — the next-generation AI full-stack developer that turns natural language prompts into stunning React applications. 

With Lovable.dev handling the heavy lifting of state integration, CSS layouting, and interactive custom workflows, we crafted a high-quality product in record time without getting bogged down in boilerplate code.

---

## ⚖️ Legal Disclaimer & Proprietary Rights

### 🚨 Strict Warning against Clones and Plagiarism

**Copyright © 2026 - Present, Mayank Malik & Pratik Sinha. All Rights Reserved.**

This project is **strictly proprietary and confidential**. The entire codebase, custom user interface design, visual asset configurations, responsive layout workflows, tailored state management architectures, and administrative dashboard structures are the exclusive intellectual property of **Mayank Malik** and **Pratik Sinha**.

Any unauthorized attempts to:
- ❌ **Copy, duplicate, or clone** this website or any of its sub-modules.
- ❌ **Redistribute, sublicense, or sell** the code (in whole or in part) under any name.
- ❌ **Reverse engineer, scrape, or extract** proprietary state context configurations, database architectures, or business patterns.
- ❌ **Hinder, disrupt, or interfere** with the active hosting, deployment, or active development progress of this application.

**WILL BE MET WITH IMMEDIATE LEGAL AND ADMINISTRATIVE ACTIONS.**

We actively monitor web deployments for identical CSS footprint patterns, UI templates, and component architectures. Any detected plagiarism or copyright infringement will result in:
1. Immediate **DMCA Takedown Requests** filed with GitHub, Vercel, Netlify, and other web host providers.
2. Formal **Plagiarism Reports** submitted directly to academic/professional institutions and corporate recruiters.
3. Legal **Cease-and-Desist Notices** served to the infringing parties.

*For Recruiters/Hiring Managers: You are granted temporary permission to read, explore, and review the codebase for candidate evaluation purposes only. All other rights are strictly reserved.*
