# SEO & Accessibility Guidelines

## SEO

### Meta Tags (required on every page)
- `<meta name="description" content="...">` — unique per page, under 160 characters
- `<link rel="canonical" href="https://rebalanceamatsu.co.uk/...">` — full canonical URL
- Open Graph tags: `og:title`, `og:description`, `og:url`, `og:image`
- Twitter card: at minimum `twitter:card` set to `summary_large_image` (homepage has this; other pages can add it)

### Structure
- One `<h1>` per page (currently the site name in the header)
- Use `<h2>`–`<h4>` for content hierarchy — do not skip levels
- Use descriptive, keyword-rich page `<title>` tags (format: "Page Topic | Rebalance Amatsu with Hannah")

### Images
- Always include meaningful `alt` text describing the image content
- Use `loading="lazy"` on images that are not in the initial viewport

### Links
- Use descriptive link text (avoid "click here")
- External links should use `target="_blank"` with appropriate context
- Internal navigation uses relative paths

### Performance
- Tailwind CDN is the only external script — keep it that way
- No render-blocking custom JS
- Optimise image file sizes before adding to `/images/`

## Accessibility

### Keyboard & Focus
- All interactive elements (links, buttons, form inputs) must be keyboard-accessible
- The hamburger menu button includes `aria-label="Toggle menu"`

### Semantic HTML
- Use `<nav>` for navigation, `<header>`, `<footer>`, `<section>`, `<main>`
- Form inputs must have associated `<label>` elements with matching `for`/`id`
- Use `<button>` for interactive controls, not `<div>` or `<span>`

### Colour Contrast
- Body text (`text-gray-800` on white) meets WCAG AA contrast requirements
- Brand colour links (`#129bba` on white) — verify contrast ratio is at least 4.5:1 for normal text
- Banner text (white on `#2dada4`) — verify contrast for readability
- Button text (white on `#2dada4`) — verify contrast ratio

### Images
- Decorative images should use `alt=""` (empty alt)
- Informative images need descriptive alt text
- Logo images should describe the brand (e.g. "Rebalance Amatsu logo")

### Responsive Design
- Site must be usable on mobile (320px+), tablet, and desktop
- Touch targets should be at least 44×44px
- Text should remain readable without horizontal scrolling on mobile
