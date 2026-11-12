# SkillBarter — Zero-Money Campus Skill Exchange Marketplace

> **Course:** CSE326 — Internet Programming  
> **Academic Task:** CA1 Project (30 Marks)  
> **Project Topic #7:** *Skill Exchange Marketplace — Students teach skills in exchange for learning other skills without monetary transactions.*

---

## 1. Problem Statement & Real-World Innovation

University campuses are filled with extraordinary peer talent — one student masters **C++ Data Structures**, another plays **Acoustic Guitar**, another speaks **Conversational French**, and another designs **Figma UI Systems**. Yet paid coaching is expensive, while traditional skill-swapping fails whenever two students don't directly need each other's exact skill (*the classic economic Double Coincidence of Wants*).

**SkillBarter** solves peer-to-peer campus learning with **zero monetary transactions (`₹0`)** through three integrated mechanisms:

1. **Bilateral Mutual Compatibility Engine (`js/matcher.js`):** Computes real-time compatibility scores (`56% – 98%`) comparing your offered and wanted skills against every peer listing.
2. **3-Way Circular Barter Ring Detector (`js/matcher.js`):** Uses a **directed graph 3-cycle algorithm (`You → Peer A → Peer B → You`)** to unlock group exchanges when 1-on-1 swaps aren't possible.
3. **Equitable Time-Bank Hour Credits (`1 Hour Taught = 1 HC`):** Every hour taught mints `1 HC` on a transparent double-entry ledger, redeemable with any mentor on campus — backed by regex validation guards that block currency symbols (`₹`, `$`, `Rs`, `UPI`) across all forms.

---

## 2. Mapping to All 10 CSE326 Course Requirements

| # | Course Requirement | Practical Implementation in SkillBarter | Key Files |
|---|---|---|---|
| **1** | **HTML Fundamentals & Semantic HTML** | Valid HTML5 document using `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<output>`, `<meter>`, `<details>/<summary>`, `<time>`, `<footer>`, skip-link & ARIA roles | `index.html`, `404.html` |
| **2** | **Forms & Form Validation** | 4 interactive forms (`Post Skill`, `Swap Proposal`, `Edit Profile`, `Group Roster`) with HTML5 constraints + real-time JS validation, character counters, self-swap prevention & anti-monetary regex guard | `js/validation.js`, `index.html` |
| **3** | **Cascading Style Sheets (CSS)** | Modular CSS3 with `:root` & `[data-theme="dark"]` custom properties, CSS Grid, Flexbox, fluid `clamp()` typography, keyframe animations & print styles | `css/variables.css`, `css/base.css`, `css/layout.css`, `css/components.css` |
| **4** | **JavaScript Fundamentals** | Modular ES6+ architecture using closures, IIFE namespacing, higher-order array methods (`map`, `filter`, `reduce`, `some`, `every`, `sort`), Sets & graph traversal | `js/data.js`, `js/matcher.js`, `js/validation.js` |
| **5** | **DOM Manipulation & Event Handling** | Event delegation on dynamic grids, live keystroke form card preview, debounced search, accessible tab controller, milestone checklists, Pomodoro timer & keyboard shortcuts (`/`, `Esc`) | `js/app.js` |
| **6** | **Browser APIs (6 Native APIs)** | `localStorage` (with safe fallback), **HTML5 Canvas 2D API** (PNG Mentor Certificate generator), **Web Speech API** (voice search), **Clipboard API**, **FileReader API** (avatar upload/compression) & `matchMedia` | `js/storage.js`, `js/certificate.js`, `js/app.js` |
| **7** | **Responsive Web Design** | Fluid desktop, tablet (`<=1080px`, `<=880px`), and mobile (`<=640px`) layouts with slide-down hamburger navigation drawer and touch-friendly controls | `css/responsive.css` |
| **8** | **Debugging & Testing Techniques** | Built-in **20-Assertion Automated Unit & Integration Test Runner**, XSS sanitizer tests, Browser API capability matrix, and structured `SkillBarter.Logger` console | `js/tests.js`, `js/logger.js`, `tests/test-suite.html` |
| **9** | **Code Organization & Documentation** | Clean separation of concerns across `css/`, `js/`, `tests/`, and `docs/` with JSDoc comments, Proposal Guide, and Viva Voce Q&A notes | `README.md`, `docs/PROPOSAL_AND_VIVA.md` |
| **10** | **Deployment using GitHub Pages** | Zero-build static architecture with `.nojekyll` and `404.html` — works identically on GitHub Pages HTTPS URLs and local offline `file://` Viva demos | `.nojekyll`, `404.html`, `index.html` |

---

## 3. Project Folder Structure

```text
skill-exchange-marketplace/
├── index.html                  # Semantic HTML5 Single-Page Marketplace & Workspace
├── 404.html                    # Custom 404 fallback page for GitHub Pages
├── .nojekyll                   # Disables Jekyll processing on GitHub Pages
├── css/
│   ├── variables.css           # Light & Dark mode CSS custom properties (design tokens)
│   ├── base.css                # Reset, focus rings, semantic element defaults & keyframes
│   ├── layout.css              # Header, hero split grid, bento stats, marketplace & workspace grids
│   ├── components.css          # Cards, badges, forms, validation states, modals, ledger & toasts
│   └── responsive.css          # Tablet/mobile media queries & print stylesheet
├── js/
│   ├── logger.js               # Structured diagnostic logger & XSS HTML-escape utility
│   ├── data.js                 # Realistic campus seed listings, profile, proposals & ledger
│   ├── storage.js              # Resilient localStorage adapter + JSON/CSV backup utilities
│   ├── validation.js           # Form & Zero-Monetary-Transaction validation rules
│   ├── matcher.js              # Bilateral compatibility scorer + 3-way circular ring detector
│   ├── certificate.js          # HTML5 Canvas 2D Peer Mentor Certificate renderer & PNG exporter
│   ├── tests.js                # 20 automated unit & integration assertions
│   └── app.js                  # DOM rendering, event delegation, voice search & live timer
├── tests/
│   └── test-suite.html         # Standalone visual QA & unit test runner page
└── docs/
    └── PROPOSAL_AND_VIVA.md    # Google Form Proposal template + 3-member Viva Voce Q&A guide
```

---

## 4. Team Division (Group of 3 Students)

> **Tip:** You can also click **"Edit Team"** in the website footer to enter your three group members' real names and LPU Registration Numbers directly in the UI!

1. **Member 1 — Frontend Structure, Semantic HTML5 & Responsive CSS Architecture:**  
   Designed `index.html`, `404.html`, `css/variables.css`, `css/layout.css`, `css/components.css`, and `css/responsive.css` (WCAG focus accessibility, light/dark themes, responsive breakpoints).
2. **Member 2 — Core JavaScript Logic, Forms Validation & Barter Matching Engine:**  
   Engineered `js/data.js`, `js/validation.js`, `js/matcher.js`, and interactive DOM workflows in `js/app.js` (2-way compatibility scoring, 3-way circular swap cycle detection, real-time card preview).
3. **Member 3 — Browser APIs, Automated Testing, Documentation & GitHub Pages Deployment:**  
   Implemented `js/storage.js`, `js/certificate.js` (Canvas 2D PNG certificates), Web Speech & FileReader integrations, `js/tests.js` (20 unit tests), `tests/test-suite.html`, and GitHub Pages CI deployment.

---

## 5. Step-by-Step Deployment to GitHub Pages

1. Create a new public repository on GitHub named `skill-exchange-marketplace`.
2. Open a terminal inside this project folder and run:

```bash
git init
git add .
git commit -m "feat: complete CSE326 SkillBarter zero-money skill exchange marketplace"
git branch -M main
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/skill-exchange-marketplace.git
git push -u origin main
```

3. On GitHub, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Select branch **`main`** and folder **`/ (root)`**, then click **Save**.
6. Within ~60 seconds, your live application will be published at:  
   `https://<YOUR_GITHUB_USERNAME>.github.io/skill-exchange-marketplace/`

---

## 6. Running Automated Tests Locally

- **In Browser (Main App):** Scroll to the footer and click **"Run QA & Unit Tests (20 Assertions)"**.
- **In Browser (Standalone Page):** Open `tests/test-suite.html`.
- **Via Node CLI (Optional):**
  ```bash
  node -e "['logger','data','storage','validation','matcher','certificate','tests'].forEach(m=>require('./js/'+m+'.js')); console.log(SkillBarter.TestSuite.runAll());"
  ```
