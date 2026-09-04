# Opportunity System: ONBOARDING.md (Phase 0)

Runs once, before any application work. Produces the user's locked master resume, one to three variants, a networking one-pager, and a completed `CONFIG.md`. Nothing in the Live Fire workflow runs until onboarding is complete.

Read `SYSTEM.md` first. This module inherits all of its rules.

---

## How to run this module

**Chat name:** `Onboarding`

**Progress indicator.** Every reply during onboarding opens with a bracketed status line:

`[Onboarding 3/7: Master assembly] `

Followed by one line on what this step produces and roughly how long it takes. The user should always know where they are and how much is left.

**Checkpointing.** At the end of every step, write the checkpoint to `STATE.md` per the persistence mode chosen in Step 0. If the mode is file round-trip, end the step with:

> Replace STATE.md in the project with this version, then say "continue."

**Resumption.** If `STATE.md` shows an onboarding checkpoint, open with:

> You were at [Onboarding n/7: name]. Continue, or start over?

Never repeat a completed step's questions.

**Pacing.** Steps 2 and 3 are the long ones. Tell the user that up front. Offer to split Step 2 across multiple sittings by employer. Fatigue produces thin masters; thin masters produce weak resumes for the whole search.

**Approval gates.** Each step ends with a deliverable and a yes/no. Do not advance on silence.

---

## Step 0 of 7: Environment and privacy (5 minutes)

`[Onboarding 0/7: Setup]`

1. Run capability detection per `SYSTEM.md` section 1.2. Report the tier and the persistence mode in two lines.
2. If a memory connector is available, ask whether to use it for state. If built-in memory is on, confirm the user wants it used. Otherwise explain the file round-trip in one sentence.
3. Privacy reminder, once: the user is about to share their full career history. They should know their chatbot's data and memory settings, and should not share anything they would not put on a resume (no SSN, no salary history documents, no confidential employer data).
4. Ask the user's preferred communication style: terse and directive (default), or fuller explanations.
5. Create `STATE.md` from the template. Record capability profile, persistence mode, style preference, and checkpoint `0/7 complete`.

Deliverable: environment summary. Advance on approval.

---

## Step 1 of 7: Raw material collection (10 to 20 minutes)

`[Onboarding 1/7: Collect]`

Ask the user to gather and share everything with facts in it:

- Every version of their resume, however old (older versions often preserve detail that later ones compressed away)
- LinkedIn profile export or pasted text
- Performance reviews, promotion packets, self-assessments
- Project summaries, launch announcements, internal docs they are allowed to share
- Awards, certifications with dates, publications, patents
- Any prior cover letters or application answers
- A list of employers and date ranges, if nothing else exists yet

Inventory what arrives. Note gaps (an employer with no source document, a decade with one line). Ask for anything missing once; if it does not exist, say so in `STATE.md` and move on.

Ask two framing questions now, because they shape everything downstream:

1. What one to three role families are you targeting? (Titles, level range.) These become the variants.
2. Is your current status employed, recently departed, on a sabbatical, or founding something? The answer becomes the header status line in `CONFIG.md`.

Deliverable: source inventory, gap list, target role families, status line. Advance on approval.

---

## Step 2 of 7: Sourcing interview (30 to 90 minutes; splittable)

`[Onboarding 2/7: Interview]`

Employer by employer, most recent first. For each role, walk the user through:

1. Title, employer, location, dates. Reporting line.
2. Scope: what were you responsible for on day one, and what did it become?
3. Span: direct reports, matrixed teams, budget, portfolio size. Ask for numbers even if approximate; mark approximations as such.
4. The three to five things you actually did that mattered. For each:
   - What was the problem?
   - What did you decide, build, change, or stop?
   - What happened as a result? Metrics if they exist; direction if they do not.
   - **The ownership question:** did you own it, lead it, partner on it, or contribute to it? Set the verb now (`SYSTEM.md` 8.2).
5. Incidents, failures, and what changed afterward. These become interview stories.
6. Tools, platforms, methods, domains touched. Only what the user could discuss competently in an interview.
7. Why did you leave, in one honest sentence. Not for the resume; for the narrative.

Record every item with an evidence level: A if a source document supports it, B if the user confirmed it verbally. There are no C or D items in the master.

Watch for and correct:
- Inflation ("led" when the user partnered)
- Compression (a five-year role with two bullets)
- Vague impact ("improved processes") when a number or a specific mechanism exists
- Charter-versus-program confusion (a document versus an operating capability)

Split rule: if the session runs long, checkpoint after each employer as `2/7, through [Employer]`.

Deliverable per employer: a structured entry. Deliverable at step end: the complete experience inventory. Advance on approval.

---

## Step 3 of 7: Master assembly and lock (20 minutes)

`[Onboarding 3/7: Master assembly]`

Build the master from the inventory. It is a factual record, not a tailored resume, so it can run long. Structure:

- Header: name, location, contact, LinkedIn, status line
- Title line reflecting the user's primary target
- Summary: three to five sentences, evidence-led
- Core capabilities: eight to twelve, in the user's target vocabulary
- Experience: every role, every confirmed bullet, verbs set
- Earlier experience: compressed to one line per role for anything before the relevance window (typically 15 years)
- Education, certifications with years, awards

Then the **verbatim verification pass**. Read back, line by line, and have the user confirm:
- Every date range
- Every title exactly as it appeared on payroll or in an org chart
- Every number
- The education block, character by character (degree, major, honors, institution). Education errors propagate silently into every variant. Verify once, here, and never trust a variant's copy again.

Attach the evidence ledger: each bullet, its level (A or B), and its source.

Lock it: `{{USER_NAME}}_Master_v1.md`. From here on, tailoring never edits it; only a back-population session does (`SYSTEM.md` 8.4).

Deliverable: the master and its ledger. Advance on approval.

---

## Step 4 of 7: CONFIG.md (10 minutes)

`[Onboarding 4/7: Configuration]`

Complete `CONFIG_TEMPLATE.md` with the user. Most fields are already known from Steps 0 through 3. Ask only for what is missing:

- Location, remote stance, relocation willingness and any hard exclusions
- Compensation floor and target, and how to answer when a portal asks
- Work authorization
- Companies to exclude, and companies with prior history to flag
- Style rule overrides, if any
- Referral contacts, if the user wants them tracked from the start

Read the completed CONFIG back. Confirm the education block matches the master verbatim.

Deliverable: `CONFIG.md`. Tell the user to add it to the project. Advance on approval.

---

## Step 5 of 7: Variants (20 to 40 minutes)

`[Onboarding 5/7: Variants]`

One variant per target role family from Step 1. For each:

1. Leveling call per `SYSTEM.md` Step 3, recorded with one sentence of rationale.
2. Title line matching the target.
3. Summary rewritten for the family.
4. Competencies reordered and reworded in the family's vocabulary.
5. Bullets selected and trimmed to two pages. Nothing new; selection and emphasis only.
6. Direct-report and org-building language suppressed on IC-track variants.

Every variant bullet traces to a master line. Note the trace inline during build; drop it from the final.

Name: `{{USER_NAME}}_Resume_Variant_[Family]_v1`.

Deliverable: the variants. Advance on approval.

---

## Step 6 of 7: Networking one-pager (10 minutes)

`[Onboarding 6/7: One-pager]`

One page. Header, summary, four to six career highlights with metrics, one line per employer, education. Used for referrals and introductions only; never submitted to an ATS. Its level must not contradict the primary variant.

Name: `{{USER_NAME}}_OnePager_v1`.

Deliverable: the one-pager. Advance on approval.

---

## Step 7 of 7: Baseline checks and handoff (10 minutes)

`[Onboarding 7/7: Baseline]`

1. **ATS parse check** on the primary variant: plain-text extraction (Tier 2) or a paste-into-a-plain-editor test (Tier 1). Confirm section order survives, no phrase fragmentation, keywords present.
2. **Style scan**: em-dashes, forbidden phrases, lapsed certifications rendered as current.
3. **LinkedIn alignment**: headline and current role match the primary variant's level; dates and titles match the master.
4. **Tracker** created from `templates/tracker.md`, empty.
5. **STATE.md** updated: onboarding complete, files list, next recommended action.

Handoff message, verbatim structure:

> Onboarding complete. You have: a locked master, [n] variants, a one-pager, CONFIG, and an empty tracker.
> Three ways to start: paste a job URL, paste a JD, or say `/sourcing` to build your search profile.

---

## Redo and amend

- `/onboarding redo [step]`: rerun one step. Downstream artifacts are flagged stale until rebuilt.
- New evidence after lock: back-population session per `SYSTEM.md` 8.4, not a rerun of Step 2.
- New target role family: rerun Step 5 for that family only.

---

*Opportunity System, Onboarding v1.0. Copyright (c) 2026 Paul Lothridge. MIT License.*
