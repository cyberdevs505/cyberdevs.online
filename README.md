# CyberDevs Website

Public-facing website for **cyberdevs.online** — hosted on GitHub Pages.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Complete single-file website (HTML + CSS + JS) |
| `_headers` | Security headers (for Cloudflare Pages / Netlify) |
| `README.md` | This file |

## Deploying to GitHub Pages

1. Push these files to your GitHub repo (e.g. `cyberdevs/cyberdevs.github.io` or any repo)
2. Go to **Settings → Pages → Source** → select `main` branch → `/ (root)`
3. Your site will be live at `https://<username>.github.io/<repo>/`

## Adding Your Logo

Replace the two `<div class="nav-logo-icon">CD</div>` tags (in nav + footer) with:

```html
<img src="logo.png" alt="CyberDevs logo" width="36" height="36" style="border-radius:8px;">
```

Then upload your `logo.png` to the same folder as `index.html`.

## Custom Domain (cyberdevs.online)

1. In your repo, create a file called `CNAME` containing just: `cyberdevs.online`
2. In your domain registrar DNS settings, add:
   - `A` record → `185.199.108.153`
   - `A` record → `185.199.109.153`
   - `A` record → `185.199.110.153`
   - `A` record → `185.199.111.153`
   - `CNAME` record: `www` → `<username>.github.io`
3. Enable **Enforce HTTPS** in GitHub Pages settings

## Security Headers

The `_headers` file works on **Cloudflare Pages** and **Netlify**.  
For pure GitHub Pages, route traffic through **Cloudflare** (free plan) to enforce the headers.

## Contact Form

The form uses `mailto:` — it opens the visitor's mail client.  
For a real form backend (no server needed), swap it for [Formspree](https://formspree.io):

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

## Color Palette

| Role | HEX |
|------|-----|
| Background | `#000000` |
| Text | `#F8F8F8` |
| Primary Blue | `#1F5EFF` |
| Medium Blue | `#2D8CFF` |
| Light Blue | `#4CCEFF` |
| Cyan | `#61E2FF` |
| Azure | `#3AA8FF` |
