NorAiGroup Dashboard — Interactive Frontend Demo

A fully client-side, interactive demo of the NorAiGroup Dashboard.
Simulates Authentication, Project Management, AI tools, Collaboration, Versioning, Deployments and Analytics using only front-end code (React + Vite + Tailwind). Built to feel like a real SaaS product with rich animations, responsive layouts, and realistic mock workflows.

🚀 Features (what this demo ships)

Authentication

Demo credentials (client-side):
Email: demo@gmail.com
Password: demo1234

Form validation, error states and toast notifications.

Navigation & Layout

Responsive sidebar navigation (collapsible) with all requested sections:

Overview / Project Summary

Projects Workspace

AI Code Generator

Drag & Drop App Builder

Live Preview / Design

AI Chat Assistant

Progress Timeline

Collaboration Hub

Version Control / History

Deployment Center

Analytics & Insights

Billing & Plans

Settings & Profile

Active section highlight uses #950101 or #3D0000.

Design & Theme

Color palette:

Background: #000000

Primary: #3D0000

Secondary / Active: #950101

Accent / Alerts: #FF0000

Font: Tomorrow (README explains how to include / fallback)

Dark mode (default) + Light theme toggle

Animations & Interactions

Animated progress bars

Fade in/out for modals, cards & chat messages

Slide-in sidebar items

Typing animation for AI assistant responses

Timeline step highlight animations

Line-by-line code generation animation for AI code generator

Smooth drag & drop builder with snapping and live preview

Mock deployment logs with animated streaming output

Charts & graphs animate on load

Mock Functionality

Client-side user state (no DB). All edits are stored in memory (session).

CRUD across projects, tasks, team invites, versions, billing items.

Simulated AI responses & realistic code generation (timed streaming).

Simulated git commits and version history (client-side).

Mock deploy flow with progress, logs and success/failure states.

Responsive across XL / LG / MD / SM breakpoints.

📦 Tech Stack

React (Functional components + Hooks)

Vite (fast dev server)

Tailwind CSS (utility-first styling)

Framer Motion (animations)

react-beautiful-dnd or @dnd-kit (drag & drop)

recharts (charts & graphs)

Toaster: [react-hot-toast] or built-in Toastr-style component

Optional: Typescript (project can be TS or JS — README examples assume JS)

No server — everything simulated client-side

🧭 Quick start (development)

Assumes Node.js >= 16 and npm or pnpm installed.

# 1. Clone (or create new repo)
git clone https://github.com/<your-org>/norai-dashboard-demo.git
cd norai-dashboard-demo

# 2. Install dependencies
npm install

# 3. Start dev server
npm run dev

# 4. Open in browser
# Vite prints local URL (usually http://localhost:5173)


Scripts (example package.json scripts)

"scripts": {
  "dev": "vite",
  "build": "vite build",
  "preview": "vite preview",
  "lint": "eslint . --ext .js,.jsx,.ts,.tsx",
  "format": "prettier --write ."
}

🔧 Tailwind + Theme setup

tailwind.config.js (important colors)

module.exports = {
  content: ['./index.html', './src/**/*.{js,jsx,ts,tsx}'],
  theme: {
    extend: {
      colors: {
        background: '#000000',
        primary: '#3D0000',
        secondary: '#950101',
        accent: '#FF0000'
      },
      fontFamily: {
        sans: ['Tomorrow', 'Inter', 'ui-sans-serif', 'system-ui']
      }
    }
  },
  plugins: []
}


Include Tomorrow font

If you have a web license, include it in /public/fonts/Tomorrow.* with @font-face in src/index.css:

@font-face {
  font-family: 'Tomorrow';
  src: url('/fonts/Tomorrow.woff2') format('woff2');
  font-weight: 300 700;
  font-style: normal;
  font-display: swap;
}
:root { --main-font: 'Tomorrow', Inter, system-ui, -apple-system, 'Segoe UI'; }
body { font-family: var(--main-font); background: #000000; }


Otherwise use a close fallback (Inter) until you include Tomorrow.

🧩 Folder structure (recommended)
/src
 ├─ /assets
 ├─ /components
 │   ├─ Sidebar.jsx
 │   ├─ Topbar.jsx
 │   ├─ Auth/LoginForm.jsx
 │   ├─ Projects/ProjectCard.jsx
 │   ├─ AI/CodeGenerator.jsx
 │   ├─ Builder/DragNDropBuilder.jsx
 │   ├─ Chat/AIAssistant.jsx
 │   ├─ Charts/AnimatedChart.jsx
 │   └─ ... (modals, toasts, forms)
 ├─ /contexts
 │   ├─ AuthContext.jsx
 │   ├─ ProjectsContext.jsx
 │   └─ UIContext.jsx
 ├─ /pages
 │   ├─ Overview.jsx
 │   ├─ Projects.jsx
 │   ├─ AI.jsx
 │   ├─ Builder.jsx
 │   └─ Settings.jsx
 ├─ /utils
 │   ├─ mockAI.js
 │   ├─ mockDeploy.js
 │   └─ helpers.js
 ├─ main.jsx
 └─ index.css

🔐 Authentication & Demo Flow

Demo Credentials (client-only):

Email: demo@gmail.com

Password: demo1234

AuthContext stores isAuthenticated and user object in memory (React state).

Login form validates email format + minimum password length; shows toast on success/failure.

After login, the app seeds demo projects and data into ProjectsContext.

Security note: This demo stores everything in client memory for UX purposes — do not use this for production auth.

✨ Animations & UX details (how they are implemented)

Progress bars: use CSS transitions + Framer Motion for easing. On mount, bar width animates from 0% → value%.

Modals & cards: fade and scale with Framer Motion AnimatePresence.

Sidebar items: slide in with staggered animation (staggerChildren) — active item highlighted in #950101.

AI typing: simulated with setInterval or Framer Motion typewriter that appends characters; show skeleton dots while generating.

Line-by-line code generation: iterate over code lines and append with short delays; highlight each line as it appears.

Drag & drop: use react-beautiful-dnd or @dnd-kit for natural dragging; add snap-to-grid logic in builder.

Deployment logs: stream log lines from mockDeploy.js with variable delays; include success/failure animation and toast.

Charts: recharts with initial values 0 then animate to target values on component mount.

🧪 Mock data & behavior

mockAI.js contains deterministic pseudo-responses and streaming logic so results feel consistent.

mockDeploy.js simulates deployment stages: Build → Test → Upload → Deploy with logs and progress percent.

Version control is simulated as an array of commits per project. Commit / rollback UI performs client-side state changes to mimic checkouts.

Collaboration Hub shows team members, invites, and real-time-like notifications (via in-memory timers).

📱 Responsive & Accessibility

Breakpoints: sm, md, lg, xl — layout shifts from collapsed sidebar (mobile) to permanent sidebar (desktop).

Interactive elements use role, aria-* attributes, focus states and keyboard navigation for accessibility.

High-contrast color palette (background black, deep reds) — ensure text contrast meets WCAG where possible.
