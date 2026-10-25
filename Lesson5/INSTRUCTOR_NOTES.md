# Lesson 5 – Example landing page with CSS Flexbox + CSS Grid — Instructor notes

**Cohort:** Group300926 (Full Stack AI Developer) · **When:** Wed 28 Oct 2026, 18:30–20:30 Stockholm (CET; 20:30 TR)
**Historical source:** `frontend-from-0/Group050626` Lesson5 (3 Jul 2026, same topic) — starter `1b87064`, completed `3eeafe0`.

## Starter (student branch `prep-lesson-5`)
- `index.html`: empty `<body>`, Google Fonts (Lato + Roboto) and `styles.css` linked.
- `styles.css`: `box-sizing` reset, body font, link reset, nav font.
- `design.png`: target design (annotated with layout boxes) — historically the screenshot was only committed after class; included up front so students can follow along.
- `assets/heart-icon.svg`, `assets/hero-img-1.svg`: images used in the page (plumbing, pre-added).
- `Lesson5/note.md` already on `main` (unchanged).

## Flow (as taught historically)
1. Look at `design.png` together; draw the boxes: header/nav, hero (text + 2×3 stats grid), image strip. Decide per box: Flexbox (1-D) or Grid (2-D).
2. Header: `nav` flex `space-between` + `align-items: center`, `max-width: 1110px; margin: auto`; `.nav-list` flex with `gap`, list reset.
3. CSS variables on `:root` (`--bg-dark`, `--text-secondary`) — recap from Lesson 4.
4. Hero: `.hero-content` flex with `gap: 80px`; `.hero-text` max-width.
5. Stats: `.hero-grid` grid `repeat(2, 1fr)` × `repeat(3, 1fr)`, `gap: 40px 78px`.
6. Nested grid in `.grid-cell` (`76px auto` columns): place icon/title/text with `grid-column`/`grid-row` — show the long-hand (`grid-column-start/end`), `1 / 2`, `1 / span 1` and `1 / -1` forms (kept as comments in the completed CSS).
7. Image strip: `.hero-images` flex; `.image-container` flex + `align-items: flex-end` to push text down, `background-image`/`background-size: contain`, rounded first/last corners.

## Completed state
See this branch: `Lesson5/index.html`, `Lesson5/styles.css`.

## Known gaps / discussion points
- Historical CSS had `grid-template-rows: repeat (3, 1fr);` (space → invalid, rule ignored; the "Anna to check how to apply repeat here" comment). Fixed in this completed version — a good live debugging moment (DevTools shows the struck-through declaration).
- All four image tiles use the same `hero-img-1.svg`; all stat icons use `heart-icon.svg` (design has different icons/colours). "Get started" button and "Purchase UI Kit" button are unstyled; no responsive styles — natural homework.

## Exercises
None prepared. Suggested homework: finish the button styles, icon colours and a simple responsive version (`flex-wrap` / single-column grid under ~768px).
