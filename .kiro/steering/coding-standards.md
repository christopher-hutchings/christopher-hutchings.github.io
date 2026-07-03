# Coding Standards

## General Rules
- No build tools or bundlers — all files are served as-is by GitHub Pages
- Keep the site fully static; no server-side logic
- Use Tailwind CSS utility classes via CDN for layout and spacing
- Use `styles.css` for brand-specific styles and reusable custom classes
- Vanilla JavaScript only — no frameworks or libraries beyond Tailwind CDN
- All pages must be valid HTML5 with `lang="en"`

## File Structure
- HTML pages live at the project root (flat structure, no subdirectories for pages)
- Images go in the `/images/` directory
- Single shared stylesheet: `styles.css`
- No separate JS files — inline scripts only, kept minimal

## HTML Conventions
- Use semantic HTML elements (`<header>`, `<nav>`, `<section>`, `<footer>`, `<main>`)
- Every page must include the full `<head>` block with meta description, Open Graph tags, canonical URL, and favicon links
- Use `loading="lazy"` on images below the fold
- Navigation links use relative paths (e.g. `href="about.html"`)
- Logo image path uses `../images/logo_new.png` (relative from root)

## CSS / Tailwind
- Tailwind is loaded from CDN — do not install it locally or add a config file
- Brand colours are defined as CSS custom properties in `styles.css`:
  - `--my-brand-color: #129bba` (primary blue/teal)
  - `--my-brand-hover-color: #0a6a80` (darker hover state)
  - `#2dada4` (green accent, used for banners and buttons)
- Custom classes: `.brand`, `.link-brand`, `.logo`, `.current_page`, `.background-container`
- Prefer Tailwind utilities for one-off spacing/layout; use custom classes for repeated brand styling
- Responsive breakpoints follow Tailwind defaults (`sm:`, `md:`, `lg:`)

## JavaScript
- Only vanilla JS, inlined in a `<script>` tag after the header
- Current JS is limited to mobile menu toggle — keep it that way unless a feature explicitly requires more
- No external JS libraries

## Images
- Use descriptive alt text on all images
- Prefer `.jpg` for photos, `.png` for logos with transparency, `.svg` for vector graphics
- Keep image file sizes reasonable for page load speed

## Forms
- Contact form submits to FormSubmit.co via POST
- Include honeypot field (`name="_honey"`) for spam protection
- Use proper `<label>` elements linked to inputs via `for`/`id`

## Deployment
- Push to `main` branch to deploy via GitHub Pages
- Custom domain is configured via `CNAME` file (do not modify)
- No CI/CD pipeline — deployment is automatic on push
