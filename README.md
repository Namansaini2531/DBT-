# 🏛️ DBT Aadhaar Seeding Awareness Portal

> A responsive, accessible government-style web portal to spread awareness about DBT-enabled Aadhaar seeding for scholarship disbursement under Pre-Matric and Post-Matric scholarship schemes for SC students.

---

## 🔗 Live Demo

**Vercel Deployment:**

```
https://direct-bt.vercel.app/guide.html
```

---

## 📌 Project Overview

This portal was built as part of an academic mini-project to help students and beneficiaries understand how to link their Aadhaar with bank accounts to receive government scholarships through the Direct Benefit Transfer (DBT) system.

The project simulates an official government awareness portal with features like multilingual support, FAQ system, notice filtering, accessibility controls, and interactive search — focused on improving user experience and accessibility for beneficiaries across different backgrounds.

---

## 🎯 Purpose

| Goal | Description |
|------|-------------|
| **Awareness** | Educate SC students about DBT-enabled Aadhaar seeding for scholarship payments |
| **Accessibility** | Provide accessible UI with font size controls and multilingual support |
| **Guidance** | Step-by-step guide to complete DBT seeding at bank branches |
| **Support** | FAQ, contact forms, and helpline information for users who need help |

---

## 🗂️ Project Structure

```
DBT-Aadhaar-Seeding-Portal/
│
├── index.html          → Home page (Hero, Info Cards, Stats, Quiz, Quick Links)
├── about.html          → About DBT page (DBT overview, schemes, technology)
├── guide.html          → Step-by-step DBT Seeding Guide
├── notices.html        → Notices & Circulars with filter and sort
├── contact.html        → Contact Us with form and helpline details
├── faq.html            → Frequently Asked Questions with search
│
├── styles.css          → All styles (responsive, accessible, themed)
└── script.js           → All JavaScript (search, FAQ, notices, accessibility)
```

---

## 📄 Pages & Features

### 1. `index.html` — Home Page
- **Accessibility Bar** — Skip to content, Font size controls (A- / A / A+), Language selector (English, Hindi, Bengali, Tamil)
- **Hero Section** — Headline, subtitle, CTA buttons (Get DBT Seeding Guide, Latest Notices), hero image
- **Important Notice Banner** — Scrolling orange warning banner about DBT requirement
- **Key Information Cards** — What is DBT Seeding, DBT-Enabled Account, Benefits
- **Comparison Section** — Aadhaar Linking vs DBT Seeding comparison cards with featured badge
- **Scholarship Schemes** — Pre-Matric and Post-Matric scholarship scheme details
- **Statistics Section** — 50L+ students benefited, ₹5000Cr+ disbursed, 99% success rate, 28 states
- **Quiz Section** — Animated quiz CTA linking to Google Forms
- **Quick Links** — Cards for Guide, Notices, Helpline, FAQ
- **Footer** — Important links, policies, contact info, helpline, copyright

---

### 2. `about.html` — About DBT
- Mission statement highlight box
- Key features of DBT (Targeted Delivery, Speed, Security, Reduced Leakages)
- 4-step DBT process flow diagram
- Benefits for beneficiaries and government (two-column grid)
- Pre-Matric and Post-Matric scholarship scheme cards
- DBT impact statistics (950+ schemes, ₹7.35 lakh crore transferred)
- Technology infrastructure (Aadhaar Auth, Banking Network, PFMS, Digital Platforms)

---

### 3. `guide.html` — DBT Seeding Guide
- Important information warning box
- 5-step seeding process (Visit Bank → Request DBT Seeding → Fill Form → OTP Verification → Confirmation)
- Alternative methods (ATM method, Online/Mobile Banking)
- Verification methods (SMS to 51969, Online on uidai.gov.in, Bank Statement)
- Accordion-style common issues and solutions (Name Mismatch, Mobile Not Updated, Account Not DBT Enabled, Transaction Failed)
- Help section with helpline, live chat, and email support

---

### 4. `notices.html` — Notices & Circulars
- Type filter (Notices / Circulars / Announcements / Advisories)
- Year filter (2024 / 2023 / 2022)
- Sort options (Newest First / Oldest First / Title A-Z / Title Z-A)
- Live search filtering of notices
- Color-coded notice type badges
- Download PDF and View Details buttons (simulated)
- Load More button
- No results state

---

### 5. `contact.html` — Contact Us
- Emergency helpline card (1800-11-1234, 24/7)
- Contact method cards (Phone, Email, Live Chat, SMS)
- Full contact form (First Name, Last Name, Email, Phone, Query Type, Subject, Message, File Attachment, Privacy checkbox)
- Head Office and Technical Support Center addresses
- Regional Support Centers (Northern / Western / Southern / Eastern India)
- Quick FAQ links for common queries

---

### 6. `faq.html` — Frequently Asked Questions
- Real-time search across all FAQ questions and answers
- 13 detailed FAQ entries covering:
  - DBT Seeding vs Aadhaar Linking difference
  - How to verify DBT status
  - Online DBT seeding options
  - Mandatory nature of DBT for scholarships
  - Scholarship eligibility and income limits
  - Common errors and troubleshooting
  - Joint account usage
  - Mobile number update process
- Toggle open/close per FAQ item
- "Still Have Questions?" CTA section

---

## ⚙️ JavaScript Features (`script.js`)

| Feature | Description |
|---------|-------------|
| **Font Size Control** | Switches between small / normal / large, saves preference in `localStorage` |
| **Language Selector** | Simulated translation to Hindi with common term mapping; placeholder for Google Translate API |
| **Search (General)** | Highlights matching text on home and other pages using DOM TreeWalker |
| **Notice Filtering** | Filters by type, year, and search term simultaneously |
| **Notice Sorting** | Sorts by date (asc/desc) or title (asc/desc) using `.sort()` with `data-date` attributes |
| **FAQ Toggle** | Accordion-style expand/collapse with CSS `max-height` animation |
| **FAQ Search** | Filters FAQ items live on `keyup` based on question and answer content |
| **Contact Form** | Validates required fields, simulates submission with ref number generation |
| **Smooth Scrolling** | Applied to all anchor (`#`) links using `scrollIntoView()` |
| **Last Updated Date** | Dynamically renders today's date in footer using `toLocaleDateString('en-IN')` |
| **Translation Loading** | Overlay loader and success/error toast notification |

---

## 🎨 CSS Overview (`styles.css`)

### Key CSS Features
| Feature | Implementation |
|---------|----------------|
| **Responsive Layout** | CSS Grid + Flexbox with `auto-fit` / `minmax()` |
| **Mobile Breakpoints** | `@media (max-width: 768px)` and `@media (max-width: 480px)` |
| **Sticky Navigation** | `position: sticky; top: 0; z-index: 100` |
| **Font Size Classes** | `.font-small`, `.font-normal`, `.font-large` toggled via JS |
| **Accordion Animations** | `max-height: 0` → `max-height: 500px` with CSS transition |
| **FAQ Animations** | Same `max-height` transition approach |
| **Hover Effects** | `translateY(-4px)` + `box-shadow` lift on cards |
| **Gradient Headers** | `linear-gradient(135deg, ...)` on header, hero, stats section |
| **Badge Colors** | Unique color per notice type (blue, green, orange, pink) |
| **Quiz Animation** | `@keyframes float` and `@keyframes bounce` for visual engagement |
| **Search Highlight** | `.search-highlight` with yellow background injected via JS |

---

## ♿ Accessibility Features

- **Skip to Main Content** button in accessibility bar
- **Font size adjustment** (A- / A / A+) saved in localStorage
- **Keyboard-friendly navigation** with focus states
- **`aria` labels** on interactive elements
- **Semantic HTML** throughout (`<header>`, `<nav>`, `<main>`, `<footer>`, `<section>`)
- **High contrast** text and button colors

---

## 🌐 Multilingual Support

Language selector supports:
- English (default — reloads page)
- हिन्दी (Hindi — key terms translated via JS mapping)
- বাংলা (Bengali — placeholder, extendable)
- தமிழ் (Tamil — placeholder, extendable)

> **Note:** Full translation requires integration with [Google Cloud Translation API](https://cloud.google.com/translate) or [LibreTranslate](https://libretranslate.com/). The current implementation includes a static mapping for common Hindi terms as a demonstration.

---

## 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| **HTML5** | Page structure and semantic markup |
| **CSS3** | Styling, animations, responsive design, CSS variables |
| **JavaScript (Vanilla)** | DOM manipulation, search, filters, form handling, accessibility |
| **Google Fonts (Inter)** | Clean, modern typography |
| **Inline SVG** | Government emblem and Digital India / DBT Mission logos |

> No frameworks or libraries used — pure HTML, CSS, and JavaScript.

---

## 🚀 How to Run Locally

### Option 1: Direct Browser Open
```bash
# Clone or download the project folder
# Open index.html directly in any browser
```

### Option 2: Live Server (VS Code)
```
1. Install the "Live Server" extension in VS Code
2. Right-click on index.html
3. Select "Open with Live Server"
4. Browser opens at http://127.0.0.1:5500
```

### Option 3: Python HTTP Server
```bash
cd project-folder
python -m http.server 8000
# Open http://localhost:8000 in browser
```

---

## 📂 Key Sections Summary

| Page | Sections Count | Interactive Features |
|------|---------------|----------------------|
| index.html | 8 sections | Search, Language, Font Size, Quiz link |
| about.html | 6 sections | Font Size, Language, Breadcrumb |
| guide.html | 6 sections | Accordion, Font Size, Language |
| notices.html | 3 sections | Filter, Sort, Live Search |
| contact.html | 6 sections | Contact Form, Live Chat button |
| faq.html | 3 sections | FAQ Toggle, Live Search |

---

## 🧑‍💻 Developer

| Field | Details |
|-------|---------|
| **Name** | Naman |
| **Institution** | GLBITM, Greater Noida |
| **Branch** | B.Tech CSE — 2nd Year |
| **LinkedIn** | [linkedin.com/in/naman-sainib19967333](https://linkedin.com/in/naman-sainib19967333) |

---

## 📜 Disclaimer

This is an **academic awareness project** built for educational purposes. It is not an official Government of India portal. All government scheme details, helpline numbers, and statistics are referenced from publicly available information for demonstration purposes only.

---

## 📄 License

This project is open for educational use. Feel free to fork and improve.

---

*Last Updated: 2026*
