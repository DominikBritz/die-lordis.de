# die-lordis.de

## Project Overview

Static website for "Die Lordis," a German brass band (Blasmusik) from the Wipperfürth/Kürten area. The site showcases the band, lists upcoming events, displays band members, and provides contact information.

## Tech Stack

- **HTML5** — static pages, no build system or backend
- **Bootstrap 5.2.3** — responsive grid, navbar, carousel, utilities (minified CSS + JS in `src/`)
- **Font Awesome 6.x** — icons (solid, brands, regular; minified JS in `src/`)
- **Custom CSS** — `src/my.css` for dark theme and responsive overrides
- **Images** — WebP format for photos, PNG for logos

No package.json, no bundler, no Node.js. Purely static files.

## File Structure

```
├── index.html              # Main page (band info, events, member carousel)
├── impressum.html          # Legal page (required by German law, §5 TMG)
├── src/
│   ├── bootstrap.min.css   # Bootstrap 5.2.3
│   ├── bootstrap.min.js    # Bootstrap 5.2.3
│   ├── my.css              # Custom dark theme + responsive styles
│   ├── fontawesome.min.js  # Font Awesome core
│   ├── solid.min.js        # FA solid icons
│   ├── brands.min.js       # FA brand icons
│   └── regular.min.js      # FA regular icons
├── images/
│   ├── favicon.png
│   ├── logo.png
│   ├── lordis_logo_transparent_500x500.png
│   └── photos/             # Band member photos (WebP) + group shots
└── claude.md               # This file
```

## Pages & Sections

### index.html
1. **Navbar** — responsive (navbar-expand-sm), links to Home, Instagram (@die_lordis), Impressum
2. **Logo** — centered band logo
3. **Band photo** — group shot (VorDerKirche960.webp)
4. **About** — band history, music style (Egerländer, polkas, waltzes, modern)
5. **Contact CTA** — mailto button to info@die-lordis.de
6. **Termine (Events)** — HTML table with upcoming gigs (dates, event names, locations)
7. **Musiker (Musicians)** — Bootstrap carousel with 8 members and their instruments
8. **Footer** — copyright, email contact

### impressum.html
- Legal contact details (Dominik Britz)
- Liability disclaimers, copyright, data privacy
- Same navbar and footer as index.html

## Styling & Theme

Dark theme defined via CSS custom properties in `src/my.css`:
- Background: `#121212`, text: `#eee`
- Primary color: `#52796F` (sage green), secondary: `#36514a`
- Container max-width: `960px`
- Responsive breakpoints: mobile (<768px), tablet (768–992px), desktop (≥992px)
- Custom `.btn-custom-primary` button style
- Carousel captions with semi-transparent background

## Deployment

- **Hosting**: GitHub Pages (repo: `DominikBritz/die-lordis.de`)
- **Branch**: `main`
- No build step — push HTML/CSS/JS directly

## External Services

- **Instagram**: link to @die_lordis profile
- **Email**: info@die-lordis.de (primary), dominik.britz+lordis@gmail.com (impressum)
- No analytics, no tracking, no external APIs

## Conventions

- Bootstrap utility classes for spacing/layout (e.g. `pt-5`, `pb-2`, `text-center`)
- Font Awesome icons via `<i class="fa-solid fa-...">` tags
- German-language content throughout
- Images optimized as WebP; logos as PNG
- Git commits track content updates (primarily event/Termine changes)
