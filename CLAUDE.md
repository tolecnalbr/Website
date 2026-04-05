# Lancelot — Personal Website & AI Learning Blog

## Project Overview

Lancelot is a personal website and blog where Lancelot documents their AI learning journey. The site features regular blog posts (daily/weekly updates) about what they've learned, what they've built, and insights along the way.

## Tech Stack

- **Framework:** Astro v5 (static site generator) — requires Node 20+
- **Content:** Markdown files for blog posts (option to add a visual CMS like Decap/Tina later). JSON files for recommendations.
- **Styling:** CSS with custom properties (light/cream theme)
- **Animations:** CSS keyframes + vanilla JS for farmer intro animation
- **Hosting:** GitHub Pages (auto-deploys on push via GitHub Actions)
- **Package manager:** npm
- **Base URL:** `/Website/` — all internal links must use `import.meta.env.BASE_URL`

## Site Structure

### Pages

- **Landing page** (`/`) — Farmer intro animation, personal greeting with name highlighted in blue, latest blog posts section.
- **Blog** (`/blog`) — List of posts (daily/weekly AI learning updates), written in Markdown. Individual posts show reading time, prev/next navigation.
- **About** (`/about`) — About Lancelot.
- **Questions** (`/questions`) — Contact info (email, LinkedIn) + FAQ-style general information.
- **Recommendations** (`/recommendations`) — Books, movies, and quotes with ratings, status badges, and optional comments. Data stored in JSON files at `src/content/recommendations/`.
- **404** — Custom error page.
- **RSS** (`/rss.xml`) — Auto-generated feed from blog posts.

### Navigation

Simple horizontal top nav: Home, Blog, About, Questions, Recommendations.

### Social Links

- LinkedIn: https://www.linkedin.com/in/lancelotbrun/
- Email: lancelot.brun@gmail.com

## Design Principles

- **Aesthetic:** Minimalist, clean, no clutter. Inspired by arvid.xyz and lovefrom.com.
- **Color:** Light/cream background (`#fafafa`), dark text (`#1a1a1a`), blue accent (`#4466AA`).
- **Typography:** Inter font with system font fallbacks.
- **Tone:** Personal, approachable, informal.
- **Intro animation:** A pixel art farmer (hay hat, blue overalls, yellow shirt, pickaxe) walks in from the right with animated legs, stops at center, digs twice — cracks appear at impact point, then the screen shatters and the farmer falls through, revealing the homepage. Plays once per browser session.

## SEO

- Semantic HTML (`<header>`, `<main>`, `<article>`, `<nav>`, etc.)
- Meta tags on every page (title, description, Open Graph, Twitter cards)
- JSON-LD structured data (Person, WebSite, BlogPosting schemas)
- Auto-generated sitemap.xml and RSS feed
- robots.txt
- Clean URL structure (e.g., `/blog/my-post-title`)
- Image alt texts on all images
- Skip-to-content link for accessibility
- Fast load times (static output)
- Mobile responsive design

## Commands

- `npm run dev` — Start local development server (site at `http://localhost:4321/Website/`)
- `npm run build` — Build the site for production
- `npm run preview` — Preview the production build locally

## Deployment

- **GitHub repo:** tolecnalbr/Website
- **Live URL:** https://tolecnalbr.github.io/Website/
- Push to `main` branch triggers auto-deploy via GitHub Actions

## Working with Lancelot

- **Experience level:** New to web development — no prior experience building websites.
- Explain technical concepts clearly when they come up.
- Suggest options rather than assuming preferences.
- Keep things simple — avoid unnecessary complexity.
- When making changes, explain what was done and why.
- Lancelot will provide resources and inspiration over time — integrate them as they come.

## Future Features

- **Screen Time Dashboard** — Pull Apple Screen Time data daily, display as graphs on the site.
- **Visual CMS** — Add Decap/Tina CMS for writing blog posts in a browser editor.
