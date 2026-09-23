🎓 DPS Learning Hub

«An interactive digital learning platform for building essential computer skills through hands-on practice.»

DPS Learning Hub is a modern, responsive educational web application that brings together three interactive learning environments — Typing Lab, Document Mastery, and Excel Lab — under one cohesive dashboard.

The platform is designed around short, practical lessons with instant feedback, progress tracking, and simulated real-world tasks.

---

✨ Features

⌨️ Typing Lab

A minimalist, Monkeytype-inspired typing environment designed to improve typing speed and accuracy.

- Real-time WPM tracking
- Accuracy calculation
- Live typing feedback
- Mistake tracking
- Progress/results screen
- Responsive typing interface
- Clean distraction-free experience

---

📄 Document Mastery

An interactive 8-lesson tutorial for learning essential document formatting skills.

Lessons cover:

1. Page Setup
2. Margins & Orientation
3. Fonts & Text Formatting
4. Paragraph Formatting
5. Alignment & Spacing
6. Tables
7. Headers & Footers
8. Print Preparation

Each lesson uses interactive tasks and provides immediate feedback when the learner completes an activity.

---

📊 Excel Lab

An interactive 8-lesson spreadsheet simulator designed to teach fundamental spreadsheet concepts.

Lessons cover:

1. Spreadsheet & Cell Basics
2. Rows, Columns & Cell References
3. Data Entry & Formatting
4. Basic Formulas
5. Functions
6. Relative & Absolute References
7. Data Organization
8. Charts & Visualization

The simulator allows students to experiment with spreadsheet concepts without needing a separate spreadsheet application.

---

🎨 Design System

The interface follows a DPS-inspired modern EdTech aesthetic.

Element| Value
Primary Navy| "#002147"
Bright Blue| "#007AFF"
Background| White
Style| Premium / Minimalist
Layout| Dashboard-based
Design Goal| Clean, modern & educational

The UI emphasizes:

- Clear visual hierarchy
- Spacious layouts
- Rounded interactive components
- Smooth transitions
- Clear success/error states
- Responsive design
- Consistent navigation

---

🧭 Application Structure

The application consists of a central dashboard with three learning modules:

                    DPS Learning Hub
                           │
              ┌────────────┼────────────┐
              │            │            │
         Typing Lab   Document Mastery  Excel Lab
              │            │            │
          Practice       Lessons       Lessons
              │            │            │
              └────────────┼────────────┘
                           │
                    Progress Tracking

---

🗺️ Navigation

The application uses client-side routing logic to provide a multi-page experience without requiring traditional server-side page navigation.

Example routes:

/
├── /typing
├── /documents
│   ├── /documents/lesson-1
│   ├── /documents/lesson-2
│   └── ...
│
└── /excel
    ├── /excel/lesson-1
    ├── /excel/lesson-2
    └── ...

---

💾 Progress Tracking

Learning progress is stored locally using LocalStorage.

The application can track information such as:

{
  typing: {
    bestWPM: 72,
    bestAccuracy: 97
  },

  documents: {
    completedLessons: [1, 2, 3]
  },

  excel: {
    completedLessons: [1, 2]
  }
}

This allows students to continue their learning journey without requiring an account or backend database.

---

🧩 Feedback System

Interactive activities provide immediate feedback.

✅ Success

Used when the learner completes an activity correctly.

Examples:

- Correct answer
- Correct formatting
- Correct formula
- Completed lesson

❌ Error

Used when an action is incorrect.

Examples:

- Incorrect answer
- Invalid formula
- Wrong formatting
- Incorrect cell reference

Feedback should be clear and constructive rather than simply indicating that something went wrong.

---

📱 Responsive Design

DPS Learning Hub is designed to work across:

- 🖥️ Desktop
- 💻 Laptop
- 📱 Mobile
- 📟 Tablet

The interface adapts navigation, cards, learning activities, and simulators according to screen size.

---

📁 Project Structure

dps-learning-hub/
│
├── 📄 index.html
├── 📄 README.md
├── 📄 package.json
├── 📄 .gitignore
│
├── 📁 public/
│   ├── 📁 images/
│   └── 📁 icons/
│
└── 📁 src/
    │
    ├── 📁 assets/
    │   ├── 📁 images/
    │   └── 📁 icons/
    │
    ├── 📁 components/
    │   ├── 📁 Navbar/
    │   ├── 📁 Sidebar/
    │   ├── 📁 ProgressCard/
    │   ├── 📁 LessonCard/
    │   └── 📁 Feedback/
    │
    ├── 📁 pages/
    │   ├── 📁 Dashboard/
    │   ├── 📁 TypingLab/
    │   ├── 📁 DocumentMastery/
    │   └── 📁 ExcelLab/
    │
    ├── 📁 lessons/
    │   ├── 📁 documents/
    │   │   ├── lesson-01/
    │   │   ├── lesson-02/
    │   │   ├── lesson-03/
    │   │   ├── lesson-04/
    │   │   ├── lesson-05/
    │   │   ├── lesson-06/
    │   │   ├── lesson-07/
    │   │   └── lesson-08/
    │   │
    │   └── 📁 excel/
    │       ├── lesson-01/
    │       ├── lesson-02/
    │       ├── lesson-03/
    │       ├── lesson-04/
    │       ├── lesson-05/
    │       ├── lesson-06/
    │       ├── lesson-07/
    │       └── lesson-08/
    │
    ├── 📁 styles/
    │   ├── global.css
    │   ├── dashboard.css
    │   ├── typing.css
    │   ├── documents.css
    │   └── excel.css
    │
    ├── 📄 app.js
    ├── 📄 router.js
    └── 📄 storage.js

📌 Directory Overview

Directory / File| Purpose
"public/"| Static files served directly by the application
"src/assets/"| Images, icons, and other application assets
"src/components/"| Reusable UI components
"src/pages/"| Main application pages/modules
"src/pages/Dashboard/"| Main DPS Learning Hub dashboard
"src/pages/TypingLab/"| Typing practice environment
"src/pages/DocumentMastery/"| Interactive document-formatting lessons
"src/pages/ExcelLab/"| Interactive spreadsheet lessons
"src/lessons/documents/"| 8 Document Mastery lessons
"src/lessons/excel/"| 8 Excel Lab lessons
"src/styles/"| Global and module-specific styling
"router.js"| Client-side page navigation/routing
"storage.js"| LocalStorage-based progress management
"app.js"| Application initialization and core logic
"index.html"| Main HTML entry point

🧩 Module Architecture

                    ┌─────────────────────┐
                    │  DPS Learning Hub   │
                    │      Dashboard      │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
       ┌─────────────┐  ┌──────────────┐  ┌─────────────┐
       │ Typing Lab  │  │   Document   │  │  Excel Lab  │
       │             │  │   Mastery    │  │             │
       └──────┬──────┘  └──────┬───────┘  └──────┬──────┘
              │                │                 │
              ▼                ▼                 ▼
        Practice &       8 Interactive      8 Interactive
        Performance         Lessons             Lessons
              │                │                 │
              └────────────────┼─────────────────┘
                               ▼
                     ┌──────────────────┐
                     │ Progress Storage │
                     │   LocalStorage   │
                     └──────────────────┘

🔄 Application Flow

User
 │
 ▼
Dashboard
 │
 ├──► Typing Lab
 │       └──► Practice → Results → Progress
 │
 ├──► Document Mastery
 │       └──► Lesson → Activity → Feedback → Progress
 │
 └──► Excel Lab
         └──► Lesson → Simulation → Feedback → Progress

🛠️ Technology Scope

The project is designed as a client-side web application.

Core technologies can include:

- HTML5
- CSS3
- JavaScript
- LocalStorage
- Client-side routing

Optional technologies/frameworks can be introduced later if the project expands.

---

🚀 Getting Started

1. Clone the repository

git clone https://github.com/YOUR-USERNAME/dps-learning-hub.git

2. Enter the project directory

cd dps-learning-hub

3. Install dependencies

If the project uses a package manager:

npm install

4. Start the development server

npm run dev

The application will then be available through the local development URL provided by the development server.

---

🎯 Project Objectives

DPS Learning Hub aims to make computer education more:

- Interactive — students learn by doing.
- Practical — lessons simulate real-world tasks.
- Trackable — progress is saved locally.
- Accessible — designed for both desktop and mobile.
- Engaging — instant feedback keeps students informed.
- Consistent — all modules share the same design language.

---

🔮 Future Improvements

Potential future additions include:

- 👤 Student profiles
- ☁️ Cloud-based progress synchronization
- 🏆 Achievement/badge system
- 📈 Learning analytics
- 🥇 Typing leaderboards
- 🌙 Dark mode
- 🔐 Authentication
- 🧑‍🏫 Teacher dashboard
- 📚 More interactive lessons
- 📝 Quizzes and assessments
- 🔊 Accessibility improvements
- 🤖 AI-powered learning assistance

---

📜 License

This project is intended as an educational project. Add an appropriate open-source license if you plan to distribute the source code publicly.

---

👨‍💻 Project

DPS Learning Hub

A modern interactive learning environment focused on developing practical digital skills through engaging, hands-on experiences.

«Learn. Practice. Improve.»
