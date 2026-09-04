# modules/EVIDENCE_STANDARD.md

Defines what may be claimed in an employer-facing artifact and how strongly. Governs `SYSTEM.md` Step 5 (traceability gate), section 8.4 (back-population), and every place the Voice Guide asks for evidence.

The single rule: **never improve prose by improving the facts.**

---

## 1. Evidence levels

Every factual claim in a resume, cover letter, application answer, outreach note, or prepared interview story is assigned one level.

| Level | Definition | Usable? | Verb strength | Disposition |
|---|---|---|---|---|
| **A: Documented** | Appears in the locked master, or in a source document collected at onboarding (prior resume, review, announcement) and reflected in the master. | Yes | Full | Use as written. |
| **B: User-confirmed** | The user has stated it explicitly in a thread and confirmed it when asked, but it is not yet in the master. | Yes | Full, once the verb is set with the user | Use; log to the back-population queue in `STATE.md`. |
| **C: Reasonable inference** | Follows from Level A or B material but the user has not stated it directly. Example: the master shows a role coordinating teams in three countries; "experience coordinating distributed engineering organizations" is a C. | Only with hedged verbs, and only if it survives a check with the user | Hedged ("supported," "worked across," "contributed to") | Ask the user. If confirmed, promote to B. If not, cut or keep hedged. |
| **D: Unsupported** | Nothing in the master, no user confirmation, no defensible inference. Includes claims imported from a JD, a reviewer's suggestion, or a plausible-sounding pattern. | No | None | Cut. Rewrite to what is supportable if something adjacent exists. |

A claim's level is about provenance, not importance. A minor detail with no source is still a D.

---

## 2. What counts as a claim

- Any number (percent, dollar, headcount, duration, count of anything)
- Any title, employer, date, or reporting line
- Any verb of ownership ("built," "established," "led," "owned," "founded")
- Any named tool, platform, method, certification, or domain
- Any named outcome ("reduced," "improved," "enabled," "prevented")
- Any characterization of scope ("global," "enterprise," "multi-region," "24x7")

Adjectives are not claims; they are assertions, and the Voice Guide already forbids most of them.

---

## 3. Verb precision

The verb is part of the claim. The same fact can be an A with one verb and a D with another.

| The fact | Correct verb | Inflated verb (becomes D) |
|---|---|---|
| Candidate worked with finance and legal to set up a process; finance owned it | Partnered with; contributed to | Established; built; owned |
| Candidate owned the incident process (runbooks, postmortems, cadence) but engineers commanded live incidents | Owned the incident management process | Led incident response; commanded incidents |
| Candidate influenced a large group without reporting authority | Matrix-managed; coordinated across; influenced | Managed; led a team of |
| Candidate wrote a charter document | Defined a charter | Built a program (a program is an operating capability; a charter is a document) |
| Candidate built and ran an operating capability | Built and ran a program | Defined a charter (understates) |
| Certification earned in a given year, since lapsed | [Certification], [Year] | [Certification] (implies current) |

When the user corrects a verb, the correction is authoritative. Record it in `STATE.md` Learnings so it is not re-inflated in a later thread.

---

## 4. The traceability gate (Step 5 format)

For each bullet or sentence in the artifact:

```
[Level] [Source] [Note]
```

Examples:

```
[A] master, [Employer] bullet 3
[B] confirmed in this thread, [date]; verb "partnered with" set by user; queued for back-population
[C] inferred from master [Employer] bullets 1 and 4; hedged to "worked across"; HOLD for user confirmation
[D] no source; cut. Adjacent supportable claim: [rewritten text] at [A]
```

Gate output is a table with one row per claim, followed by a HOLD list. The gate does not close while any HOLD is open or any D remains.

Applies to every employer-facing artifact, not only the resume: cover letters, screening answers, outreach messages, and prepared interview stories all get a trace pass before they are used.

---

## 5. Sources that do not confer evidence

These are inputs, not sources. Nothing in them raises a claim above D on its own.

- The job description (a JD describes what the employer wants, not what the candidate did)
- A reviewer's findings from `/import-review` (a reviewer can suggest a claim; only the user can confirm it)
- An earlier tailored resume that was never traced (prior artifacts inherit their own errors; trace to the master, not to a variant)
- LinkedIn profile text the user has not verified in onboarding
- The assistant's own recollection from a prior thread, unless it is recorded in `STATE.md` or the master

The last item matters. Memory across threads is convenient and fallible. A claim the assistant "remembers" the user confirming, with no record, is a C until re-confirmed.

---

## 6. Back-population

Level B evidence accumulates. When the queue in `STATE.md` reaches five items, or before any major new push, the assistant proposes a back-population session:

1. Open a chat named `Back-population - [date]`.
2. Walk each queued item: confirm the fact, set the verb, choose the employer and placement.
3. Amend the master. Increment its version. Re-lock.
4. Update the evidence ledger.
5. Mark variants that now contain outdated or missing material as stale.
6. Clear the queue in `STATE.md`.

The master is never amended inside a Live Fire chat. This is what keeps tailoring pressure from leaking into the factual record.

---

## 7. Edge cases

- **Approximate numbers**: usable at the level of their source, rendered with a tilde or "about." Never round an approximation into a precise figure.
- **Ranges the user cannot pin down**: use the conservative end.
- **Claims about teams the user was part of but did not lead**: "as part of a team that..." or "contributed to..." at the source's level.
- **Confidential employer details**: if the user cannot say it in an interview, it does not go on the page.
- **Results that occurred after the user left**: attributable only if the user's work is the documented cause; otherwise cut.
- **Education and credentials**: always A, always verbatim from `CONFIG.md`, checked on every artifact. This is the one place where a copy error propagates silently across every document; the standard treats it as a hard check, not a judgment call.

---

## 8. Why this exists

Tailoring pressure is constant and mostly benign. A keyword is missing; a bullet almost fits; a reviewer says "you should mention X." Each step is small. The accumulation is a resume the candidate cannot defend in an interview. The evidence level attached to every claim is the mechanism that stops the drift, and the back-population queue is the mechanism that lets true-but-undocumented facts enter the record properly instead of by accident.

---

*Opportunity System Evidence Standard v1.0. MIT License. Copyright (c) 2026 Paul Lothridge.*
