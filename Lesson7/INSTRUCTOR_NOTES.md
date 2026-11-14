# Lesson 7 – Accessibility — Instructor notes

**Cohort:** Group300926 (Full Stack Developer) · **When:** Wed 18 Nov 2026, 18:30–20:30 Stockholm (CET; 20:30 TR)
**Historical source:** `frontend-from-0/Group050626` Lesson7 (Mon 27 Jul 2026, "Web Accessibility", same course) — starter `2e6b8a3` (18:22 CEST), completed `c29f725` (21:15 CEST).

## Starter (student branch `prep-lesson-7`) — identical to the historical starter
- `a11y.md`: why accessibility matters, WCAG + POUR principles, additional resources, best practices, `role` attribute, ARIA (when to use / not to use).
- `index.html`: "wellness club" page built with only `<div>`/`<span>` (BEM classes) and deliberate a11y problems: no landmarks, `<span>` page title, icon-only home link, image without `alt` / `alt="picture"`, `<div class="button">`, labels without `for`.
- `styles.css`: low-contrast colours (`#888` on `#eae4e4`, white button text on `#eae4e4`), `cursor: pointer` on headings/paragraphs, nav reordered with `order` (visual ≠ DOM/tab order), focus outline removed (`outline: none !important`), 10px small text.
- No plumbing needed (static HTML/CSS, open with Live Server).

## Flow (as taught historically)
1. Theory from `a11y.md` (POUR, WCAG levels, ARIA rules).
2. Run a **Lighthouse** accessibility audit (Chrome DevTools → Lighthouse → Accessibility) on the starter page via Live Server; optionally also a screen reader / keyboard-only walk-through (Tab order!).
3. Fix the page:
   - Landmarks: `header`, `nav`, `main`, `section`s, `footer`; page title `span` → `h1`.
   - Icon link: `aria-label="Home"` on the link, `aria-hidden="true"` on the `<i>` icon.
   - Meaningful `alt` texts on both images.
   - `<div class="button">` → `<button>`.
   - `<label for="...">` for name, email, message and privacy checkbox (+ `.checkbox-container` spacing).
   - CSS: introduce `--bg-dark` / `--text-light` custom properties with sufficient contrast, `.button:hover`, bigger button padding, small text 10px → 12px; remove the `cursor: pointer` rule, the nav `order` rules and the focus-visible outline removal.
4. Re-run Lighthouse and compare scores.

## Completed state
See this branch: `Lesson7/index.html`, `Lesson7/styles.css` (= historical completed code).
The historical completed commit also contained `Report-01.html` — a 350 KB saved Lighthouse report generated in class (local 127.0.0.1 URL). It is **not** included (generated artifact; students produce their own).

## Notes / possible homework
- Typo "Meditaion" in the page is left as-is (fun to spot).
- `index.html` loads Anna's Font Awesome kit (`kit.fontawesome.com/d2ae1f236a.js`) — public by design, same as in the historical repo; restrict the kit's allowed domains in Font Awesome if needed.
- Homework idea: run Lighthouse on their Lesson 5/6 pages (landing page / dashboard) and fix the issues; check colour contrast with the DevTools contrast checker.
No exercises prepared (no homework in the historical source).
