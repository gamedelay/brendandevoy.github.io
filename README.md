# brendandevoy.github.io

Windows 95-themed personal site for brendandevoy.com, hosted free on GitHub Pages.

---

## How to set this up

### Step 1 — Create your GitHub repository

1. Go to [github.com](https://github.com) and log in
2. Click the **+** button (top right) → **New repository**
3. Name it exactly: `brendandevoy.github.io`
4. Set visibility to **Public**
5. Tick **Add a README file**
6. Click **Create repository**

---

### Step 2 — Upload the site files

Your repository needs this folder structure:

```
brendandevoy.github.io/
├── index.html
├── README.md
└── images/
    ├── me.png           ← your profile photo
    ├── misfit1.jpg      ← Misfit beer images
    ├── misfit2.jpg
    ├── misfit3.jpg
    ├── misfit4.jpg
    ├── misfit5.jpg
    ├── misfit6.jpg
    ├── bundi1.jpg       ← bundipaints artwork images
    ├── bundi2.jpg
    ├── bundi3.jpg
    ├── bundi4.jpg
    ├── bundi5.jpg
    ├── bundi6.jpg
    ├── bundi7.jpg
    └── bundi8.jpg
```

**To upload:**
1. Open your repository on GitHub
2. Click **Add file → Upload files**
3. Drag in `index.html` and this `README.md`
4. Click **Commit changes**

**To create the images folder:**
1. Click **Add file → Create new file**
2. Type `images/placeholder.txt` in the filename box
3. Add any text to the file body
4. Click **Commit changes**
5. Now go into the `images/` folder and click **Add file → Upload files**
6. Upload all your images
7. Click **Commit changes**

---

### Step 3 — Enable GitHub Pages

1. In your repository, click **Settings**
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Set Branch to **main** and folder to **/ (root)**
5. Click **Save**
6. Wait about 60 seconds
7. Your site will be live at `https://brendandevoy.github.io`

---

### Step 4 — Point your custom domain (brendandevoy.com)

**In GitHub:**
1. Go to **Settings → Pages**
2. Under **Custom domain**, type `brendandevoy.com`
3. Click **Save**
4. Tick **Enforce HTTPS** once it appears

**In your domain registrar** (wherever you bought brendandevoy.com):
1. Go to your DNS settings
2. Delete any existing A records pointing to Squarespace
3. Add these new records:

| Type  | Name | Value              |
|-------|------|--------------------|
| A     | @    | 185.199.108.153    |
| A     | @    | 185.199.109.153    |
| A     | @    | 185.199.110.153    |
| A     | @    | 185.199.111.153    |
| CNAME | www  | brendandevoy.github.io |

DNS changes take up to 24 hours but usually under an hour.
GitHub will automatically provision a free SSL certificate (https://).

---

### Step 5 — Adding your images

Open `index.html` and find the placeholder comments. They look like this:

```html
<!-- Replace ppt-img-ph divs with: <img class="ppt-img" src="images/misfit1.jpg" alt=""> -->
<div class="ppt-img-ph">add image</div>
```

Replace each placeholder div with a real image tag:

**Misfit page:**
```html
<img class="ppt-img" src="images/misfit1.jpg" alt="Misfit Beer">
<img class="ppt-img" src="images/misfit2.jpg" alt="Misfit Beer">
```

**Bundipaints page:**
```html
<img class="paint-img" src="images/bundi1.jpg" alt="Artwork">
<img class="paint-img" src="images/bundi2.jpg" alt="Artwork">
```

You can add as many images as you like — the grid adjusts automatically.

---

### Step 6 — Cancel Squarespace

Once your site is live on GitHub Pages and your domain is pointing correctly:

1. Log into Squarespace
2. Go to **Settings → Billing & Account → Cancel subscription**
3. Your domain (brendandevoy.com) is registered separately and you keep it

> **Note:** Make sure your domain is registered through your registrar (e.g. GoDaddy, Namecheap), NOT through Squarespace. If Squarespace is your registrar, transfer the domain out first before cancelling.

---

## Making edits to the site

All the content is in `index.html`. To edit:

1. Open the file in your GitHub repository
2. Click the **pencil icon** (Edit this file)
3. Make your changes
4. Click **Commit changes**
5. The site updates automatically within ~30 seconds

Or edit locally with any text editor (Notepad, VS Code, etc.) and re-upload.

---

## Contact form (optional upgrade)

The current contact form opens the visitor's email client. For a proper backend form that emails you directly without requiring the visitor to have email set up, sign up for free at [formspree.io](https://formspree.io):

1. Create a free account
2. Create a new form — you'll get a URL like `https://formspree.io/f/abcdefgh`
3. In `index.html`, find the `submitContact` function and replace the mailto line with a fetch to your Formspree URL

---

**Total ongoing cost: $0** — GitHub Pages is free forever for public repositories.
