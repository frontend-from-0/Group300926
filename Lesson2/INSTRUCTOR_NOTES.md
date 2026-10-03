# Lesson 2 — HTML & CSS basics, semantic structure, forms (Instructor Notes)

**Topic:** Semantic HTML, linking CSS, building a sign-up form  
**Cohort / repo:** 30092026 → `frontend-from-0/Group300926`  
**When:** Wed 7 Oct 2026, 19:30 Europe/Stockholm  
**Historical source:** `frontend-from-0/Group050626` Lesson2  
- Starter: `e2274be` “Lesson2 starter files”  
- Completed: `556652d` “Add Lesson2 completed files”

Student PR: `questions.md` only.  
This instructor PR: completed `index.html`, `sign-up.html`, `style.css`, `note.md` + these notes. **Do not merge** into student-visible `main` until you decide.

L1 student/instructor PRs #1/#2 remain open — left untouched; this branch is based on current `main`.

## Goals

- Contrast **semantic** vs non-semantic elements (`header`/`nav`/`main`/`footer` vs `div`/`span`).
- Three ways to add CSS (inline, internal `<style>`, external stylesheet) — prefer external.
- Prefer **class** selectors for styling over IDs/tags.
- Build a **form** with labels, inputs, textarea, radio/checkbox, `name` attributes, GET submit → query string.

## Before class

- [ ] Recording on
- [ ] Live Server (or equivalent) ready
- [ ] Be ready to show the query string after submit (`note.md` has example URLs)

## Teaching flow

1. **Questions.md** (TR/EN) — semantic vs not; name 5 semantic tags; three CSS attachment methods; why classes; form tags; why `name` matters for the backend.
2. **Build `index.html` live** — `header`/`nav`/`main`/`footer`; link `./style.css`; show a small internal `<style>` and one inline `span` style as “what not to overuse”.
3. **`sign-up.html`** — shared nav; `<form method="GET">` with:
   - text + email inputs (`required`, `autocomplete`, matching `label for` / `id`)
   - textarea for AI prompt
   - radio group for model choice
   - checkbox for save-model / terms
   - submit → inspect URL query params
4. **`style.css`** — layout helpers (`.input-group`, `.full-width`, `.block-label`, accent).
5. **`note.md`** — paste example submitted URLs; discuss missing fields when inputs lack `name` or are empty.

## Starter vs completed

| Starter | Completed |
|---------|-----------|
| `questions.md` | + `index.html`, `sign-up.html`, `style.css`, `note.md` |

## Pitfalls

- `label` without matching `for`/`id`.
- Forgetting `name` → field missing from query string.
- Using only IDs for CSS (specificity / reuse).
- Relative links between `index.html` and `sign-up.html` broken if wrong folder.

## Exercises

No separate Lesson2 exercises repo entry needed for this new cohort yet; historical homework not clearly packaged for copy. Skipped.

## Files in this instructor PR

| Path | Role |
|------|------|
| `Lesson2/index.html` | Semantic home page + CSS link demos |
| `Lesson2/sign-up.html` | Completed form |
| `Lesson2/style.css` | Shared styles |
| `Lesson2/note.md` | Example GET query strings from classroom |
| `Lesson2/INSTRUCTOR_NOTES.md` | These notes |
