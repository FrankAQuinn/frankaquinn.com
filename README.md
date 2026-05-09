# frankaquinn.com

A single-page editorial-style site for Frank A. Quinn — Georgia commercial lines producer and founder of Quinn Alliance, a commercial lines specialty P&C and consulting firm. Designed to elevate Frank's personal brand and route serious commercial inquiries to Quinn Alliance.

---

## What's in this folder

```
frankaquinn-site/
├── index.html         The site (single file, no build step)
├── CNAME              Tells GitHub Pages which domain to serve
├── .nojekyll          Disables Jekyll processing on GitHub Pages
├── assets/
│   ├── headshot.jpg   ← drop your portrait here (4:5 portrait)
│   └── README.txt     Notes on the photo
└── README.md          This file
```

No frameworks, no build step. You can open `index.html` directly in a browser to preview.

---

## Before you publish — fill in the placeholders

Open `index.html` and search for `[` to find every placeholder. The ones to update:

| Where | What to replace |
|---|---|
| Credentials → Resident State | `[license number]` → your GA producer license number |
| Credentials → NPN | `[NPN]` → your National Producer Number |
| Credentials → Non-Resident | `[Add additional appointed states]` → list any other states |
| Credentials → Designations | `[CIC · CRM · CPCU · in progress …]` → your designations |
| Credentials → Affiliations | adjust as applicable |
| Connect → Telephone | `[your direct line]` → your phone number, plus update the `tel:` link |
| Connect → LinkedIn | `[linkedin.com/in/your-handle]` → your LinkedIn URL (also update the `href`) |
| Connect → Office | `[Atlanta · by appointment]` → your address line |

Optional polish:
- Swap the headline city in the masthead row (`Atlanta, Georgia`) if you operate elsewhere.
- The "Vol. I · Established MMXXVI" line is editorial flourish — keep, edit, or remove.

---

## Step-by-step: deploy on GitHub Pages with frankaquinn.com

### 1. Create the repo

On GitHub (logged into the account that owns the project), create a new **public** repository named:

```
frankaquinn.com
```

(The exact name doesn't matter for Pages, but matching your domain keeps things tidy.)

### 2. Upload the files

Easiest path with no command line:
1. On the new empty repo, click **uploading an existing file**.
2. Drag the **contents** of this `frankaquinn-site/` folder into the upload box — `index.html`, `CNAME`, `.nojekyll`, and the `assets/` folder. Don't upload the parent folder itself; upload what's inside it.
3. Commit directly to `main`.

Command-line path (if you prefer):
```bash
cd frankaquinn-site
git init -b main
git add .
git commit -m "Initial site"
git remote add origin https://github.com/<your-username>/frankaquinn.com.git
git push -u origin main
```

### 3. Turn on GitHub Pages

In the repo: **Settings → Pages**.
- **Source:** Deploy from a branch
- **Branch:** `main` · **Folder:** `/ (root)`
- Save.

Within a minute or two, GitHub will publish the site. The Pages settings page will show a green box with the live URL once it's ready.

### 4. Point the domain at GitHub Pages

In your domain registrar's DNS settings for **frankaquinn.com**, set these records:

**A records (apex / `@`)** — point all four to GitHub:
```
@   A   185.199.108.153
@   A   185.199.109.153
@   A   185.199.110.153
@   A   185.199.111.153
```

**AAAA records (apex / `@`)** — IPv6, optional but recommended:
```
@   AAAA   2606:50c0:8000::153
@   AAAA   2606:50c0:8001::153
@   AAAA   2606:50c0:8002::153
@   AAAA   2606:50c0:8003::153
```

**CNAME for www**:
```
www   CNAME   <your-github-username>.github.io.
```

(The trailing dot is fine; some registrars strip it automatically.)

### 5. Verify the custom domain in GitHub

Back in **Settings → Pages**:
- **Custom domain:** `frankaquinn.com`
- Save.
- Wait until DNS check shows ✓ (can take 5–60 minutes).
- Tick **Enforce HTTPS** once it becomes available.

You're live.

---

## Updating the site later

GitHub Pages publishes automatically every time you commit to `main`. Edit `index.html` in the GitHub web editor (the pencil icon on the file page), commit, and the change is live in about 60 seconds.

---

## Browser preview locally

Just double-click `index.html`. No server required. The Google Fonts will load over the network.

---

## Why this design

Editorial magazine layout — Fraunces serif headlines, drop caps, a deep oxblood accent, ivory paper background, and a dark Quinn Alliance feature panel. The architecture is intentional:

- **You** are the masthead — the human relationship and the credentials.
- **Quinn Alliance** is the institution — the place to actually buy coverage.
- The page never asks the visitor to choose between them; it routes to both.

Built to feel timeless rather than trendy. Heavy whitespace, restrained motion, no gimmicks — the kind of presence a commercial buyer expects from someone they're going to hand a million dollars of premium to.
