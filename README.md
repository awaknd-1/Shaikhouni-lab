# Shaikhouni Lab — GitHub Pages Website

A static multi-page lab website for the **Shaikhouni Lab** at Nationwide Children's Hospital,
Department of Neurosurgery.

---

## Pages

| File | Description |
|------|-------------|
| `docs/index.html` | Home page — hero, research highlights, news |
| `docs/research.html` | Research programs and methods |
| `docs/people.html` | PI bio and lab member directory |
| `docs/publications.html` | Publication list with year filtering |
| `docs/contact.html` | Contact form and location |
| `docs/css/style.css` | Shared stylesheet |

---

## Deploying to GitHub Pages

### 1. Create a GitHub repository

```bash
# In this project directory
git init
git add docs/
git commit -m "Initial lab website"
```

Or create the repo on [github.com](https://github.com/new) and push:

```bash
git remote add origin https://github.com/YOUR_USERNAME/shaikhouni-lab.git
git push -u origin main
```

### 2. Enable GitHub Pages

1. Go to your repository on GitHub.
2. Click **Settings → Pages** (left sidebar).
3. Under **Source**, select **Deploy from a branch**.
4. Choose branch `main` and folder `/docs`.
5. Click **Save**.

Your site will be live at:
```
https://username.github.io/shaikhouni-lab/
```

*(Replace `YOUR_USERNAME` with your GitHub username and `shaikhouni-lab` with your repo name.)*

---

## Using a Custom Domain (optional)

To use a custom domain like `shaikh ounilab.org`:

1. In `docs/`, create a file named `CNAME` containing only your domain:
   ```
   shaikhounilab.org
   ```
2. Configure your DNS provider to point to GitHub Pages (see [GitHub docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)).

---

## Enabling the Contact Form

The contact form uses [Formspree](https://formspree.io) (free tier available):

1. Sign up at [formspree.io](https://formspree.io).
2. Create a new form and copy your form ID.
3. In `docs/contact.html`, replace:
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```
   with your actual form endpoint.

---

## Enabling the Google Maps Embed (optional)

In `docs/contact.html`, replace `YOUR_MAPS_API_KEY` with a valid
[Google Maps Embed API key](https://developers.google.com/maps/documentation/embed/get-api-key).

Alternatively, replace the `<iframe>` with a key-free OpenStreetMap embed:

```html
<iframe
  src="https://www.openstreetmap.org/export/embed.html?bbox=-82.9994,39.9969,-82.9954,39.9999&layer=mapnik&marker=39.9984,-82.9974"
  width="100%" height="320" style="border:0;" loading="lazy">
</iframe>
```

---

## Updating Content

| What to update | Where |
|---|---|
| Lab members / photos | `docs/people.html` — replace placeholder cards |
| Publications | `docs/publications.html` — add `.pub-item` entries |
| News items | `docs/index.html` — update news cards section |
| Research projects | `docs/research.html` — edit project blocks |
| Contact info | Footer in each HTML file |
