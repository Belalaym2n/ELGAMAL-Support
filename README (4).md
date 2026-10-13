# El Baroudy In English — Support Website

The official App Store support page for the iOS app **El Baroudy In English**.

A static website (HTML + CSS + a little JavaScript) designed to be hosted **free on GitHub Pages** and used as the **Support URL** in App Store Connect.

- No Firebase, no backend, no server
- No Node.js, npm, or build step
- No paid domain or paid services
- Responsive (iPhone, Android, tablet, desktop) with automatic light/dark mode
- Works by simply opening `index.html`

---

## Files

```text
el-baroudy-support/
│
├── index.html   ← the page (content, contact links, FAQ)
├── style.css    ← all styling
├── script.js    ← small enhancements (copy email, animations, placeholder checks)
└── README.md    ← this guide
```

---

## ⚠️ Values you must replace before publishing

These placeholders are in **`index.html`**. Nothing was invented — you must add your real values.

| Placeholder | What to put there | Where it appears |
|---|---|---|
| `SUPPORT_EMAIL_HERE` | Your real support email address, e.g. the inbox you monitor for app support | Every `mailto:` link and the visible email address (several places — replace **all** occurrences) |
| `PRIVACY_POLICY_URL_HERE` | Full HTTPS URL of your Privacy Policy | Footer → "Privacy Policy" link |
| `TERMS_URL_HERE` | Full HTTPS URL of your Terms of Use | Footer → "Terms of Use" link |

**Easiest way:** open `index.html` in any text editor (VS Code, Notepad, TextEdit in plain-text mode) and use **Find & Replace → Replace All** for each placeholder.

Safety features while placeholders remain:

- A yellow **"Setup required"** banner appears at the top of the page listing what's missing.
- The Privacy Policy and Terms links are **hidden automatically** until you add real URLs, so the live page never shows a broken link.
- Once every placeholder is replaced, the banner disappears and the links show automatically.

If you don't have a Terms of Use page, you can remove that `<li>` line from the footer in `index.html` instead.

> Note: App Store Connect also requires a **Privacy Policy URL** in a separate field. You can host a privacy policy page on GitHub Pages the same way (for example, a `privacy.html` file in this same repository).

---

## Preview locally

Double-click `index.html` to open it in your browser. No installation needed.

---

## Publish on GitHub Pages (free)

### Step 1 — Create a GitHub repository

1. Sign in at <https://github.com> (create a free account if needed).
2. Click **+** (top right) → **New repository**.
3. Repository name: **`el-baroudy-support`**
4. Visibility: **Public** (GitHub Pages is free for public repositories).
5. Click **Create repository**.

### Step 2 — Upload the files

1. In the new repository, click **Add file → Upload files** (or the "uploading an existing file" link).
2. Drag in these four files (the files themselves, not a folder or a zip):
   ```text
   index.html
   style.css
   script.js
   README.md
   ```
3. Click **Commit changes**.

`index.html` must be at the **root** of the repository (not inside a sub-folder).

### Step 3 — Open the Pages settings

Go to **Repository → Settings → Pages** (Pages is in the left sidebar under "Code and automation").

### Step 4 — Configure the source

Under **Build and deployment**:

- **Source:** `Deploy from a branch`
- **Branch:** `main`
- **Folder:** `/ (root)`

### Step 5 — Save

Click **Save**. After a minute or two, refresh the page — GitHub shows **"Your site is live at …"** with a URL like:

```text
https://USERNAME.github.io/el-baroudy-support/
```

Replace **`USERNAME`** with your actual GitHub username. For example, if your username is `jane-dev`, the URL is `https://jane-dev.github.io/el-baroudy-support/`.

Open the URL in a private/incognito browser window to confirm it loads without logging in.

### Updating the site later

Edit a file on GitHub (pencil icon) or upload a new version and commit. GitHub Pages republishes automatically within a minute or two.

---

## Add the Support URL in App Store Connect

1. Sign in to **App Store Connect** → **Apps** → **El Baroudy In English**.
2. Open the **iOS App** version (e.g. **1.0**).
3. In **Product Page Information** (the version's information section), find **Support URL**.
4. Paste your GitHub Pages URL:
   ```text
   https://USERNAME.github.io/el-baroudy-support/
   ```
   (with `USERNAME` replaced by your GitHub username)
5. Click **Save**.

Requirements Apple checks:

- The URL must use **HTTPS** (GitHub Pages provides this automatically).
- It must be **publicly accessible without any login**.
- It must contain real, working contact information — so make sure `SUPPORT_EMAIL_HERE` is replaced first.

---

## Final verification checklist

- [ ] `index.html`, `style.css`, `script.js` are at the repository root
- [ ] `SUPPORT_EMAIL_HERE` replaced everywhere with your real support email
- [ ] `PRIVACY_POLICY_URL_HERE` replaced (or the link removed)
- [ ] `TERMS_URL_HERE` replaced (or the link removed)
- [ ] No yellow "Setup required" banner shows on the live site
- [ ] Contact Support button opens a new email to your address
- [ ] Footer links open the correct pages
- [ ] Page looks right on your iPhone and on desktop
- [ ] Live URL loads over HTTPS in a private window without login
- [ ] Support URL pasted into App Store Connect and saved
