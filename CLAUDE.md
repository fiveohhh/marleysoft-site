# CLAUDE.md - AI Assistant Guide

## Project Overview

This is the Marleysoft consulting website - a static site for an embedded firmware consulting business specializing in IoT and connected products.

## Tech Stack

- **Framework:** Astro 5.x (static site generator)
- **Styling:** Tailwind CSS 4.x (via @tailwindcss/vite)
- **Deployment:** Netlify (free tier)
- **Forms:** Netlify Forms (no backend needed)

## Project Structure

```
/home/andy/gitRepos/marleysoft-site/
├── src/
│   ├── layouts/
│   │   └── Layout.astro          # Base layout with Header/Footer
│   ├── components/
│   │   ├── Header.astro          # Navigation header
│   │   └── Footer.astro          # Site footer
│   ├── pages/
│   │   ├── index.astro           # Home page
│   │   ├── services.astro        # Services page
│   │   ├── about.astro           # About page
│   │   └── contact.astro         # Contact form page
│   └── styles/
│       └── global.css            # Global styles (Tailwind imports)
├── public/
│   └── favicon.svg               # Site favicon
├── astro.config.mjs              # Astro configuration
├── tailwind.config.mjs           # Tailwind configuration
├── netlify.toml                  # Netlify deployment config
└── package.json                  # Dependencies
```

## Key Business Context

**Company:** Marleysoft (solo consultant)
**Focus:** IoT and connected products (but not limited to)
**Experience:** 15+ years across medical, industrial, and consumer electronics

**Core Value Proposition:**
- Firmware architecture and development infrastructure - not just writing code
- Team integration - works alongside client teams, not as a black-box consultant
- Testing infrastructure, CI/CD, and developer experience optimization

**Voice & Tone:**
- Use "Marleysoft" as the brand
- Use "I" for personal/about content
- Neutral/passive voice for service descriptions
- Professional but approachable

## Content Guidelines

### Primary Differentiators (keep these central):
1. **Architecture First** - System design over quick implementation
2. **Testing Infrastructure** - Host-side and hardware-in-the-loop testing
3. **CI/CD Pipelines** - Build systems and release management
4. **Developer Experience** - Tooling and workflow optimization
5. **Team Integration** - Embedded in client teams (standups, workflows, daily collaboration)

### Service Categories:
1. Firmware Architecture & Development
2. Testing Infrastructure
3. Development Infrastructure
4. Developer Experience

### Industries:
- Medical devices
- Industrial systems
- Consumer electronics

## Common Modifications

### Adding a New Page
1. Create `src/pages/pagename.astro`
2. Import and use the `Layout` component
3. Update navigation in `src/components/Header.astro` and `src/components/Footer.astro`

### Updating Copy
- Home page hero: `src/pages/index.astro` (lines 10-30)
- Services: `src/pages/services.astro`
- About: `src/pages/about.astro`
- Contact: `src/pages/contact.astro`

### Styling Changes
- Global styles: `src/styles/global.css`
- Tailwind config: `tailwind.config.mjs`
- Color scheme uses blue-900/blue-800 for primary, gray for text

### Contact Form
- Form is in `src/pages/contact.astro`
- Uses Netlify Forms (requires deployment to Netlify to work)
- Fields: name, email, company (optional), message
- Includes honeypot spam protection

## Development Commands

```bash
npm run dev          # Start dev server (localhost:4321)
npm run build        # Build for production (outputs to dist/)
npm run preview      # Preview production build locally
```

## Deployment

The site is configured for Netlify:
- Push to Git repository
- Connect repo to Netlify
- Netlify auto-detects Astro and uses settings from `netlify.toml`
- Build command: `npm run build`
- Publish directory: `dist`

## Important Notes

- **Solo practice:** The consultant works alone, so avoid "team" or "we" language except for "Marleysoft" brand references
- **No case studies yet:** Content is kept general; specific projects can be added later
- **No branding assets:** Currently uses clean blue/gray palette; no logo yet
- **Team integration is KEY:** This differentiator should be visible on home page and emphasized throughout
- **Not just code:** Emphasize architecture, infrastructure, and process over implementation

## Maintenance Tips

- Keep copy focused on architecture and infrastructure value
- Maintain professional but approachable tone
- Ensure team integration messaging stays prominent
- When adding content, follow the pattern of neutral/passive voice for services, "I" for personal sections
