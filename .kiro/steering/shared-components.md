# Shared Components

This site does not use a templating engine. The header, footer, mobile menu script, and maternity banner are manually duplicated across all pages. When modifying any shared component, **update all 5 HTML files** to keep them in sync.

## Pages to Update
1. `index.html`
2. `about.html`
3. `amatsu.html`
4. `appointments.html`
5. `contact.html`

---

## Maternity Leave Banner
Appears at the very top of `<body>`, before the header. Teal background (`bg-[#2dada4]`), white text, centred.

```html
<div class="bg-[#2dada4] text-white text-center px-4 py-3 text-sm sm:text-base">
  <strong>Maternity Leave Notice:</strong>
  I am currently on maternity leave and will be returning in <strong>November 2026</strong>.
  Thank you for your understanding 💛
</div>
```

Remove this banner when Hannah returns from maternity leave.

---

## Header & Navigation
Sticky header with logo (left), site title (centred), and navigation (right). Includes a responsive hamburger menu for mobile.

Key elements:
- Logo links to `index.html`
- Desktop nav: visible at `md:` breakpoint and above
- Mobile nav: hidden by default, toggled by hamburger button
- Site title uses `.brand` class with the "aesthet nova" font

Navigation links (in order):
1. Home → `index.html`
2. About → `about.html`
3. What is Amatsu → `amatsu.html`
4. Appointments → `appointments.html`
5. Contact → `contact.html`

---

## Mobile Menu Toggle Script
Placed immediately after the `</header>` closing tag on every page:

```html
<script>
  const toggle = document.getElementById('menu-toggle');
  const menu = document.getElementById('mobile-menu');
  toggle.addEventListener('click', () => {
    menu.classList.toggle('hidden');
  });
</script>
```

---

## Footer
Consistent across all pages. Three-column layout on desktop, stacked on mobile:
- **Left:** Email link (`hannah@rebalanceamatsu.co.uk`)
- **Centre:** Social media icons (Instagram, Facebook, Twitter/X, LinkedIn)
- **Right:** Phone number (`07894 276 779`)
- **Bottom row:** Copyright notice

Social links:
- Instagram: `https://www.instagram.com/hbtherapies`
- Facebook: `https://www.facebook.com/share/1FtspKrQrh/`
- Twitter/X: `https://x.com/hcboot`
- LinkedIn: `https://uk.linkedin.com/in/hannah-boot-79a73540`

---

## Content Section Pattern
Each page wraps its main content in a section with the `.background-container` class, which applies a semi-transparent background image overlay:

```html
<section class="py-0 bg-white text-center">
  <div class="background-container">
    <div class="container mx-auto px-4">
      <!-- Page-specific content -->
    </div>
  </div>
</section>
```
