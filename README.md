# Swiss Style Linktree — International Typographic Style Creator Hub

[![Astro 5](https://img.shields.io/badge/Astro-v5.0+-BC52EE.svg?style=flat&logo=astro&logoColor=white)](https://astro.build)
[![Tailwind CSS v4](https://img.shields.io/badge/Tailwind_CSS-v4.0-38B2AC.svg?style=flat&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![Bun](https://img.shields.io/badge/Bun-1.0+-FBF0DF.svg?style=flat&logo=bun&logoColor=black)](https://bun.sh)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Deploy with GitHub Pages](https://github.com/robinsehnalik/linktree-swiss/actions/workflows/astro.yml/badge.svg)](https://github.com/robinsehnalik/linktree-swiss/actions/workflows/astro.yml)

A modernist, minimalist Linktree-style landing page inspired by the **Swiss Style (International Typographic Style)**. Built with **Astro 5**, **Tailwind CSS v4**, and **Astro Content Collections**, it prioritizes objective visual clarity, asymmetric structural grids, hairline rules, and iconic Swiss vermillion red accents.

---

## ✨ Highlights & Features

- **📐 International Typographic / Swiss Style Design**:
  - Strict mathematical grid alignment with asymmetric structured layouts.
  - Crisp hairline borders and structural rules (`--swiss-rule: #000000`, `--swiss-grid-line`).
  - Objective modernist typography: Plus Jakarta Sans with JetBrains Mono tabular numerals.
  - Iconic Swiss color palette: Warm concrete white canvas (`#f4f4f4`), stark white cards (`#ffffff`), dense black ink (`#111111`), and vibrant Swiss vermillion red accent (`#ff3300`).
  - Distraction-free, functional hierarchy designed for high readability.
- **👤 Precision Creator Profile Header**:
  - Tabular layout, verified indicator, creator headline, location tag, and numerical audience stats (subscribers, views, newsletter).
- **📱 Structured Social Directory**:
  - Accessible social buttons with sharp hairline rules and inverted hover states (YouTube, Instagram, X/Twitter, TikTok, GitHub, Discord, Spotify).
- **🗂️ Indexed Categorized Link Cards**:
  - **Category Index Markers**: Distinct typographic indices for each section.
  - **Structured Metadata**: Tag chips, category badges, external indicator glyphs (`↗`), and clean hover transitions.
  - **Highlights & Products**: Priority resources, courses, consulting services, and community channels.
- **📤 Native Share Profile API**: Instant device sharing dialog with clipboard copy fallback and accessible toast notification.
- **📬 Minimalist Newsletter Form**: Clean, distraction-free email sign-up with submit states and validation messages.
- **🌓 High-Contrast Light & Dark Themes**: Retains typographic crispness and architectural clarity across both light and dark modes.
- **📦 Type-Safe Astro Content Collections**: Structured YAML collections in `src/content/profile/alex.yml` and `src/content/links/links.yml` validated via `src/content.config.ts`.
- **🚀 Performance & Accessibility**: Zero cumulative layout shift (CLS), WCAG AA compliant contrast ratios, optimized WebP images, and OpenGraph SEO cards.

---

## 🛠️ Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **[Astro 5](https://astro.build)** | Zero-JS static site generation & type-safe content layer |
| **[Tailwind CSS v4](https://tailwindcss.com)** | Modern utility styling via `@tailwindcss/vite` |
| **[Astro SEO & Sitemap](https://github.com/jonasmerlin/astro-seo)** | Automated search engine metadata & sitemaps |
| **[Bun](https://bun.sh)** | Fast package management & build execution |

---

## 🚀 Quick Start

### Prerequisites

- [Bun](https://bun.sh) (recommended) or [Node.js](https://nodejs.org) (v18.17.0+ or v20+)
- Git

### Installation

```bash
# Clone repository
git clone https://github.com/robinsehnalik/linktree-swiss.git
cd linktree-swiss

# Install dependencies with Bun
bun install

# Or with npm / pnpm / yarn
npm install
```

### Local Development

Start the development server at `http://localhost:4321`:

```bash
bun run dev
# or npm run dev
```

### Production Build & Preview

```bash
# Build static site to /dist directory
bun run build
# or npm run build

# Preview production build locally
bun run preview
# or npm run preview
```

---

## 📂 Project Structure

```text
├── .github/workflows/       # Automated GitHub Pages CI/CD deployment
├── public/                  # Static assets (favicons, robots.txt)
├── src/
│   ├── assets/              # High-resolution optimized avatars & imagery
│   ├── components/          # Reusable Astro components
│   │   ├── BaseHead.astro   # SEO metadata, OpenGraph, font preloads
│   │   ├── Header.astro     # Minimal top bar with Share modal & theme toggle
│   │   ├── ProfileHeader.astro # Swiss-style tabular avatar, stats, bio, socials
│   │   ├── LinkCard.astro   # Hairline-bordered card with index number & arrow
│   │   ├── NewsletterCard.astro # Minimalist newsletter subscription box
│   │   └── Footer.astro     # Copyright & author attribution
│   ├── content/
│   │   ├── links/links.yml  # Link categories, titles, tags, and URLs
│   │   └── profile/alex.yml # Creator bio, stats, location, and social links
│   ├── layouts/
│   │   └── BaseLayout.astro # Core HTML shell with architectural grid lines
│   ├── pages/
│   │   └── index.astro      # Single-page creator hub entry point
│   ├── styles/
│   │   └── global.css       # Tailwind v4 styles, hairline rules & Swiss red tokens
│   ├── utils/
│   │   ├── consts.ts        # Configuration loader
│   │   └── slugify.ts       # URL & withBase helper utilities
│   ├── content.config.ts    # Type-safe Astro content schemas
│   └── site-config.yml      # Global site metadata (title, author, description)
├── .pages.yml               # Pages CMS configuration schema
├── astro.config.mjs         # Astro integrations & Vite plugins
└── package.json
```

---

## ⚙️ Configuration & Content Editing

### 1. Creator Profile (`src/content/profile/alex.yml`)
Edit your avatar, handle, verified status, headline, metrics, and social accounts:
```yaml
name: "Alex Vance"
handle: "@alexvance"
verified: true
tagline: "Design Engineer & Creative Technologist"
bio: "Building thoughtful digital products, sharing UI systems, and documenting the creator journey."
location: "San Francisco, CA"
stats:
  - label: "YouTube"
    value: "145K"
  - label: "Monthly Views"
    value: "2.4M"
  - label: "Subscribers"
    value: "32K"
```

### 2. Curated Links (`src/content/links/links.yml`)
Add, reorder, or organize links by category:
```yaml
items:
  - title: "Design Systems Masterclass 2026"
    url: "https://example.com/course"
    category: "Featured"
    highlight: true
    badge: "New Release"
    icon: "tabler:sparkles"
```

### 3. Styling & Swiss Design Tokens (`src/styles/global.css`)
Easily customize grid lines, rules, and colors:
```css
:root {
  --swiss-bg: #f4f4f4;          /* Concrete warm white */
  --swiss-surface: #ffffff;     /* Stark white */
  --swiss-ink: #111111;         /* Dense black */
  --swiss-red: #ff3300;         /* Iconic Swiss Vermillion Red */
  --swiss-border: #111111;      /* Hairline borders */
  --swiss-rule: #000000;
}
```

---

## 🚢 Deployment

### Automated GitHub Pages Deployment

This repository includes a pre-configured GitHub Actions workflow in [`.github/workflows/astro.yml`](.github/workflows/astro.yml).

1. Go to your GitHub repository settings: **Settings > Pages**.
2. Under **Build and deployment > Source**, select **GitHub Actions**.
3. Push to the `main` branch to trigger an automatic build and deployment.

### Other Hosting Providers

- **[Vercel](https://vercel.com/)**: Connect repository and deploy with the Astro preset.
- **[Netlify](https://www.netlify.com/)**: Build command `bun run build`, publish directory `dist`.
- **[Cloudflare Pages](https://pages.cloudflare.com/)**: Build command `bun run build`, output directory `dist`.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
