# Rizky Sulaeman — Portfolio (Static)

Modern, responsive, accessible portfolio to showcase profile, experience, and projects. Built with Tailwind CSS (CDN) + Alpine.js (CDN). No build step required.

## Tech Stack
- Tailwind CSS (latest) via CDN
- Alpine.js (latest) via CDN (+ Intersect plugin for entrance animations)
- HTML5 + vanilla JS (minimal)

## Structure
```
CV RISKI/
├─ index.html              # Main single-page site (Home, About, Projects, Resume, Contact)
├─ resume.html             # Print-friendly resume page (export to PDF)
├─ assets/
│  ├─ profile.svg          # Avatar placeholder (replace with your photo .webp)
│  ├─ project-placeholder.svg
│  └─ resume.pdf           # (Optional) Exported PDF after printing resume.html
└─ README.md
```

## Run locally
No tooling needed. Open `index.html` in a modern browser.
- Windows: double click `index.html`
- Or serve with any static server (optional):
  - Python: `python -m http.server 8080`
  - Node: `npx serve .`

## Deployment
Any static host works:
- Vercel: import the folder and deploy
- Netlify: drag-and-drop or link repo
- GitHub Pages: push repo and enable Pages

## Replace content
- Images: Put optimized `.webp` in `assets/` and update `src` in `index.html`.
- Contact form: Replace `https://formspree.io/f/your-id` with your Formspree endpoint. Alternatively use Netlify Forms by adding `netlify` on the `<form>`.
- Social links: Add your LinkedIn/GitHub URLs in the JSON‑LD (`index.html`) and footer if desired.

## Resume (PDF)
1. Open `resume.html` in the browser.
2. File → Print → Destination: “Save as PDF”.
3. Save as `assets/resume.pdf`. The “Download PDF” button hides automatically if the file is missing.

## Accessibility & SEO
- Semantic HTML, labeled controls, keyboard navigation, visible focus styles.
- High contrast color palette; alt text on images.
- Skip link provided; modals are dismissible (Esc key or close button).
- SEO meta tags (title, description, OpenGraph, Twitter) and Person JSON‑LD.

## Performance tips
- Replace SVG placeholders with compressed `.webp` images. `loading="lazy"` is used on images.
- Keep animations lightweight; prefer CSS/transition based.
- Lighthouse targets: Accessibility ≥ 90, Best Practices ≥ 90, SEO ≥ 90.

## Browser support
- Tested on latest Chrome, Firefox, Edge, and Safari.
- Responsive across sm, md, lg, xl breakpoints.

## Notes on personal data
- Only non-sensitive information from the provided CV is displayed by default (city & masked phone). If you wish to publish additional details, edit the About section consciously.

## CDN versions
- Tailwind CSS: `https://cdn.tailwindcss.com`
- Alpine.js: `https://unpkg.com/alpinejs@3.x.x`
- Alpine Intersect: `https://unpkg.com/@alpinejs/intersect@3.x.x`

---
If you need a live demo link, deploy to Vercel or Netlify and share the URL.
