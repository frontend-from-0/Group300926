# Lesson 6 – Example dashboard layout with CSS Grid — Instructor notes

**Cohort:** Group300926 (Full Stack Developer) · **When:** Wed 4 Nov 2026, 18:30–20:30 Stockholm (CET; 20:30 TR)
**Historical source:** `frontend-from-0/Group050626` Lesson6 (10 Jul 2026, "building an example layout using CSS Grid", same course) — completed `0858f7f`. There was **no starter commit** historically: the whole page was built from scratch in class.

## Starter (student branch `prep-lesson-6`)
- `index.html`: boilerplate, `styles.css` linked, empty `<body>`.
- `styles.css`: `box-sizing: border-box` reset, `body { margin: 0 }`.
- `task.md` (new): ASCII sketch of the target layout (outer 3-column page grid + inner 4-column card grid) and the list of Grid features practised — replaces a design image (none exists in the historical repo).

## Flow (as taught historically)
1. Markup: `<main>` with `nav.sidebar-left-container`, `div.controls-container`, `header.page-header` (h1 "Overview"), `div.main-container` (cards: Views, Visits, New Users, Active Users; sections: Total Users, Traffic by Website, Traffic by Device, Traffic by Location, Marketing & SEO), `aside.sidebar-right-container`. Temporary background colours to see the areas.
2. Outer grid on `main`: `min-height: 100vh`; `grid-template-columns: [page-start] minmax(200px, 250px) [main-start] auto [main-end] minmax(250px, 300px) [page-end]`; `grid-template-rows: 68px 120px auto`.
3. Place areas three ways (the first two are kept as comments in the completed CSS):
   - line numbers: `grid-column: 1 / span 1; grid-row: 1 / -1`
   - named lines: `grid-column: page-start / main-start`
   - `grid-template-areas` + `grid-area` (final version).
4. Nested grid on `.main-container`: `grid-template-columns: 1fr 1fr 1fr 1fr` (good moment for `repeat(4, 1fr)`), rows `112px 330px 280px 280px`.
5. Card placement: `.card-1..4` one column each; `.total-users` `1 / span 3`; `.website-traffic` `4 / span 1`; `.start-span-2` `1 / span 2`; `.middle-span-2` `3 / span 2`; `.row` `1 / -1`.

## Completed state
See this branch: `Lesson6/index.html`, `Lesson6/styles.css` (identical to the historical completed code, only the `<title>` changed).

## Discussion points / possible homework
- No `gap` yet — add `gap` and padding to the inner grid.
- Replace `1fr 1fr 1fr 1fr` with `repeat(4, 1fr)`; class names `start-span-2`/`middle-span-2`/`row` are layout-based — discuss semantic naming.
- Responsive: collapse the sidebars / change `grid-template-areas` in a media query.
- Card content/styling (Lesson 5 Flexbox skills) inside each card.
No exercises prepared (no homework in the historical source).
