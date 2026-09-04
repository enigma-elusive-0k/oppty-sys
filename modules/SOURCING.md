# modules/SOURCING.md (Step 0)

Finds roles worth running through Live Fire. Two modes: build the search profile (first run), then produce ranked shortlists (every later run). Triggered by `/sourcing`.

Requires web search. If unavailable, this module produces the search profile only and hands the user a set of copy-paste queries for their own use.

---

## 1. Search profile (first run, about 15 minutes)

Most fields are already in `CONFIG.md`. Pull them; ask only for what is missing.

1. **Target titles**, with common synonyms. For each role family in CONFIG, list the title variants employers actually post (for example "Technical Program Manager," "TPM," "Program Manager, Engineering," "Engineering Program Manager").
2. **Level range** to include and exclude. Explicit floor and ceiling.
3. **Location filter**: from CONFIG. Include remote roles whose posted location is elsewhere only if the posting says remote.
4. **Industries and company stages**: prefer and exclude, from CONFIG.
5. **Differentiators**: two or three phrases that, when they appear in a JD, indicate a strong fit. Drawn from the candidate's strongest evidence, not from aspiration.
6. **Disqualifiers**: phrases that, when present, make the role a No-Go regardless of title (for example "5 days onsite" for a remote-only candidate, a hard certification requirement the user lacks, a security clearance).
7. **Posting age limit**: default 21 days. Older postings are flagged, not excluded.
8. **Exclusions**: companies from CONFIG plus any the user names now.
9. **Cadence**: weekly by default. If scheduled tasks are available, offer to schedule; otherwise give the one-line prompt from `START_HERE_PROMPT.md`.

Store the profile in `STATE.md` under Sourcing. Confirm it back in a single table before the first run.

---

## 2. Shortlist run (every later run, about 10 minutes)

### 2.1 Search
For each title variant, search the major job boards and any company career pages the user named. Combine title with location and the top differentiator. Keep queries short. Vary them across runs; identical queries return identical results.

### 2.2 Filter
Drop anything that hits a disqualifier, an excluded company, or the level ceiling. Drop anything already in the tracker (applied, No-Go, closed). Flag postings older than the age limit.

### 2.3 Quick fit estimate
For each survivor, a one-line read and a provisional score:

- **Strong (8+)**: title, level, and at least two differentiators present; no obvious gaps.
- **Probable (6 to 7)**: title and level fit; one differentiator; a visible gap that looks bridgeable.
- **Marginal (5)**: fits on title only. Shown, not recommended.

Provisional scores are not triage. Step 2 of Live Fire does triage with the full JD.

### 2.4 Contact check
Cross-reference each surviving company against the Contacts table in CONFIG. Mark any with a warm or close contact. These sort to the top within their score band.

### 2.5 Deliverable
One table, ranked, maximum 15 rows:

| # | Company | Title | Location / remote | Posted | Est. fit | Contact | One-line rationale | Link |

Followed by:
- Count of postings reviewed and dropped, with the top two reasons for drops.
- Any posting that looks stale or duplicated across boards.
- The prompt: "Say `intake [n]` to start Live Fire on a row, `drop [n]` to exclude it, or `refine` to adjust the profile."

### 2.6 Promotion
`intake [n]` starts `SYSTEM.md` Step 1 for that row. Tell the user to open a new chat named `[Company] - [Role] - Live Fire` and paste the link there. Record the promotion in `STATE.md`.

---

## 3. Profile maintenance

- After every three runs, ask whether the results are drifting from what the user wants. Adjust titles, differentiators, or disqualifiers.
- After every Live Fire triage, compare the provisional score to the actual triage score. A gap of three or more points is a signal to adjust the profile. Log it under Learnings.
- If two consecutive runs produce nothing above Marginal, say so plainly and propose broadening: adjacent titles, a wider location, a different stage.

---

## 4. Stale and misleading postings

- Job boards syndicate and lag. A posting that appears on an aggregator may be closed on the employer's site. Prefer the employer's own posting when both exist.
- "Evergreen" postings (open for months, generic language, no team named) are low-yield. Flag them.
- If a fetch reports "closed" or "filled," cross-check with a web search before reporting that to the user. SPA-rendered career pages return stale states.
- Reposted roles: if a company reposts a role the user already applied to, flag it with the prior outcome. Do not silently surface it as new.

---

*Opportunity System Sourcing v1.0. MIT License. Copyright (c) 2026 Paul Lothridge.*
