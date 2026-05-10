# Healing Hub

A mental wellness web application designed to support emotional well-being through mood tracking, journaling, cycle awareness, mindfulness exercises, and a gentle AI companion.

---

## Features

- **Dashboard** — At-a-glance view of mood streaks, journal count, sleep average, and 30-day mood trend
- **Soul Scribbles (Journal)** — Private journaling with CBT-based prompts and mood tagging
- **Luna Tracker** — Menstrual cycle tracking with phase predictions and daily symptom logging
- **Mindfulness** — Guided breathing exercises (Box, 4-7-8, Belly, Coherent) and yoga postures
- **Tune In** — Curated music for different emotional states
- **Brain Teasers** — Light cognitive games to shift focus
- **Gratitude Garden** — Daily gratitude logging
- **Sage (AI Companion)** — A gentle chat-based companion powered by a Supabase edge function
- **Insights** — Weekly mood trend charts and recent mood history
- **Therapist Finder** — Signposting to real professional support

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 18 + Vite |
| Language | TypeScript |
| Styling | Tailwind CSS + shadcn/ui |
| Auth & DB | Supabase |
| Animation | Framer Motion |
| Charts | Chart.js via react-chartjs-2 |

---

## Getting Started

**Prerequisites:** Node.js 18+ and npm

```sh
# Install dependencies
npm install

# Start the dev server
npm run dev
```

The app runs at `http://localhost:5173` by default.

### Environment variables

Create a `.env` file at the project root (copy from `.env.example` if present):

```
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

---

## Project Structure

```
src/
├── components/       # Shared UI components (Navbar, Footer, Chatbot, etc.)
├── hooks/            # Custom React hooks (useAuth)
├── integrations/     # Supabase client setup
├── lib/              # Business logic (wellness-logic.ts, user-profile.ts)
├── pages/            # Route-level page components
└── index.css         # Global styles and design tokens
```

---

## Local Data & Privacy

Most user data (mood logs, journal entries, cycle entries, sleep data) is stored in `localStorage` and never leaves the device. Only authentication and the AI companion require a network connection.

---

## Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint |
