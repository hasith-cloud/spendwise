# 🚀 Deployment Guide — SpendWise

Quick guide to get your app live in under 10 minutes using free hosting.

---

## Option A — Netlify Drop (Fastest: ~2 minutes)

No account needed for a quick demo URL. For a permanent link, create a free account.

1. Go to **[app.netlify.com/drop](https://app.netlify.com/drop)**
2. Drag and drop your `spendwise.html` file onto the page
3. Netlify generates a live URL instantly (e.g. `https://random-name-123.netlify.app`)
4. ✅ Done — share the URL

**To make it permanent & rename it:**
1. Create a free account at netlify.com
2. In your site dashboard → **Site settings → Change site name**
3. You can set a custom subdomain like `spendwise-yourname.netlify.app`

---

## Option B — GitHub Pages (Best for submitting source code too)

This gets you both a GitHub repo link AND a hosted URL in one step.

### Step 1 — Create a GitHub repo
1. Go to **[github.com/new](https://github.com/new)**
2. Name it `spendwise` (or any name)
3. Set it to **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

### Step 2 — Upload your files
1. In your new repo, click **Add file → Upload files**
2. Upload `spendwise.html` — **rename it to `index.html`** before uploading (GitHub Pages serves `index.html` as the root)
3. Also upload `AI_WORKFLOW.md` and `DEPLOYMENT.md`
4. Commit the files

### Step 3 — Enable GitHub Pages
1. Go to **Settings → Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Branch: `main`, Folder: `/ (root)`
4. Click **Save**
5. Wait ~60 seconds, then your site is live at:
   `https://YOUR-USERNAME.github.io/spendwise`

---

## Option C — Vercel (Best performance)

1. Go to **[vercel.com](https://vercel.com)** and sign up with GitHub
2. Click **New Project → Import** your GitHub repo (from Option B)
3. No configuration needed — Vercel auto-detects the HTML file
4. Click **Deploy**
5. Your app is live at `https://spendwise.vercel.app` (or similar)

---

## Recommended File Structure for GitHub Repo

```
spendwise/
├── index.html          ← The main app (rename from spendwise.html)
├── README.md           ← Brief description of the project
├── AI_WORKFLOW.md      ← AI documentation (required deliverable)
└── DEPLOYMENT.md       ← This file
```

---

## README.md Template

Copy this into your GitHub README:

```markdown
# SpendWise 💰

A personal finance tracking app built in 90 minutes for RSL Mini-Hack '26.

## 🔗 Live App
[Insert your Netlify/GitHub Pages URL here]

## 🔑 Login
PIN: `1234` (can be changed in Settings)

## ✨ Features
- Dashboard with income/expense summary and charts
- Transaction management (add, delete, filter)
- Savings Goals tracker with progress rings
- Recurring Bills with due-date reminders
- AI Chat assistant (powered by Claude API)
- Monthly Report Card with letter grade
- Spending Anomaly alerts
- Gamification: XP, levels, streaks, and badges
- Quick-add shortcuts for common expenses
- Mobile responsive

## 🤖 Built With
- HTML / CSS / JavaScript (single file, no framework)
- Claude AI (claude.ai) for development
- Anthropic Claude API for in-app AI features
- localStorage for data persistence

## 📄 AI Documentation
See [AI_WORKFLOW.md](./AI_WORKFLOW.md) for full documentation of AI usage.
```

---

## Sharing Credentials for Judges

When submitting, include:

| Item | Value |
|------|-------|
| App URL | [Your deployed URL] |
| GitHub Repo | [Your repo URL] |
| PIN to log in | `1234` |
| AI docs | `AI_WORKFLOW.md` in the repo |

---

*That's it — your app is live! 🎉*
