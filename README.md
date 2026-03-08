# Cohorts — Retreat OS Website

## Quick Start

### Prerequisites
- Node.js 16+ (https://nodejs.org)
- npm 8+ (comes with Node)

### Install & Run

```bash
# 1. Navigate into the project folder
cd cohorts

# 2. Install dependencies
npm install

# 3. Start the development server
npm start
```

The app will open at **http://localhost:3000**

---

### Production Build

```bash
npm run build
```

This creates an optimised production build in the `/build` folder ready to deploy to any static host (Vercel, Netlify, S3, etc.).

---

### Deploy to Vercel (recommended)

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy from project root
vercel
```

### Deploy to Netlify

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Build first
npm run build

# Deploy
netlify deploy --prod --dir=build
```

---

## Project Structure

```
cohorts/
├── public/
│   └── index.html          # HTML shell
├── src/
│   ├── index.js            # React entry point
│   ├── App.jsx             # Full website (all pages, routing)
│   └── siteConfig.js       # ← SINGLE SOURCE OF TRUTH for all data
├── package.json
└── README.md
```

## Customising Content

**All content lives in `src/siteConfig.js`** — edit this file to change:
- Brand name, tagline, CTA labels
- Pricing plans and amounts
- Platform modules
- Solutions
- Retreat types
- Locations
- Testimonials, stats, blog posts, guides

The website reads everything from this file. You never need to touch `App.jsx` for content changes.

---

## Pages & Routes (internal SPA routing)

| Page key | URL equivalent | Description |
|---|---|---|
| `home` | / | Homepage |
| `platform` | /platform | Platform overview |
| `platform-{id}` | /platform/{module} | Individual module pages (8) |
| `solutions` | /solutions | Solutions overview |
| `solution-{id}` | /solutions/{solution} | Individual solution pages (6) |
| `pricing` | /pricing | Pricing page |
| `locations` | /locations | Locations overview |
| `location-{id}` | /locations/{location} | Individual location pages (10) |
| `retreat-types` | /retreat-types | All retreat type software pages |
| `seo-{typeId}-{locationId}` | /{type}/{location} | SEO matrix pages (100) |
| `case-studies` | /case-studies | Case studies |
| `resources` / `blog` | /resources | Blog & resources |
| `about` | /about | About page |
| `contact` | /contact | Book simulation / contact |
