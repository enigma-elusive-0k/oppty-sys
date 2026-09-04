# modules/DOCX_BUILD.md (Step 7)

How a tailored resume becomes a submission file. Tier 2 generates the DOCX from the specification below; Tier 1 delivers markdown plus the layout guide for the user to apply in their own editor. No template file ships with the package; the spec is the template.

---

## 1. Formatting specification (both tiers)

| Element | Spec |
|---|---|
| Page | US Letter (A4 if `CONFIG.md` location is outside North America) |
| Margins | 0.5 to 0.6 in all sides |
| Font | One family throughout: Calibri, Aptos, or Arial. Set on every run, not only on the style. |
| Name | 15 to 17 pt bold |
| Contact line | 9 to 10 pt, single line: location, phone, email, LinkedIn. Pipes or bullets as separators. |
| Status line | 9 to 10 pt italic, directly under contact, from `CONFIG.md` |
| Title line | 10 to 11 pt bold, uppercase, matches the leveling decision |
| Section headings | 9 to 10 pt bold uppercase, thin bottom rule |
| Body and bullets | 9 to 9.5 pt. Floor is 9. Never lower to force pagination. |
| Line spacing | 1.0 |
| Paragraph spacing | 2 to 4 pt after bullets; 6 to 8 pt before section headings |
| Bullets | Standard round bullet, 0.15 to 0.2 in hanging indent |
| Employer line | Bold employer, then location and dates. Dates right-aligned via a right tab stop, not spaces. |
| Role title line | Bold, directly under employer |
| Competencies | Single-column delimited line or short single-column list. **No tables.** |
| Footer | Optional; small, one line. Page numbers optional. |
| Page count | Target 2. Three is acceptable for 20+ years at Director level and above; one is acceptable for early-career. |
| Punctuation | Per `SYSTEM.md` 8.3. No em-dashes. Curly quotes are fine. |

Section order: Header, Title line, Summary, Core competencies, Experience, Earlier experience (if used), Education, Certifications (if any). Nothing else. No photo, no graphics, no text boxes, no columns in the body.

Why no tables: multi-column and borderless tables are the most common ATS parse failure. They fragment phrases across cells and reorder text. A delimited line parses everywhere.

---

## 2. Tier 2: build

### 2.1 Tooling
Use whatever document-generation capability the environment provides. If a docx skill or library guide is available, read it before building; it will have environment-specific constraints. Preferred libraries in order: docx-js, python-docx. Either is fine if the output satisfies the checks below.

### 2.2 Build rules
- Set fonts on both the style and each run (the `w:rFonts` element in OOXML), or the render will fall back on some machines.
- Use real bullets (numbering definitions), not typed bullet characters.
- Use a right tab stop for dates. Verify its position in the OOXML.
- Insert a hard page break only where it improves skim value (typically before a role that would otherwise split three lines onto the next page). Never to pad.
- Set core properties: title, subject, author (the user's name), and clear `lastModifiedBy`. Remove any comments part, tracked changes, and custom XML the library emits by default.
- Filename per `SYSTEM.md` section 10.

### 2.3 Verification, in order
1. **Plain-text extraction.** Dump the document text. Confirm section order survives, every keyword from the coverage table is present, no phrase is split, and the education block matches `CONFIG.md` verbatim.
2. **OOXML inspection.** Confirm font set on runs, tab stop present, no stray parts (comments, custom XML), no em-dash characters (U+2014) anywhere in `document.xml`.
3. **Render to PDF or PNG.** Open every page image. Check the pass criteria below. Text extraction cannot see clipping, overlap, spacing collapse, or a heading orphaned at a page foot.
4. **Page count** matches the target. If it does not, adjust content before adjusting spacing; adjust spacing before adjusting margins; never adjust font size below the floor.

### 2.4 Pass criteria
- Every page renders.
- Page count as expected.
- No clipping, overlap, or missing text.
- Name, contact, status, and title lines fit cleanly on their own lines.
- Bullets consistently indented; no bullet wraps into a fourth line.
- No section heading alone at the bottom of a page.
- No role split with fewer than two bullets on either side of a page break.
- Dates align on the right.
- Footer readable and unobtrusive.
- Opens in LibreOffice (or the available renderer) without layout warnings.

The last render is the shipping gate. Any edit after it requires a re-render.

### 2.5 Deliver
Present the DOCX. Present a PDF only if the portal requires it or the artifact is for networking. State the page count and confirm the four verification steps passed in one line each.

---

## 3. Tier 1: layout guide for the user

Deliver the resume as clean markdown with this structure, then this checklist. The user applies the spec in Word, Google Docs, or Pages.

### 3.1 Markdown structure delivered
```
# Full Name
Location | Phone | Email | LinkedIn
*Status line*

## TITLE LINE

## SUMMARY
Three to five sentences.

## CORE COMPETENCIES
Term | Term | Term | Term | Term | Term | Term | Term

## EXPERIENCE

**Employer** | Location | Mon YYYY to Mon YYYY
**Role Title**
- Bullet
- Bullet

(repeat)

## EDUCATION
Institution
Degree, Major, Honors

## CERTIFICATIONS
Name, Issuer, Year
```

### 3.2 User checklist
1. Paste into a blank document. Set one font family for everything at 9 to 9.5 pt body.
2. Apply the sizes in section 1 to name, title, and headings.
3. Set margins to 0.5 to 0.6 in.
4. Replace the competencies line separators with the same character throughout; keep it one paragraph.
5. Put dates on the right with a right-aligned tab stop, not spaces.
6. Turn the dashes into real bullets with the editor's bullet tool.
7. Check the page count. If it runs long, cut a bullet before shrinking anything.
8. Find-and-replace: search for the em-dash character and remove every one by rewriting the sentence.
9. Read the education block against `CONFIG.md` character by character.
10. Export to DOCX (preferred) or PDF if the portal requires it. Name per `SYSTEM.md` section 10.
11. Reopen the exported file and page through it at 100 percent. Anything that looks wrong probably is.

---

## 4. Known defects to watch for

- Two-column or borderless tables for competencies: fragments in ATS parse. Do not use.
- Font set on the style only: renders as a fallback font on some systems and in some ATS previews.
- Typed bullet characters instead of real bullets: parse as literal characters; some ATS drop the line.
- Library-emitted metadata (`lastModifiedBy` values like "Un-named," empty comments parts): unprofessional if a reviewer checks properties. Clean it.
- Hard page breaks left in after content changes: produce a mostly blank page. Re-check after every edit.
- Em-dashes reintroduced by an editor's autocorrect: scan after the user's manual edits, not only after generation.

---

*Opportunity System DOCX Build v1.0. MIT License. Copyright (c) 2026 Paul Lothridge.*
