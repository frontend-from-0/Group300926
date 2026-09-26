# Lesson 1 — First introduction + first HTML page (Instructor Notes)

**Topic:** Course intro + build first HTML page  
**Cohort / repo:** 30092026 → `frontend-from-0/Group300926`  
**When:** Wed 30 Sep 2026 (calendar)  
**Historical source:** `frontend-from-0/Group050626` Lesson1  
- Starter: `a723136` (empty `Lesson1/index.html` + course PDF)  
- Completed: `b532028` (full `index.html` + `favicon.ico`)

Student PR: empty `Lesson1/index.html` + course program PDF.  
This instructor PR: completed page with teaching comments + favicon + these notes. **Do not merge** into student-visible `main` until you decide; keep instructor content off the student branch.

## Before class

- [ ] Start / remind **recording**
- [ ] Confirm students can open the repo / PR materials (or share the course PDF)
- [ ] Have VS Code + Live Server (or browser open-file) ready
- [ ] Icebreaker ready (see below)

## Icebreaker (5–10 min)

Ask each student briefly:

1. Name + city / timezone
2. Why they joined Code2Career / what they hope to build
3. Any prior HTML/CSS/JS experience (none is fine)

Optional warm-up: “What is a website made of?” — collect answers on a whiteboard/chat before naming HTML/CSS/JS.

## Course goals (high level)

Walk the **course program PDF** (`Code2Career course program 2026.pdf`):

- Full-stack journey overview (HTML → CSS → JS → React → Node, etc.)
- Tools: VS Code, Git/GitHub, browser DevTools, Figma later
- Expectations: attendance, practice, asking questions, recording for review
- Where materials live (this Group repo)

Keep it short — motivation + map, not a full syllabus lecture.

## Teaching flow: empty HTML → structure

Students start from **empty** `Lesson1/index.html`. Build live toward the completed file in this branch.

Suggested order:

1. **Doctype** — `<!doctype html>` (browser mode / HTML5)
2. **`html` root** — `<html lang="en">` … `</html>` (mention `lang` as an attribute)
3. **`head` vs `body`** — metadata vs visible content
4. **`meta` charset + viewport** — UTF-8, mobile scaling
5. **`title`** — tab title (“Lesson 1”)
6. **Favicon** — `<link rel="shortcut icon" …>` + drop in `favicon.ico` (you can paste/link this; students need the file)
7. **Headings** — `h1` “First lesson”
8. **`section` + `h2` + `p`** — first content block (course topics); lorem or real short text
9. **Lists** — unordered (`ul` / `li`, optional `list-style-type`) then ordered (`ol type="A"`) for tools
10. **Links** — `<a href="…" target="_blank">` to W3Schools, MDN, FreeCodeCamp, etc.
11. **Images** — `<img src="…" alt="…">` (explain `src` / `alt`; use a public Unsplash URL or similar)
12. **`div` / `span`** — generic containers vs inline (light touch)

Point at the HTML comments in the completed `index.html` while teaching (attributes, closing tags, Turkish notes on `src`/`alt` if useful for the group).

## What students type vs what you paste

| Students type themselves | OK to paste / provide |
|--------------------------|------------------------|
| doctype, `html`/`head`/`body` skeleton | Long Unsplash `src` URL |
| `meta`, `title`, headings, short paragraphs | Full favicon `<link>` once explained |
| `ul`/`ol`/`li` with short items | Completed reference after they try |
| Simple `<a href="https://…">` links | `favicon.ico` binary file |
| A short `alt` and maybe a simple img URL | Entire final file if someone is blocked |

Rule of thumb: structure and tags by hand; long URLs and binary assets from you.

## End of lesson

- [ ] Students save and open the page in a browser
- [ ] Quick recap: doctype / head / body / section / list / link / img
- [ ] Point to course PDF for the bigger picture
- [ ] Homework if any: recreate the page from memory or tweak text/links
- [ ] Confirm recording stopped / link shared if needed

## Files in this instructor PR

| Path | Role |
|------|------|
| `Lesson1/index.html` | Completed teaching version (comments + full structure) |
| `Lesson1/favicon.ico` | Favicon used by the completed page |
| `Lesson1/INSTRUCTOR_NOTES.md` | These notes (instructor-only; keep off student merge) |
