# Softadex GitHub Organization Profile — Setup & Deployment Guide

This guide details how to publish and maintain the high-end GitHub organization profile for **Softadex** (`@softadex01-ai`).

---

## 1. Repository Structure

In GitHub organizations, a special repository named `.github` renders the profile page for the entire organization:

```text
.github/
├── .github/
│   ├── profile/
│   │   └── README.md          # Organization profile README (Wali Muhammad & Softadex details)
│   └── workflows/
│       └── update-repos.yml   # Pinned Action for auto-syncing public repositories
├── assets/
│   ├── hero-dark.svg          # Dark-mode responsive vector banner
│   ├── hero-light.svg         # Light-mode responsive vector banner
│   ├── divider-dark.svg       # Dark-mode divider
│   ├── divider-light.svg      # Light-mode divider
│   ├── logo-lockup-dark.svg   # Wordmark & monogram (dark)
│   ├── logo-lockup-light.svg  # Wordmark & monogram (light)
│   └── icons/                 # Service icons (dual-mode)
│       ├── web-dark.svg / web-light.svg
│       ├── mobile-dark.svg / mobile-light.svg
│       ├── design-dark.svg / design-light.svg
│       └── ai-dark.svg / ai-light.svg
└── SETUP.md                   # This deployment documentation
```

---

## 2. Publishing to GitHub

Since your target repository is:
👉 **`https://github.com/softadex01-ai/.github`**

Run these commands in this directory:

```bash
# 1. Initialize git (if not already done)
git init

# 2. Add remote to your org repo
git remote add origin https://github.com/softadex01-ai/.github.git

# 3. Rename branch to main
git branch -M main

# 4. Stage and commit all files
git add .
git commit -m "feat(brand): launch Softadex agency profile"

# 5. Push to GitHub
git push -u origin main
```

*(Agar repo already GitHub pe bani hui hai aur usme pehle se files hain, toh `git push -u origin main --force` ya pull karke push kar sakte ho).*

---

## 3. Recommended Organization Settings

Go to **`https://github.com/organizations/softadex01-ai/settings/profile`**:

* **Organization display name:** `Softadex`
* **Short description:** `Boutique digital studio. Precision web & mobile engineering, design systems, and rapid AI delivery.`
* **Location:** `Karachi, Pakistan`
* **Organization email:** `softadex01@gmail.com`
* **Website URL:** *(Apni website ka URL daal dein jab ready ho)*

---

## 4. Repositories to Pin

Apne org profile page par ja kar **"Customize pins"** click karein aur in repos ko pin karein:

1. **`.github`** — Studio Profile & Engineering Standard
2. **Founder portfolio / projects** — (Showcase repositories)

---

## 5. Workflow Permissions for Auto-Update

Action `.github/workflows/update-repos.yml` org ki public repos ko dynamically sync karta hai:

1. Go to: **Organization Settings** → **Actions** → **General**
2. Under **Workflow permissions**, choose **"Read and write permissions"**.
3. Save.
