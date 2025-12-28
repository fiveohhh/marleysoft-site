# Marleysoft Website

Static website for Marleysoft - an embedded firmware consulting firm specializing in IoT and connected products.

## Tech Stack

- [Astro](https://astro.build) - Static site generator
- [Tailwind CSS](https://tailwindcss.com) - Utility-first CSS framework
- [Netlify](https://netlify.com) - Hosting and forms

## Getting Started

### Prerequisites

- Node.js 18.20.8, 20.3.0+, or 22.0.0+
- npm 10+

### Installation

```bash
# Install dependencies
npm install
```

### Development

```bash
# Start dev server at http://localhost:4321
npm run dev
```

### Build

```bash
# Build for production
npm run build

# Preview production build locally
npm run preview
```

## Project Structure

```
/
├── public/           # Static assets (favicon, images, etc.)
├── src/
│   ├── components/   # Reusable Astro components
│   │   ├── Header.astro
│   │   └── Footer.astro
│   ├── layouts/      # Page layouts
│   │   └── Layout.astro
│   ├── pages/        # File-based routing
│   │   ├── index.astro      # Home page
│   │   ├── services.astro   # Services page
│   │   ├── about.astro      # About page
│   │   └── contact.astro    # Contact form
│   └── styles/       # Global styles
│       └── global.css
├── astro.config.mjs  # Astro configuration
├── tailwind.config.mjs # Tailwind configuration
└── netlify.toml      # Netlify deployment settings
```

## Deployment

### Netlify Setup

1. Push this repository to GitHub/GitLab/Bitbucket
2. Log in to [Netlify](https://app.netlify.com)
3. Click "Add new site" → "Import an existing project"
4. Connect your Git repository
5. Netlify will auto-detect Astro settings:
   - Build command: `npm run build`
   - Publish directory: `dist`
6. Click "Deploy site"

### Contact Form

The contact form uses Netlify Forms:
- Works automatically once deployed to Netlify
- Free tier includes 100 form submissions/month
- Form submissions appear in Netlify dashboard under "Forms"
- No backend or additional configuration needed

## Publishing Updates

Once your site is deployed to Netlify, any changes you push to your Git repository will automatically trigger a new deployment.

### Standard Workflow

1. **Make your changes** to the code (edit content, update styles, etc.)

2. **Test locally**
   ```bash
   npm run dev
   # View at http://localhost:4321
   ```

3. **Build to verify**
   ```bash
   npm run build
   # Ensure build succeeds without errors
   ```

4. **Commit and push**
   ```bash
   git add .
   git commit -m "Description of your changes"
   git push
   ```

5. **Netlify deploys automatically**
   - Netlify detects the push and starts building
   - Build typically takes 30-60 seconds
   - Site updates automatically when build completes
   - You'll receive email notifications if build fails

### Checking Deployment Status

- Visit your Netlify dashboard: https://app.netlify.com
- Click on your site
- View "Deploys" tab to see build logs and status
- Each deploy shows commit message and build output

### Rollback if Needed

If something goes wrong:
1. Go to Netlify dashboard → Deploys
2. Find a previous successful deploy
3. Click "Publish deploy" to rollback

## Customization

### Colors

Primary color palette is defined in Tailwind classes:
- Primary: `blue-900`, `blue-800`
- Backgrounds: `gray-50`, `blue-50`, `white`
- Text: `gray-900`, `gray-700`, `gray-600`

To change colors, update Tailwind classes in components or customize `tailwind.config.mjs`.

### Content

Edit content directly in the `.astro` files:
- **Home:** `src/pages/index.astro`
- **Services:** `src/pages/services.astro`
- **About:** `src/pages/about.astro`
- **Contact:** `src/pages/contact.astro`

### Navigation

Update navigation links in:
- `src/components/Header.astro`
- `src/components/Footer.astro`

## Adding a New Page

1. Create a new file in `src/pages/`, e.g., `src/pages/blog.astro`
2. Import and use the Layout component:

```astro
---
import Layout from '../layouts/Layout.astro';
---

<Layout title="Page Title" description="Page description">
  <!-- Your content here -->
</Layout>
```

3. Add navigation link to Header and Footer components
4. The page will be available at `/blog` (file name = URL path)

## Development Notes

- Astro uses [file-based routing](https://docs.astro.build/en/core-concepts/routing/)
- Components use `.astro` format (HTML-like with frontmatter)
- Tailwind classes are applied directly in components
- Site builds to static HTML (no client-side JavaScript by default)
- Perfect for SEO and performance

## Resources

- [Astro Documentation](https://docs.astro.build)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Netlify Documentation](https://docs.netlify.com)
- [Netlify Forms](https://docs.netlify.com/forms/setup/)

## License

Private project - All rights reserved
