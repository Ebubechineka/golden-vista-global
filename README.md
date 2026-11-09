# Golden Vista Global — Portfolio

Portfolio website for Benito K Chukwuemeka (Golden Vista Global) — self-taught software engineer and designer building business websites, landing pages, web apps and books for clients in Nigeria and internationally.

## Live site

**https://goldenvistaglobal.vercel.app/**

## How to run locally

The site is pure static HTML/CSS/JS. No build step is needed.

1. Download or clone this repository.
2. Open `index.html` in any browser — that's it.

Or serve it with any static file server:

```bash
# Python
python3 -m http.server 8000
# then open http://localhost:8000
```

## How to update the site

- **Content lives in `index.html`** — all sections (hero, about, projects, services, pricing, FAQ, notes, contact) are plain HTML with clear comments.
- **New projects**: find the `<!-- PROJECTS -->` section in `index.html`. Copy one existing project card (a `<article class="project-card">` block), paste it, and change the screenshot filename, title, description and live link. Drop the screenshot into `images/portfolio/`.
- **Contact form**: the quote form does not post to any server. It builds a `mailto:` link and opens the visitor's own email app with the message pre-filled. To change the receiving address, search for `Goldenvistaglobal@gmail.com` in `index.html`.

## How to publish changes

This site is hosted on **Vercel**, deployed from this repository's `main` branch. Any commit to `main` triggers a new deployment automatically.

1. Edit the files locally (or directly on GitHub).
2. Commit and push to `main`.
3. Vercel rebuilds and publishes within about a minute.

If you prefer the GitHub web UI:

1. Go to https://github.com/Ebubechineka/golden-vista-global
2. Click **Add file → Upload files**
3. Drag in `index.html`, the `images/` folder and the PDF
4. Click **Commit changes**

## Tech notes

- **Hosting:** Vercel, static deployment, no build step, no server.
- **No third-party scripts.** The only external request is Google Fonts. There is no analytics, no tracking, no cookie, no form relay.
- **No cookies, no localStorage, no fingerprinting.** The site is a portfolio: it takes no payments, has no login and asks for no passwords.
- All asset paths are relative, so the site also works from a sub-path or any other static host.
- `.nojekyll` is kept so the folder can also be served by GitHub Pages unchanged, if ever needed.

## Structure

```
index.html                      the whole site (HTML + CSS + JS in one file)
golden-vista-global-profile.pdf one-page PDF profile (downloadable)
images/                         logo, favicons, backgrounds, portrait
images/portfolio/               project screenshots and book covers
.nojekyll                       disables Jekyll processing on GitHub Pages
```
