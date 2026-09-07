# VieOS Portfolio

Personal one-page portfolio website for VieOS — Enterprise IT Infrastructure & Security Engineer.

## Tech Stack

- Pure HTML/CSS/JS (no framework)
- Vanilla JavaScript with Intersection Observer
- CSS custom properties for theming
- Responsive mobile-first design
- Client-side admin panel with live editing (contentEditable + localStorage)

## File Structure

```
vieos-portfolio/
├── index.html          # Main website file (all-in-one)
├── README.md           # This file
└── .gitignore          # Git ignore rules
```

## Local Development

Just open `index.html` in your browser. No build step needed.

```bash
# Optional: serve locally with live reload
npx serve .
# or
python -m http.server 8000
```

## Admin Panel

This production build does not include the client-side admin panel. It was removed for security before deployment.

To make content changes, edit `index.html` directly and push to GitHub. Cloudflare Pages will auto-rebuild and deploy in ~30 seconds.

> **Note:** For a real CMS experience, consider using Cloudflare Workers + KV storage, or a headless CMS like Contentful/Strapi.

## Deploy to Cloudflare Pages

### Option A: GitHub Integration (Recommended)

1. Push this repo to GitHub
2. Go to [Cloudflare Dashboard](https://dash.cloudflare.com) → Pages → Create a project
3. Connect your GitHub account and select this repo
4. Build settings:
   - **Build command:** (leave empty)
   - **Build output directory:** `/` (root)
   - **Root directory:** `/` (root)
5. Click **Save and Deploy**
6. Cloudflare gives you a `*.pages.dev` URL + custom domain support

### Option B: Direct Upload (No Git)

1. Go to Cloudflare Dashboard → Pages → Create a project → Direct Upload
2. Drag and drop this folder
3. Done — instant deploy

## Custom Domain on Cloudflare Pages

1. In your Pages project → Custom domains → Add domain
2. Enter your domain (e.g., `vieos.dev`)
3. Cloudflare auto-configures DNS + SSL (if domain is on Cloudflare nameservers)
4. Wait a few minutes for propagation

## Update Workflow

```bash
# Make edits locally, then:
git add .
git commit -m "feat: update hero copy"
git push origin main
# Cloudflare Pages auto-rebuilds and deploys in ~30 seconds
```

## Environment Variables / Secrets

This is a static site with no secrets. If you add a backend later, use Cloudflare Workers + environment variables for secrets.

## License

MIT — VieOS 2025
