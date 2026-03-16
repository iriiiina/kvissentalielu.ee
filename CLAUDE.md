# CLAUDE.md — Kvissentali Elu MTÜ Website

## Project Overview

Static website for **Kvissentali Elu MTÜ**, a neighborhood association in Tartu, Estonia.
Live at **https://kvissentalielu.ee**, deployed via GitHub Pages.

## Tech Stack

- **Pure HTML5 + CSS3** — no JavaScript, no frameworks, no build tools
- **No package.json** — nothing to install or build
- **Deployment:** push to `main` → GitHub Pages serves it (CNAME: `kvissentalielu.ee`)
- **Font:** Raleway (TTF files bundled in `style/`)

## File Structure

```
index.html          — Homepage with 6 category cards
about.html          — Organization info, statute, reports
join.html           — Membership information
projects.html       — Active and completed projects
people.html         — Board members
day.html            — Kvissentali Day annual event
kvissentali.html    — Neighborhood history/info

style/
  common.css        — Shared styles, fonts, footer
  index.css         — Homepage-specific (logo animation, cards)
  category.css      — All content pages (nav, header, layout, responsive)

images/             — All visual assets (favicon/, projects/, people/, icons/)
documents/          — PDFs (statute, annual reports, board meeting minutes)
media-kit/          — Brand assets in various sizes and colors
old/                — Archived content
AI/                 — Context files for AI assistants
```

## Key Conventions

- **Language:** All content is in Estonian (lang="et-EE")
- **HTML structure:** Every page uses `<header>`, `<nav>`, `<main>`, `<footer>` with consistent layout
- **SEO:** Schema.org microdata embedded in HTML, Open Graph meta tags, sitemap.xml, robots.txt
- **CSS approach:** Flexbox layout, ID-based selectors for page sections, class-based for reusable components
- **Color palette:** Dark green `#023020`, yellow `#FFC300`, plus 6 accent colors (`#84a98c`, `#e3b23c`, `#a4969b`, `#655560`, `#50858b`, `#c1666b`)
- **Responsive breakpoints:** 500px, 1000px, 1500px
- **External links:** Use `target="_blank"` with arrow symbol (&#10138;)
- **Navigation:** 7 pages linked in every page's nav + footer
- **Commit style:** Short descriptive messages, often referencing what changed

## Git Policy

**Do NOT run any git commands that modify state.** No `git add`, `commit`, `push`, `pull`, `fetch`, `merge`, `rebase`, `checkout`, `reset`, `stash`, or `branch`. Only read-only commands are allowed: `git status`, `git diff`, `git log`, `git show`, `git blame`, etc.

## When Editing

- Edit HTML files directly — there is no templating or build step
- Keep Schema.org microdata consistent when modifying page structure
- Update `sitemap.xml` lastmod dates when pages change
- Maintain the consistent header/nav/footer across all pages
- Test responsiveness — layouts use flexbox with media queries
- Logo uses CSS `@keyframes` color animation cycling through 6 accent colors
