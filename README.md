# 🚀 Career & Learning Dashboard

A personal all-in-one dashboard to track job applications, manage your learning roadmap, schedule events, and stay on top of tasks — all in a single HTML file that runs entirely in your browser, protected by a password.

**[→ View Live Demo](https://adityaamitra.github.io/Career_Tracker/)**

---

## 🔐 Privacy & Login

The dashboard is protected by a password you set on first visit. Anyone who visits your GitHub Pages URL will see a login screen — they can't see your data without the password.

- **First visit** — you'll be prompted to create a password
- **Return visits** — enter your password to get in; the session stays active until you sign out
- **Sign out** — button in the top-right corner of the dashboard
- **Forgot password** — a reset link on the login screen wipes all data and lets you start over

> **How it works:** Your password is SHA-256 hashed in the browser and stored in `localStorage`. Your data never leaves your device — there's no server involved. Since `localStorage` is per-browser, anyone visiting from a different device sees an empty setup screen, not your data.

---

## ✨ Features

### 💼 Jobs — Application tracker
- Log every application with company, position, status, and date applied
- Add the people you cold-emailed — name, designation, and email
- Track job posting URLs and personal notes per application
- Filter by status, search by company or role
- Expand any row to see full details, edit, or delete

**Statuses:** Applied → Phone Screen → Interviewing → Offer / Rejected / Ghosted

### 📅 Calendar
- Monthly view with color-coded event dots per day
- Click any day to view or add events
- Each event has a title, time, description, and color label
- Navigate months with arrow buttons

### 📚 Learning tracker
- Pre-loaded roadmaps for **Python**, **DSA in Python**, **DevOps**, **Web Development**, and **AI/ML**
- 10 topics per subject — check them off as you finish each one
- Progress bar per subject showing completion percentage
- **Weekly timetable** — click any cell to assign a subject to that slot (Morning / Afternoon / Evening / Night across Mon–Sun), click again to cycle

### ✅ Todo & notes
- Add tasks with a category tag (General, Job Search, Python, DSA, DevOps, Web Dev, AI/ML)
- Press **Enter** to quickly add
- Filter by category
- Check tasks off when done; they stay for progress tracking

### 📊 Progress overview
- Summary stats: applications sent, overall learning %, tasks done, upcoming events
- Job application funnel across all statuses
- Learning progress bars per subject + overall completion
- Task completion breakdown by category
- Upcoming events list

---

## 🗂️ Repo structure

```
your-repo/
├── index.html    ← the entire app (one file, no build step)
└── README.md
```

---

## 🚀 Deploying to GitHub Pages

### Step 1 — Create a new repository

1. Go to [github.com](https://github.com) and click **New repository**
2. Give it a name (e.g. `dashboard` or `my-tracker`)
3. Set visibility to **Public**
4. Click **Create repository**

### Step 2 — Upload the files

**Option A — via the GitHub website**
1. In your new repo, click **Add file → Upload files**
2. Drag in `index.html` and `README.md`
3. Click **Commit changes**

**Option B — via Git**
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
# Copy index.html and README.md into this folder, then:
git add .
git commit -m "Initial commit"
git push origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repo → **Settings → Pages**
2. Under **Source**, select **Deploy from a branch**
3. Branch: **main**, folder: **/ (root)**
4. Click **Save**

Your site will be live in about a minute at:
```
https://adityaamitra.github.io/Career_Tracker/
```

### Step 4 — Set your password

Open the live URL in your browser. You'll see the setup screen — create your password and you're in.

> Update the demo link at the top of this README once your site is live.

---

## 💾 Data & storage

Everything is saved in your **browser's `localStorage`** — nothing is sent to any server or stored in this repository.

| | Detail |
|---|---|
| ✅ Persists across sessions | Close the tab, come back later — your data is still there |
| ✅ Password protected | Visitors to your URL see a login screen, not your data |
| ✅ Works offline | After the first load, no internet required |
| ⚠️ Device-specific | Data lives in the browser you used; a different device means a fresh start |
| ⚠️ Clearing browser data | Clearing site data / localStorage will erase everything |

**Backing up your data:** Open the browser console (`F12 → Console`) and run:
```js
JSON.stringify(localStorage)
```
Copy the output somewhere safe. To restore it on another browser:
```js
const data = { /* paste your backup here */ };
Object.entries(data).forEach(([k, v]) => localStorage.setItem(k, v));
location.reload();
```

---

## 🛠️ Tech stack

| | Purpose |
|---|---|
| Plain HTML + CSS + JavaScript | Everything — structure, style, and logic |
| Web Crypto API (`SubtleCrypto`) | SHA-256 password hashing, built into all modern browsers |
| Browser `localStorage` | Data and session persistence |
| Tabler Icons (CDN) | Icon font — the only external dependency |

No React. No build step. No Node.js. No dependencies to install. Download and open.

---

## 📚 Learning roadmap topics

<details>
<summary>Python (10 topics)</summary>

Variables & Data Types · Control Flow · Functions · OOP · Modules & Packages · File I/O · Error Handling · List Comprehensions · Decorators · Async/Await
</details>

<details>
<summary>DSA in Python (10 topics)</summary>

Arrays & Lists · Linked Lists · Stacks & Queues · Hash Tables · Trees & BST · Graphs · Sorting Algorithms · Searching · Dynamic Programming · Recursion
</details>

<details>
<summary>DevOps (10 topics)</summary>

Linux Basics · Shell Scripting · Git & Version Control · Docker · Kubernetes · CI/CD Pipelines · AWS Basics · Monitoring & Logging · Infrastructure as Code · Networking
</details>

<details>
<summary>Web Development (10 topics)</summary>

HTML & CSS · JavaScript · React · REST APIs · Node.js · SQL Databases · Authentication · Deployment · TypeScript · Testing
</details>

<details>
<summary>AI/ML (10 topics)</summary>

Python for ML · NumPy & Pandas · Data Visualization · Scikit-learn · Regression & Classification · Neural Networks · Deep Learning (PyTorch) · NLP Basics · Computer Vision · LLMs & Prompting
</details>

---

## 📋 Job application statuses

| Status | Meaning |
|---|---|
| 🔵 Applied | Application submitted |
| 🟣 Phone Screen | Initial recruiter call scheduled or completed |
| 🟡 Interviewing | In the interview loop |
| 🟢 Offer | Received an offer |
| 🔴 Rejected | Application declined |
| ⚫ Ghosted | No response after follow-ups |

---

*One file. No installs. No accounts. Just open and go.*
