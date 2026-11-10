# Task Management System (TaskFlow Pro)

[![React](https://img.shields.io/badge/React-18.3-61DAFB?logo=react&logoColor=black)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Vite-5.4-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Recharts](https://img.shields.io/badge/Recharts-2.13-22c55e?logo=d3.js&logoColor=white)](https://recharts.org/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> A modern, responsive, commercial-grade **Task Management System** designed for high-performance productivity tracking, college project demonstrations, GitHub portfolios, and resume showcases. Inspired by modern SaaS productivity tools with full offline LocalStorage synchronization.

---

## 🌟 Key Features

### 1. 📊 Executive Dashboard & Analytics
- **Dynamic KPI Cards:** Live dynamic calculation of Total, Pending, Completed, Overdue, and Starred tasks.
- **Productivity Score Ring:** Real-time percentage completion calculation with animated progress indication.
- **Weekly Activity Chart:** Interactive area chart measuring daily tasks created versus completed using **Recharts**.
- **Priority & Status Distribution:** Breakdown of tasks across Urgent, High, Medium, and Low tiers.
- **Category Focus:** Visualized distribution across College, Projects, Work, Personal, and Meetings.

### 2. 🗂 Complete Task CRUD & Multiple View Modes
- **Full CRUD:** Create, read, update, delete, complete, and star tasks.
- **Multi-View Switcher:**
  - **Grid Card View:** Clean cards with priority badges, checklist progress bars, and tag chips.
  - **Interactive Kanban Board:** Drag-and-drop workflow status columns (`Pending`, `In Progress`, `Completed`).
  - **Data Table View:** Sortable tabular interface with checkboxes for bulk actions.
- **Subtask Checklists:** Track granular sub-items per task with real-time progress percentages.
- **Overdue Detection:** Visual indicators and notifications for tasks past their deadlines.

### 3. 📅 Interactive Monthly Calendar
- Full calendar matrix showing tasks mapped to their specific due dates.
- Previous / Next month navigation and one-click "Today" reset.
- Date agenda panel to view and add tasks directly for any selected day.

### 4. ⚡ Quick Creation & Keyboard Speed
- **Quick Add Bar:** Instant one-line task creation without opening full modals.
- **Keyboard Shortcuts:**
  - `N`: Create new task
  - `D`: Jump to Dashboard
  - `A`: Jump to All Tasks
  - `T`: Jump to Today's Tasks
  - `C`: Open Calendar
  - `S`: Open Settings
  - `/`: Focus search input
  - `?`: Open Keyboard Shortcuts cheat sheet
  - `Esc`: Close any active modal

### 5. 🔔 Notifications & Auditory Feedback
- **Dynamic Notification Center:** Automated alerts for overdue tasks, tasks due today, and milestone achievements.
- **Audio Synthesis:** Zero-dependency pleasant chimes via Web Audio API when tasks are marked complete.
- **Confetti Celebration:** Confetti particle bursts upon finishing milestones.

### 6. 💾 Backup, Export & Portability
- **JSON Backup:** Full workspace snapshot export and validation import.
- **CSV Spreadsheet Export:** Export tasks to `.csv` format ready for Excel or Google Sheets.
- **Demonstration Reset:** One-click restoration of realistic sample data (Java assignments, exam preparation, projects).

---

## 🛠 Tech Stack

| Domain | Technology |
|---|---|
| **Framework** | [React 18](https://react.dev/) |
| **Bundler & Tooling** | [Vite 5](https://vitejs.dev/) |
| **Styling** | [Tailwind CSS 3](https://tailwindcss.com/) |
| **Icons** | [Lucide React](https://lucide.dev/) |
| **Data Visualization** | [Recharts 2](https://recharts.org/) |
| **Celebration Effects** | [Canvas-Confetti](https://www.npmjs.com/package/canvas-confetti) |
| **Data Persistence** | Browser LocalStorage (Synchronous & Offline-First) |
| **CI/CD Deployment** | GitHub Actions & GitHub Pages |

---

## 📁 Project Structure

```
task-management-system/
├── .github/
│   └── workflows/
│       └── deploy.yml          # Automated GitHub Pages CI/CD workflow
├── public/                     # Static assets & icons
├── src/
│   ├── components/
│   │   ├── calendar/
│   │   │   └── CalendarView.jsx       # Interactive calendar grid & agenda
│   │   ├── common/
│   │   │   ├── Badge.jsx              # Priority & status color badges
│   │   │   ├── ConfirmModal.jsx       # Danger confirmation dialogs
│   │   │   ├── EmptyState.jsx         # Friendly empty state placeholders
│   │   │   ├── ShortcutsModal.jsx     # Keyboard shortcuts cheat sheet
│   │   │   └── ToastContainer.jsx     # Toast notifications
│   │   ├── layout/
│   │   │   ├── Header.jsx             # Top bar: search, theme, notifications, avatar
│   │   │   └── Sidebar.jsx            # 10-view collapsible navigation sidebar
│   │   ├── notifications/
│   │   │   └── NotificationDropdown.jsx # Dynamic overdue & upcoming alerts
│   │   └── tasks/
│   │       ├── KanbanBoard.jsx        # Drag-and-drop 3-column status board
│   │       ├── QuickAddBar.jsx        # Fast single-line task input
│   │       ├── TaskCard.jsx           # Grid item card with subtask progress
│   │       ├── TaskFilters.jsx        # Status tabs, search, dropdowns, bulk actions
│   │       ├── TaskModal.jsx          # Create/Edit modal with subtasks & tags
│   │       └── TaskTable.jsx          # Sortable table view with bulk select
│   ├── context/
│   │   └── TaskContext.jsx            # Centralized state provider & LocalStorage sync
│   ├── pages/
│   │   ├── AnalyticsPage.jsx          # Velocity, priority & category charts
│   │   ├── CalendarPage.jsx           # Dedicated calendar view page
│   │   ├── DashboardPage.jsx          # Executive KPI cards & recent focus
│   │   ├── HelpPage.jsx               # Interactive FAQ, diagnostics & guide
│   │   ├── SettingsPage.jsx           # Preferences, profile, import/export
│   │   └── TasksPage.jsx              # Unified tasks page (All, Today, etc.)
│   ├── utils/
│   │   ├── dateUtils.js               # Date formatting, overdue check, calendar matrix
│   │   ├── exportUtils.js             # JSON backup & CSV spreadsheet generators
│   │   ├── sampleData.js              # Realistic initial task datasets
│   │   └── soundEffects.js            # Synthesizer web audio controller
│   ├── App.jsx                        # Layout router & shell
│   ├── index.css                      # Tailwind base & custom scrollbar
│   └── main.jsx                       # Application bootstrap
├── index.html
├── package.json
├── tailwind.config.js
└── vite.config.js
```

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v18.0 or higher)
- [npm](https://www.npmjs.com/) or [pnpm](https://pnpm.io/)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/harikrishna-web/Task-Management-System.git
   cd Task-Management-System
   ```

2. **Install project dependencies:**
   ```bash
   npm install
   ```

3. **Start the local development server:**
   ```bash
   npm run dev
   ```

4. **Open in browser:**
   Open [http://localhost:5173](http://localhost:5173) to view the application live.

5. **Build for production:**
   ```bash
   npm run build
   ```

---

## 🌐 Deploying to GitHub Pages

### Method 1: Automated Deployment via GitHub Actions (Recommended)

1. Push your repository to GitHub:
   ```bash
   git init
   git add .
   git commit -m "feat: complete modern task management system"
   git branch -M main
   git remote add origin https://github.com/<your-username>/Task-Management-System.git
   git push -u origin main
   ```
2. Navigate to your repository on GitHub:
   - Go to **Settings** > **Pages**.
   - Under **Build and deployment** > **Source**, choose **GitHub Actions**.
3. Every push to the `main` branch will automatically build and publish your site!

### Method 2: Manual Deploy via `gh-pages`

1. Install `gh-pages` helper package:
   ```bash
   npm install --save-dev gh-pages
   ```
2. In `package.json`, add deploy scripts:
   ```json
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```
3. Run:
   ```bash
   npm run deploy
   ```

---

## 🎓 College Demonstration & Portfolio Showcase

This project demonstrates software engineering principles:
- **Clean Architecture:** Separation of Concerns via React Context API, custom hooks, and utility layers.
- **Defensive Design:** Safe LocalStorage fallbacks, JSON schema verification, and confirmation gates on destructive actions.
- **Accessibility & UX:** Full light and dark mode compliance, custom focus rings, responsive mobile navigation drawers, and keyboard shortcuts.
- **Zero Third-Party Audio Bloat:** Web Audio API oscillator synthesis avoids missing external media files.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
