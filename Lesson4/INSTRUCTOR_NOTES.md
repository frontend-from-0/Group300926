# Lesson 4 – Building layouts with Flexbox + CSS Variables — Instructor notes

**Cohort:** Group300926 (Full Stack AI Developer, 30092026) · **When:** Wed 21 Oct 2026, 19:30–21:30 Stockholm (20:30 TR)
**Historical source:** `frontend-from-0/Group050626` Lesson4 (26 Jun 2026, identical calendar topic) — starter `2175aa5`, completed `1f87ff8`

## Starter (student branch `prep-lesson-4`)
- `index.html`: empty `<body>`, Google Fonts (Fraunces + Nunito Sans) linked, `styles.css` linked.
- `styles.css`: `box-sizing: border-box` reset + body font.
- `questions.md`: 4 Flexbox check questions (EN + TR).
- Note: the image assets (`assets/logo.svg`, `assets/hero.svg`) were only added in the historical *completed* commit — export them from the design live or share them from this branch before class.

## Flow (as built historically) — "Life Coach Reiki" landing page header + hero
1. Recap Lesson 3 (box model, typography, units, colors).
2. Introduce CSS variables: `:root { --color-black; --color-grey; --color-white; --color-bg }` and `var(--…)`; use for body background, text and buttons.
3. Build the top nav with Flexbox: `.nav-top { display:flex; justify-content: space-between; align-items:center; }`, logo link + two `ul.menu-list` (links / buttons).
4. Small utility classes: `.flex`, `.gap-48`, `.gap-16`, `.justify-center` — discuss utility vs component classes (preview of Tailwind later).
5. Buttons: `.btn`, `.btn-outlined`, `.btn-filled` with `:hover` swaps using variables.
6. Hero section: `.badge`, `h1` (Fraunces, 72px/82px, `max-width` + `margin:auto`), paragraph, centered button row, hero image (`img { width:100% }`).
7. Go through `questions.md` together (`display:flex` effect on children, `justify-content` vs `align-items`, `flex-direction: column`, block vs flex on same element).

## Completed state
See this branch: `Lesson4/index.html`, `Lesson4/styles.css`, `Lesson4/assets/` (logo + hero SVG). `.badge` rule is left empty in the historical code (finish live or as homework).

## Homework context
Classroom items due 21 Oct for this cohort: freeCodeCamp CSS Box Model (Rothko), Colors (markers), Typography (Nutrition Label), "Designing Content" video, Refactoring UI ebook. No repo-based exercise needed.

Next lesson (historical Group050626 Lesson5): example landing page with Flexbox + CSS Grid.
