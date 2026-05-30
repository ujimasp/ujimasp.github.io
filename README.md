# Ujima S&P Website

Afrofuturist-themed website for the Ujima Security and Privacy Research Group at UC San Diego.

## File Structure

```
ujima-site/
├── index.html          ← Homepage
├── researchers.html    ← Team page
├── projects.html       ← Research projects
├── publications.html   ← Publications list
├── news.html           ← News & updates
├── contact.html        ← Contact form
├── assets/
│   ├── style.css       ← All shared styles
│   ├── logo.png        ← Ujima S&P logo
│   └── tshirt.png      ← T-shirt design reference
└── README.md
```

---

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `ujimasp-website`)
2. Upload all files keeping the folder structure
3. Go to **Settings → Pages**
4. Set Source to `main` branch, `/ (root)` folder
5. Your site will be live at `https://yourusername.github.io/ujimasp-website/`

**Custom domain (ujimasp.com):**
- In GitHub Pages settings, add your custom domain
- In your domain registrar (Google Domains, Namecheap, etc.), add a CNAME record pointing to `yourusername.github.io`

---

## Editing Guide

### Adding researcher headshots
1. Create a folder: `assets/headshots/`
2. Save photos as JPG, ideally square crop, 400×400px minimum
3. In `researchers.html`, find the placeholder comments like:
   ```html
   <!-- REPLACE with: <img class="researcher-photo" src="assets/headshots/mya-bolds.jpg" alt="Mya Bolds"/> -->
   ```
4. Delete the `<div class="researcher-photo-placeholder">...</div>` block
5. Uncomment and use the `<img>` tag instead

### Adding/editing publications
In `publications.html`, each publication is a `.pub-entry` block.
Replace the `[YEAR]`, `[Venue]`, `[Venue Type]`, title, authors, and `href="#"` with real values.
To add more publications, copy one entire `<div class="pub-entry">` block and paste it above or below.

### Adding news items
In `news.html`, copy a `.news-entry` block and fill in the date, category badge, headline, and body text.
Badge color: use `badge gold` for awards/publications, `badge green` for events/talks, `badge` (plain) for general news.

### Enabling the contact form
The form in `contact.html` needs a backend to actually send emails. Easiest options:

**Formspree (free tier available):**
1. Sign up at formspree.io
2. Create a new form, get your form ID
3. Change the form tag to: `<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">`

**Netlify Forms (if hosting on Netlify):**
1. Add `netlify` attribute to the `<form>` tag
2. Netlify handles the rest automatically

### Enabling the stats section (homepage)
When you're ready to show stats, open `index.html` and find the HTML comment block:
```
<!-- ─── Stats (commented out — update when ready) ──────────── -->
```
Remove the `<!--` at the start and `-->` at the end of that entire section.
Update the numbers before uncommenting.

### Fonts
The site uses Google Fonts: Syne (headings) + Space Mono (body/labels).
They load from the internet via `@import` in `style.css`. If you want to self-host fonts for offline use, download them from fonts.google.com and update the CSS path.

---

## Colors
- Black: `#0a0a0a`
- White/Cream: `#f0ede6`
- Gold: `#d4af37`
- Green: `#4caf50`

---

## Contact
Lab website: https://www.ujimasp.com  
Led by Dr. Imani N. S. Munyaka · UC San Diego
