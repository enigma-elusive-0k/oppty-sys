# Example: one Live Fire, start to finish

Fictional candidate, fictional company, invented details. The point is the shape of each step's deliverable and how short the exchanges are. Approvals are the user's single-word replies.

Candidate: Dana Reyes, most recently Director of Program Management at a payments company, targeting Staff TPM (IC) and Director roles. Onboarding complete; Tier 2; built-in memory.

---

## Chat: `Halden Systems - Staff TPM, Ingestion - Live Fire`

**User**
> [Live Fire] Run the Opportunity System bootstrap. Here is the role: https://halden.example/careers/staff-tpm-ingestion

**Assistant**
> Tier 2, built-in memory. Onboarding complete. No open checkpoint.
> Starting Live Fire Step 1 for Halden Systems, Staff TPM, Ingestion.

### Step 1: Intake

**Assistant**
> **Intake**
> 1. Halden Systems, Staff Technical Program Manager, Ingestion Platform. Boston, hybrid 3 days. Posted 9 days ago. No deadline shown.
> 2. Target level: IC, Staff. JD body confirms: no direct reports, "partner with" engineering managers, owns program outcomes.
> 3. CONFIG conflicts: none. Hybrid Boston is within your commutable radius.
> 4. Prior history: none in tracker.
> 5. Contacts: none at Halden. One second-degree possibility (M. Okafor knows their VP Eng) noted in CONFIG.
> 6. Employer AI policy: none stated in the posting.
>
> Proceed to triage?

**User**
> Yes

### Step 2: Fit and triage

**Assistant**
> **Fit: 8/10. Verdict: Go.**
>
> Themes: they are hiring someone to make a pipeline that already works at scale become predictable to change. Release discipline, cross-team dependency management, incident-to-backlog closure, and a partner who can hold engineering managers to commitments without authority.
>
> Keywords (weighted): technical program management (must), distributed systems (must), release management (must), incident management (must), cross-functional (must), SLO (nice), Kafka (nice), roadmap (must), stakeholder (must), risk (must), on-call (nice), metrics (must), vendor (nice).
>
> Gaps: no Kafka; SLO experience is as a consumer, not owner. Both bridgeable.
>
> Risks: four Director titles on an IC req.
>
> Variant: Staff TPM (IC) base. Import the on-call and postmortem bullets from the Director variant's Meridian Pay section, reframed as program ownership.
>
> Proceed to leveling?

**User**
> Go

### Step 3: Leveling

**Assistant**
> **Down-level.** Title line "Staff Technical Program Manager." Direct-report counts suppressed on all four roles. Leadership framed as program ownership and influence without authority. Rationale: the JD is explicit about IC scope, and Director-scale org language would trigger the overqualified screen.
>
> Proceed to draft?

**User**
> Proceed

### Step 4: Tailored draft

**Assistant**
> Draft attached (markdown, 2 pages at spec).
>
> **Change log**
> 1. Title line changed to target.
> 2. Summary rewritten around pipeline predictability and incident-to-backlog closure.
> 3. Competencies reordered: release management and dependency management moved to positions 1 and 2; org design removed.
> 4. Meridian Pay: imported the settlement-pipeline replay bullet and the on-call rotation bullet. Retired the "built PMO from zero to 3 reports" bullet.
> 5. Northwind Logistics: "managed 12 engineers" changed to "ran program delivery across three squads."
> 6. Education block checked against CONFIG: match.
>
> **Coverage: 88 percent weighted.**
>
> | Term | Present | Where |
> |---|---|---|
> | technical program management | yes | title, summary |
> | distributed systems | yes | Meridian bullet 1 |
> | release management | yes | competencies, Meridian bullet 3 |
> | incident management | yes | Meridian bullet 4 |
> | cross-functional | yes | summary |
> | SLO | yes, hedged | Meridian bullet 2 ("worked to SLOs owned by SRE") |
> | Kafka | no | cannot cover truthfully |
> | roadmap | yes | Northwind bullet 1 |
> | stakeholder | yes | summary |
> | risk | yes | competencies |
> | on-call | yes | Meridian bullet 4 |
> | metrics | yes | competencies, Northwind bullet 2 |
> | vendor | yes | Northwind bullet 3 |
>
> Proceed to trace gate?

**User**
> Yes

### Step 5: Traceability gate

**Assistant**
> 14 claims traced. 11 at A. 2 at B. 1 at C.
>
> | Claim | Level | Source |
> |---|---|---|
> | Replay capability at Meridian | A | master, Meridian bullet 2 |
> | Carried on-call rotation two years | B | confirmed this thread; queued for back-population |
> | Owned postmortem process | B | confirmed this thread; verb "owned" set by you; queued |
> | "Worked to SLOs owned by SRE" | C | inferred from master Meridian bullets 2 and 4; hedged |
> | (remaining 10 rows omitted here; all A) | | |
>
> **HOLD 1**: confirm the SLO sentence as written, or cut it.
>
> Optional: `/export` for an outside review before the letter.

**User**
> Confirm SLO. Export, redacted.

**Assistant**
> HOLD 1 closed; SLO promoted to B and queued. Gate closed.
>
> Review package attached: `Review_Package_Halden_Resume_r1.md`, redacted. Paste it into your second chatbot; bring the findings back with `/import-review`.

*(User runs the review elsewhere and returns.)*

**User**
> /import-review
> [pastes seven findings and a verdict of Revise]

**Assistant**
> | # | Type | Sev | Disposition | Reason |
> |---|---|---|---|---|
> | 1 | FACT | blocker | Reject | "reduced settlement latency 40%" traces to master Meridian bullet 2, Level A |
> | 2 | FIT | should-fix | Accept | replay bullet buried at position 3; moved to 1 |
> | 3 | FIT | should-fix | Partial | reviewer wants Kafka mentioned; Level D. Added "streaming ingestion" (A, master Meridian bullet 1) instead |
> | 4 | VOICE | nit | Accept | "robust" removed |
> | 5 | VOICE | nit | Accept | triad in summary cut to two |
> | 6 | RISK | should-fix | Accept | four Director titles: added status line clarifying IC intent, per CONFIG |
> | 7 | RISK | nit | Reject | reviewer suggests dropping Northwind; it carries the roadmap and vendor keywords |
>
> Revised draft attached. Change log keyed to findings 2 through 6. Re-traced changed sentences: all A. Round 1 of 2 logged.
>
> Proceed to letter and answers?

**User**
> Proceed

### Step 6: Cover letter and screening answers

**Assistant**
> Letter attached, 231 words. Hook: Halden's public post on treating late telemetry as a safety problem. Proof points: replay capability; incident-to-backlog closure at Meridian. Concern named in one sentence: Director titles, IC intent. Close on the ingestion pipeline.
>
> Screening answers drafted: why Halden; why this role; comp (range per CONFIG); authorization; hybrid stance; Kafka knockout question answered honestly with adjacent streaming experience.
>
> Trace: all letter claims A or B. Forbidden-phrase scan clean.
>
> Proceed to build?

**User**
> Yes

### Step 7: Build and QA

**Assistant**
> Built `Dana_Reyes_Resume_Halden_StaffTPM_v1.docx` and `Dana_Reyes_CoverLetter_Halden_StaffTPM_v1.docx`.
>
> 1. Text extraction: section order intact, 12 of 13 keywords present, education matches CONFIG.
> 2. OOXML: fonts on runs, right tab at 10080, no comments part, no U+2014.
> 3. Render: 2 pages, no clipping, no orphaned heading, dates aligned.
> 4. Page count: 2 as expected.
>
> Proceed to package?

**User**
> Go

### Step 8: Submission package

**Assistant**
> 1. Files: the two above.
> 2. Route: ask M. Okafor for an intro to Halden's VP Eng first (OUTREACH 2.2, draft attached). Hold the portal submission until Okafor replies or three business days pass, whichever is first.
> 3. Refinements available: shorter summary; one more metric at Northwind if you can source it; PDF for Okafor.
> 4. Metadata clean.
> 5. Screen-prep stub: likely questions (why IC after Director; Kafka; how you hold EMs to commitments). Three proof points: replay capability, on-call ownership, 40 percent latency result. Probable gap: Kafka. Answer: streaming ingestion at Meridian on a different broker; the program mechanics do not change with the broker.
>
> Send the Okafor note and I will log the submission when you confirm.

**User**
> Sent. Okafor replied, intro made. Portal submitted day 3.

### Step 9: Log

**Assistant**
> Logged. Tracker row: Halden, Staff TPM, Fit 8, Go, Down-level, Staff IC variant + Meridian imports, route referral then portal, contact Okafor (second degree, offered intro), status Submitted, coverage 88, review round 1. Back-population queue now at 3.
>
> Next action: follow-up at 10 business days if silent. Say `/prep Halden` when a screen is scheduled.

---

## What this example shows

- Every step is one exchange. The user's replies are one to three words.
- The reviewer's suggestion to add Kafka was rejected on evidence grounds and replaced with a supportable adjacent claim. That is the evidence standard doing its job.
- The Director-title risk was handled three times: leveling (suppress counts), status line (state IC intent), and the letter (name the concern). None of it required invention.
- Two facts confirmed during the run went to the back-population queue instead of quietly into the master.

---

*Opportunity System example v1.0. MIT License. Copyright (c) 2026 Paul Lothridge.*
