# 🤖 AI Workflow Documentation — RSL Mini-Hack '26
## SpendWise: Personal Finance Tracker

**Participant:** [Your Name]
**Date:** March 31, 2026
**Time Budget:** 90 minutes

---

## 1. Overview

This document describes how AI tools — specifically **Claude (Anthropic)** — were used throughout the development of SpendWise during the RSL Mini-Hack '26. The entire application was designed, architected, coded, and iterated using Claude as the primary development co-pilot, enabling a non-engineer (Product background) to produce a full-stack-style web application within the time limit.

---

## 2. AI Tool Used

| Tool | Model | Usage |
|------|-------|-------|
| Claude (claude.ai) | Claude Sonnet 4.6 | Architecture, design decisions, full code generation, debugging, feature ideation |
| Claude API (embedded) | claude-sonnet-4-20250514 | In-app AI chat assistant and financial analysis |

---

## 3. Development Steps & Prompts Used

### Step 1 — Initial App Generation

**Prompt used:**
> *[Pasted the full hackathon brief including all requirements]*
> "Please help work on this [hackathon challenge]"

**What Claude did:**
- Analysed all requirements from the brief
- Chose a tech stack (single-file HTML/CSS/JS) optimal for fast deployment with no build step
- Generated a complete working app including PIN login, dashboard with charts, transaction CRUD, category breakdown, donut chart, trend chart, AI chat, and settings
- Pre-loaded demo data so the app looks alive immediately
- Used `localStorage` for persistence (no backend required)
- Embedded the Claude API directly in the app for the AI chat feature

**Output:** Fully working ~700-line single-file web app rendered live in chat

---

### Step 2 — Feature Expansion (Engagement Layer)

**Prompt used:**
> "Yes let's add more features since we have more time. Try to be creative, something that keeps user engagement with app."

**What Claude did:**
- First presented a visual feature roadmap with 6 proposed additions, explaining the rationale for each
- Then built all 6 features into the upgraded app:

| Feature | Description |
|---------|-------------|
| 🏆 Gamification (Streaks & Badges) | Daily login streaks, XP points, level system, 9 earnable badges |
| 📅 Smart Bill Reminders | Recurring bills with due-date tracking and "due this week" alerts |
| 🎯 Savings Goals Tracker | Named goals with progress rings, contribute flow, deadline tracking |
| 📊 Monthly Report Card | AI-generated letter grade (A–D) with scores for Budget, Savings, Tracking |
| ⚡ Quick-Add Shortcuts | One-tap templates for common daily expenses (coffee, lunch, metro) |
| 🔔 Spending Anomaly Feed | Real-time alerts for unusual transactions and budget overruns |

**Additional improvements made during this step:**
- Added transaction filtering (All / Expenses / Income)
- Added currency symbol customisation in Settings
- Improved toast notifications for all user actions
- Added smooth CSS animations on tab transitions
- 5-tab bottom navigation (Home, Add, Goals, AI, Awards)

---

### Step 3 — Documentation & Deployment

**Prompt used:**
> "I will need the AI workflow documentation markdown file and definitely help with the deployment steps at the end."

**What Claude did:**
- Generated this `AI_WORKFLOW.md` file
- Produced a `DEPLOYMENT.md` with step-by-step hosting instructions for Netlify, GitHub Pages, and Vercel

---

## 4. How AI Accelerated Each Phase

### Design
- Claude made all aesthetic decisions: dark finance-themed UI, color palette, typography (Syne + DM Sans fonts), card layouts
- No Figma or design tool needed — design happened directly in code

### Coding
- 100% of the HTML, CSS, and JavaScript was written by Claude
- Claude handled complex parts: canvas-based charts, donut chart rendering, XP/levelling system, localStorage data layer
- Error handling, edge cases (empty states, validation), and mobile responsiveness all included automatically

### Debugging
- Claude self-reviewed the code during generation, catching potential issues before they surfaced
- When asked to add features, Claude integrated them cleanly without breaking existing functionality

### Feature Ideation
- Claude proposed the engagement features proactively (gamification, bills, goals) rather than just implementing what was asked
- Each suggestion came with a rationale tied to user retention

---

## 5. AI in the Product Itself

Beyond using AI to *build* the app, AI is also a **core feature** of the product:

### AI Chat Assistant (Insights Tab)
- Powered by the Claude API (`claude-sonnet-4-20250514`)
- Users can ask natural language questions: *"Where did I spend most last month?"*, *"Am I on track with budget?"*, *"Give me a savings plan"*
- The app builds a financial context string from the user's live data and sends it with each query
- Falls back to local logic if the API is unavailable (offline mode)

### Monthly Report Card
- Algorithmically generates a letter grade (A+ to D) based on budget discipline, savings rate, and tracking consistency
- Includes a personalised narrative paragraph

### Spending Anomaly Feed
- Rule-based engine detects: unusually large transactions vs. category average, budget overrun, high entertainment spend ratio
- Surfaces alerts directly on the Dashboard

---

## 6. Key Interactions Summary

| # | Prompt Intent | AI Output |
|---|---------------|-----------|
| 1 | Build full app from brief | ~700-line complete working app |
| 2 | Add engaging features | Feature plan visual + ~500-line upgraded app |
| 3 | Generate documentation | This document + deployment guide |

**Total prompts to production-ready app: 3**

---

## 7. Reflections

### What worked well
- Claude understood the full brief in a single prompt and made sensible architectural decisions without needing guidance
- The AI independently chose a deployment-friendly architecture (single HTML file, no build step, no backend)
- Feature suggestions were grounded in product thinking (engagement, retention) not just technical capability
- The embedded Claude API gives the app genuine AI intelligence, not just a chatbot façade

### What required human judgment
- Deciding *which* features to prioritise given the 90-minute constraint
- Confirming the aesthetic direction matched the intended audience
- Reviewing the final output for any data or logic issues

### Surprising moments
- Claude proactively added demo seed data so the app "comes alive" immediately on first open — without being asked
- The gamification system (XP, levels, badges) was fully implemented as a suggestion, not a requirement from the brief

---

## 8. Links

- **App URL:** [Insert Netlify/GitHub Pages URL after deployment]
- **GitHub Repo:** [Insert GitHub URL]
- **Built with:** Claude claude.ai + Anthropic API

---

*Document generated with AI assistance as part of the RSL Mini-Hack '26.*
