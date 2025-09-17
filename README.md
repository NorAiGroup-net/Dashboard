NorAiGroup Dashboard — Interactive Frontend Demo

A fully client-side, interactive demo of the NorAiGroup Dashboard.
Simulates Authentication, Project Management, AI tools, Collaboration, Versioning, Deployments and Analytics using only front-end code (React + Vite + Tailwind). Built to feel like a real SaaS product with rich animations, responsive layouts, and realistic mock workflows.

Features (what this demo ships)

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
