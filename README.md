# 🌐 HealthSphere AI

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Vite](https://img.shields.io/badge/Vite-6.x-646CFF.svg?style=flat&logo=vite)](https://vitejs.dev/)
[![React](https://img.shields.io/badge/React-19.x-61DAFB.svg?style=flat&logo=react)](https://react.dev/)
[![Express](https://img.shields.io/badge/Express-4.x-000000.svg?style=flat&logo=express)](https://expressjs.com/)
[![Gemini](https://img.shields.io/badge/Gemini_API-2.5--flash-f1c40f.svg?style=flat&logo=google)](https://ai.google.dev/)

**HealthSphere AI** is a professional, modern public health awareness and digital guidance platform. It combines a state-of-the-art React frontend with a secure, rate-limited Express gateway connecting directly to Google's **Gemini 2.5 Flash** model. 

The application is engineered to assist communities in making informative, evidence-based wellness decisions (covering topics like diseases, vaccination schedules, nutritional guidance, and hygiene) while strictly adhering to safety guardrails.

---

## 🎯 Key Features

- **🧠 Guardrailed AI Public Health Agent**: Powered by `gemini-2.5-flash` through system instructions that reject unrelated topics (e.g. politics, coding, gossip) and gracefully request user redirection to health topics.
- **📄 Downloadable Health Reports**: One-click PDF generation utilizing `jsPDF` to save symptom checklists, nutrition advice, or guidance summaries locally.
- **📊 Health Trends & Metrics Dashboard**: Interactive disease tracking and statistical visualization powered by `Recharts`.
- **🔐 Firebase Integration**: User session handling and persistent cloud-synced Chat History database queries.
- **🎨 Glassmorphic Dark-Mode UI**: Implemented via Vanilla CSS & Tailwind v4 paired with smooth layout micro-animations (`motion` / `lucide-react`).

---

## 🛠️ Tech Stack

### Frontend Hub
- **UI Framework:** React 19 (TypeScript)
- **Tooling & Bundler:** Vite 6
- **Styling & Icons:** CSS, TailwindCSS v4, Lucide React
- **Animations:** Motion
- **Chart Visuals:** Recharts
- **PDF Core:** jsPDF

### Backend Proxy Gateway
- **Runtime:** Node.js
- **Server Framework:** Express
- **API Client:** Official Google GenAI SDK (`@google/genai`)
- **Compilation Tool:** esbuild (Bundles TS files to light Node CommonJS output)
- **Dev Runner:** `tsx` (TypeScript Execute)

### Services & Data
- **Database / Auth:** Firebase Firestore (saves users, current messages, & sessions)

---

## 📂 Project Structure

```bash
├── src/
│   ├── components/      # Modular UI components (AIChatbot, Dashboard, etc.)
│   ├── lib/             # Firebase configuration interface 
│   ├── App.tsx          # Main layout application router and workspace
│   ├── main.tsx         # React application DOM entrypoint
│   └── index.css        # Core global styles and theme variables
├── server.ts            # Node/Express backend that proxies Gemini requests safely
├── package.json         # Build commands, scripts, and production dependencies
├── vite.config.ts       # Frontend configuration & proxy rules
└── tsconfig.json        # Strict TypeScript compiler instructions
```

---

