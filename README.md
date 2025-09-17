# NorAiGroup Dashboard

> A fully client-side, interactive demo of the **NorAiGroup Dashboard**.  
> Simulates Authentication, Project Management, AI tools, Collaboration, Versioning, Deployments and Analytics using only front-end code (React + Vite + Tailwind).  
> Built to *feel* like a real SaaS platform with rich animations, responsive layouts, and realistic mock workflows.

---

##  Features

- **Authentication**
  - Demo login:  
    `Email: demo@gmail.com`  
    `Password: demo1234`
  - Form validation + toast notifications.

- **Navigation & Layout**
  - Responsive sidebar with all core sections:
    - Overview / Project Summary  
    - Projects Workspace  
    - AI Code Generator  
    - Drag & Drop App Builder  
    - Live Preview / Design  
    - AI Chat Assistant  
    - Progress Timeline  
    - Collaboration Hub  
    - Version Control / History  
    - Deployment Center  
    - Analytics & Insights  
    - Billing & Plans  
    - Settings & Profile  

- **Design & Theme**
  - Colors:  
    - Background `#000000`  
    - Primary `#3D0000`  
    - Secondary `#950101`  
    - Accent `#FF0000`  
  - Font: **Tomorrow**
  - Dark & Light theme toggle

- **Animations & Interactions**
  - Animated progress bars  
  - Fade in/out modals & chat messages  
  - Sidebar slide-in animations  
  - Typing animation for AI assistant  
  - Timeline highlights  
  - Line-by-line AI code generation  
  - Smooth drag & drop builder  
  - Animated deployment logs  
  - Animated charts & graphs  

- **Mock Functionality**
  - All state stored client-side (no DB)  
  - CRUD support for projects, tasks, commits, billing items  
  - Simulated AI responses & code generation  
  - Simulated version control & deployments  
  - Mobile-first responsive design  

---

##  Tech Stack

- [React](https://react.dev/) + [Vite](https://vitejs.dev/)  
- [Tailwind CSS](https://tailwindcss.com/)  
- [Framer Motion](https://www.framer.com/motion/)  
- [React Hot Toast](https://react-hot-toast.com/)  
- [Recharts](https://recharts.org/)  
- [React Beautiful DnD](https://github.com/atlassian/react-beautiful-dnd) or [dnd-kit](https://dndkit.com/)  

---

##  Getting Started

### Prerequisites
- Node.js 16+  
- npm / pnpm / yarn  

### Setup
```bash
# Clone repo
git clone https://github.com/<your-org>/norai-dashboard-demo.git
cd norai-dashboard-demo

# Install deps
npm install

# Start dev server
npm run dev

# Open in browser (default http://localhost:5173)
