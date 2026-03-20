# Birch Street Law PLLC — Website

Static marketing site for [Birch Street Law PLLC](https://birchstreetlaw.com), 
a law firm in Shelton, Washington.

## Tech Stack

| Layer | Choice |
|---|---|
| Framework | [SvelteKit](https://kit.svelte.dev) |
| Adapter | `@sveltejs/adapter-static` (full SSG) |
| Markdown | [mdsvex](https://mdsvex.pngwn.io) |
| CSS | Vanilla CSS (global stylesheet + scoped component styles) |
| Fonts | Playfair Display (serif/headings) + Inter (sans/body) via Google Fonts |
| CI/CD | GitHub Actions → artifact upload (FTP to Dreamhost TBD) |

## Project Structure

```
birchstreetlaw/
├── .github/
│   └── workflows/
│       └── build.yml          # CI/CD pipeline
├── content/                   # Markdown source files (reference / CMS-lite)
│   ├── home.md
│   ├── about.md
│   └── mediation.md
├── src/
│   ├── app.html               # HTML shell (fonts, meta)
│   ├── lib/
│   │   ├── styles/
│   │   │   └── global.css     # Global design system
│   │   ├── BirchDivider.svelte  # Inline SVG birch branch accent
│   │   ├── Nav.svelte         # Sticky responsive nav with mobile drawer
│   │   └── Footer.svelte      # Site footer
│   └── routes/
│       ├── +layout.svelte     # Root layout (Nav + Footer wrapper)
│       ├── +page.svelte       # Home page
│       ├── about/
│       │   └── +page.svelte   # Attorney bios
│       ├── practice-areas/
│       │   └── +page.svelte   # Practice areas with quick-nav
│       ├── mediation/
│       │   └── +page.svelte   # FAQ accordion, fees, scheduling
│       └── contact/
│           └── +page.svelte   # Phone + location (no form)
├── static/                    # Static assets
├── svelte.config.js
├── vite.config.js
└── package.json
```

## Pages

| Route | Description |
|---|---|
| `/` | Home — hero, intro, practice areas summary, CTA |
| `/about` | Attorney bios (David P. Sisk, Rebekah Zinn) |
| `/practice-areas` | All 6 practice areas with detailed descriptions |
| `/mediation` | FAQ accordion, fees, scheduling info |
| `/contact` | Phone number and location (no form) |

## Local Development

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Open in browser
open http://localhost:5173
```

## Building for Production

```bash
npm run build
```

Output is in `build/`. The entire site is statically rendered — no server required.

## Deploying to Dreamhost

The GitHub Actions workflow (`.github/workflows/build.yml`) builds the site on every push to `main` 
and uploads the `build/` folder as a GitHub Actions artifact named **`site`**.

To enable FTP auto-deploy to Dreamhost:

1. Create these **GitHub Secrets** (repo → Settings → Secrets → Actions):
   - `FTP_SERVER` — your Dreamhost FTP hostname
   - `FTP_USERNAME` — FTP username
   - `FTP_PASSWORD` — FTP password

2. Uncomment the FTP deploy step in `.github/workflows/build.yml` and adjust the `server-dir` path.

3. Push to `main` — the action will build and deploy automatically.

## Design System

| Token | Value | Usage |
|---|---|---|
| `--green-deep` | `#2c4a35` | Primary brand, headings, buttons |
| `--green-mid` | `#4a7c59` | Links, icons, accents |
| `--green-light` | `#8ab89a` | Borders, hover states |
| `--cream` | `#f5f0e8` | Page background |
| `--cream-dark` | `#ede7d9` | Alt section background |
| `--gray-warm` | `#857f74` | Muted text |
| `--gray-dark` | `#2d2b27` | Body text |

Fonts: **Playfair Display** for headings (elegant, trustworthy); **Inter** for body (clean, legible).

## Updating Content

Content can be edited directly in the `.svelte` files or via the reference Markdown files in `content/`. 
To add attorney photos later, add images to `static/images/` and reference them in `about/+page.svelte`.

## License

Private. All rights reserved — Birch Street Law PLLC.
