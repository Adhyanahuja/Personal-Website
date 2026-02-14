# Setup & testing your personal site

## What’s already done

The site is configured with the name **Adhyan** in:

- Browser tab title
- Sidebar name and avatar alt text
- Testimonial placeholders

Contact details (email, phone, birthday, location, social links) are still placeholders so you can test the layout first.

---

## How to test the website

### Option 1: Open the file in a browser

Double‑click `index.html` or drag it into a browser window.  
Works for a quick check; some features (e.g. loading local files) may behave differently than on a real server.

### Option 2: Local server (recommended)

From the project root:

```bash
# Python 3
python3 -m http.server 8000

# Or with Node (if you have npx)
npx serve .
```

Then open **http://localhost:8000** (or the port shown) in your browser.

---

## When you’re ready to add your data

Edit **`index.html`** and update:

| Section   | What to change |
|----------|----------------|
| **Sidebar** | Name, job title, email, phone, birthday, location, social links |
| **About**   | “About me” paragraphs and “What I’m doing” services |
| **Resume**  | Education, experience, skills |
| **Portfolio** | Project cards and filters |
| **Blog**   | Article entries (or remove section) |
| **Contact** | Form recipient and any extra contact info |

Replace **`./assets/images/my-avatar.png`** with your own photo.  
Replace **`./assets/images/logo.ico`** if you want a custom favicon.

If your name isn’t “Adhyan”, do a find‑and‑replace in `index.html` for **Adhyan** and **adhyan@example.com** and put in your name and email.

---

## Hosting on GitHub Pages (github.io)

To make the site public at a URL like `https://yourusername.github.io/your-repo/` (or `https://yourusername.github.io/` if you use the special repo name):

### 1. Put the project in your own GitHub repo

Because you cloned someone else’s repo, your local repo likely still points to theirs. Use **your own** repo:

- **Create a new repo** on GitHub (e.g. `personal-website` or `username.github.io`).  
  Do **not** add a README, .gitignore, or license (you already have files).
- In your project folder, add that repo as `origin` and push:

```bash
cd "/Users/adhyan/Desktop/Projects/Personal Website"

# If the current remote is the original template, replace it with your repo:
git remote set-url origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
# Or if you have no remote yet:
# git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git

git push -u origin main
```

Use your real GitHub username and repo name. If your default branch is `master`, use `git push -u origin master` and then in step 2 use the `master` branch.

### 2. Turn on GitHub Pages

- Open your repo on GitHub → **Settings** → **Pages** (sidebar).
- Under **Build and deployment**:
  - **Source**: Deploy from a branch.
  - **Branch**: `main` (or `master`), folder **/ (root)**.
- Click **Save**.

### 3. Your live URL

- If the repo is named **`yourusername.github.io`**  
  → **https://yourusername.github.io**
- Any other repo name (e.g. `personal-website`)  
  → **https://yourusername.github.io/personal-website**

The first deploy can take 1–2 minutes. Later pushes to `main` will update the site automatically.
