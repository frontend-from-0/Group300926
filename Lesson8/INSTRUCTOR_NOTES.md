# Lesson 8 – Responsive web design — Instructor notes

**Cohort:** Group300926 (Full Stack Developer) · **When:** Wed 25 Nov 2026, 18:30–20:30 Stockholm (CET; 20:30 TR)
**Historical source:** `frontend-from-0/Group050626` Lesson8 (Mon 3 Aug 2026, "Responsive web design", same course) — starter `9088802` (18:38 CEST), completed `ed156e8` (21:39 CEST).

## Starter (student branch `prep-lesson-8`) — identical to the historical starter
- `note.md`: Responsive Web Dev Cheatsheet — mobile-first, Flexbox vs Grid, `clamp()` / fluid units, `dvh`/`svh`/`lvh`, responsive images (`srcset` / `sizes` / `picture`), image formats, logical properties.
- `index.html`: empty `<body>`, viewport meta, only `styles.css` linked.
- `styles.css`: reset/base only (box-sizing, body padding 16px, list reset, link styles, fluid images).
- `assets/`: logo, hamburger / play / briefcase icons, hero images (PNG + WebP, sm + md).
- No plumbing needed (static HTML/CSS, open with Live Server).

## Flow (as taught historically)
1. Theory from `note.md` (mobile-first, breakpoints, responsive images, viewport units, logical properties).
2. Build the Travlog header + hero, starting from the small-screen layout:
   - SM: hamburger + logo. Nav uses `flex-direction: row-reverse` so the logo appears on the left and the hamburger on the right, while the hamburger stays first in the DOM. Hide `.nav-list` and `.nav-actions`. Hero is `flex-direction: column-reverse` (image above text).
   - MD (768px–1023.98px): show Log In / Sign Up (`.nav-actions`), switch nav to `flex-direction: row` (hamburger, logo, actions). Body padding 64px.
   - LG (≥1024px): hide the hamburger, show the nav links, hero becomes a row (text + image).
3. Styles were split into separate files with `media` on the `<link>` tags (`md.css`, `lg.css`) rather than `@media` blocks in `styles.css` (those are left commented in the completed `styles.css` as an alternative).
4. Add a responsive hero image (`srcset` / WebP). The completed markup is unfinished: `src` is the PNG, `srcset` lists two WebPs without width descriptors or `sizes`, and the alt text still says "TO BE UPDATED". Useful live demo of why `srcset` needs width descriptors.

## Completed state
See this branch: `Lesson8/index.html`, `styles.css`, `md.css`, `lg.css` (= historical completed code).
`note.md` is unchanged from the starter (the historical completed commit only added two blank lines at the top).

## Notes / possible homework
- In-class HTML comments keep the typo "login/singup" and "Nav elmentleri" (Turkish for "nav elements") — left as-is.
- `:root {}` is empty; `.nav-hamburger:hover` is commented; the "Watch Demo" control is a `<button href="">` (invalid `href` on a button).
- Historical Classroom homework (10 Aug 2026): finish the portion shown on the assignment screenshot so it works on mobile, tablet and laptop; reading guides on responsive design and responsive images; FreeCodeCamp "Learn Responsive Web Design by Building a Piano".
No exercises repo homework starter in the historical source.
