# Aybala Ören Dental Clinic – Website

A single-page, responsive website I built for Aybala Ören Dental Clinic in Kozan, Adana, Türkiye. The site content is in Turkish.

I didn't use any framework, build tool or JavaScript library. The site is written in plain HTML5, CSS3 and vanilla JavaScript and served as static files.

## Features

- **Responsive design:** separate layouts for desktop, tablet and mobile using `@media` queries (breakpoints at 1000px and 820px)
- **Mobile menu:** below 820px the navigation collapses into a hamburger menu that opens a full-screen overlay, toggled with JavaScript
- **Fixed navigation:** the top bar gets a darker background once the page is scrolled (`scroll` event listener)
- **Smooth in-page navigation:** `scroll-behavior: smooth`, plus `scroll-margin-top` so the fixed header doesn't cover section headings
- **WhatsApp integration:** a fixed appointment button linking to `wa.me`
- **Click-to-call:** a `tel:` link that starts a call directly on mobile
- **Map link:** the address opens in Google Maps through a search URL
- **Performance:** `loading="lazy"` on off-screen images; all images resized for the web
- **SEO basics:** `lang="tr"`, a meta description, a meaningful heading hierarchy and `alt` text on every image
- **Accessibility:** `aria-label` on icon-only buttons, `aria-hidden` on decorative SVGs

## Page Structure

| Section | Content |
|---|---|
| Hero | Full-screen image, gradient overlay, headline and CTA |
| Services | General, cosmetic and pediatric dentistry (inline SVG icons) |
| Treatments | Root canal, fillings, whitening, extraction, zirconia crowns |
| Gallery | 4-column CSS Grid (2 columns on mobile) |
| About | Dentist biography, education, courses and congresses |
| Appointment (CTA) | WhatsApp redirect |
| Contact | Address, phone, opening hours |

## Tech Stack

- **HTML5:** semantic elements (`header`, `nav`, `section`, `footer`)
- **CSS3:** custom properties, Flexbox, CSS Grid, fluid typography with `clamp()`, `aspect-ratio`, `object-fit`
- **JavaScript (vanilla):** menu and scroll behavior
- **Google Fonts:** Cormorant Garamond (headings), Jost (body text)
- **Images:** royalty-free photos under the Unsplash License
- **Hosting:** Netlify (static deploy)

## File Structure

```
├── index.html      # Page structure and content
├── style.css       # Styles, color variables and responsive rules
├── images/         # Optimized images
└── README.md
```

## Running Locally

No installation needed: opening `index.html` in a browser is enough. You can also serve it with a simple local server:

```bash
python3 -m http.server 5500
```

Then open `http://localhost:5500` in your browser.

## Deployment

The site is currently live on Netlify under a `*.netlify.app` subdomain. Updates go live by redeploying the files to Netlify.

## Project Status & Next Steps

- [ ] **Custom domain:** buy a domain for the site and connect it to Netlify (DNS settings + automatic SSL). **Waiting for the site owner's approval.** The clinic is still under construction, so the domain will be purchased once construction is finished.
- [ ] Replace the Unsplash photos with the clinic's own photos
- [ ] Link the site to the clinic's Google Business Profile and Google Maps location
- [x] Complete all content sections
- [x] Mobile responsiveness
- [x] WhatsApp and phone integration
