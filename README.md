# jiho-baik.github.io

Personal academic website. Plain HTML + CSS, no build step, no dependencies.

## Files

```
index.html              the entire site (content + styling in one file)
assets/
  Jiho_Baik_CV.pdf      linked from the header
  ...                   project images / GIFs go here
README.md               this file
```

## Editing

Open `index.html` in any text editor. Content sections are marked with comment
banners like `<!-- ===== PROJECTS ===== -->`. Save the file and refresh the browser
to see the change — there is nothing to compile.

### Profile photo

Save a square headshot as `assets/profile.jpg` (600×600 px is plenty), then in the
sidebar replace `<div class="avatar-placeholder">JB</div>` with:

```html
<img class="avatar" src="assets/profile.jpg" alt="Jiho Baik">
```

### Project images

Drop the file into `assets/` and replace the `<div class="media-placeholder">…</div>`
block with:

```html
<img class="project-media" src="assets/your-file.gif" alt="Short description">
```

Keep GIFs under ~5 MB so the page stays fast.

## Publishing to GitHub Pages

One-time setup:

1. Create a **public** repository on GitHub named exactly `jiho-baik.github.io`.
   The name must match the username for the site to live at the root domain.
2. From this folder, run the commands below (replace nothing — the URL is already correct).
3. In the repo on GitHub: **Settings → Pages → Source → Deploy from a branch → `main` / `(root)`**.

```bash
cd ~/Desktop/personal-website
git init -b main
git add .
git commit -m "Initial site"
git remote add origin https://github.com/jiho-baik/jiho-baik.github.io.git
git push -u origin main
```

The site goes live at **https://jiho-baik.github.io** within a minute or two.

To publish later edits:

```bash
cd ~/Desktop/personal-website
git add .
git commit -m "Update projects"
git push
```

## Notes

- The CV in `assets/` is a copy. When you update the original, copy the new version
  over `assets/Jiho_Baik_CV.pdf` and push again.
- Phone number and home address are deliberately not on the page — a public site
  gets scraped. Email is enough.
- The page adapts to light and dark mode automatically.
