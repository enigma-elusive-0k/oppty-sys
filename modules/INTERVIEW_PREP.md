# modules/INTERVIEW_PREP.md (Step 10)

Runs when an interview is scheduled. Triggered by `/prep [company]`. Chat name: `Prep - [Company] - [Stage]`. One chat per company; all stages accumulate there.

Inherits `modules/VOICE_GUIDE.md` (answer architecture) and `modules/EVIDENCE_STANDARD.md` (every prepared story is traced).

---

## 1. Intake for the stage (5 minutes)

Pull from the tracker and the Live Fire chat: the JD, the triage themes, the leveling call, the three proof points and the one probable gap from the Step 8 stub.

Ask for the new information:

1. Stage: recruiter screen / hiring manager / panel / onsite / final / executive.
2. Interviewer names and titles, if known. Format and length.
3. Anything the recruiter or hiring manager said about what the stage is for.
4. What the user has already learned from earlier stages (record in the debrief log, section 5).

If any of this is unknown, propose the note in section 6.1 to ask for it. Interviewers usually answer.

---

## 2. Panel map

One entry per interviewer or room:

| Interviewer | Role and relationship to the position | What they are likely evaluating | Lead story | Backup story | What to avoid |

Rules for filling it:

- **Hiring manager**: fit for the role's actual problem, and whether they can work with this person. Lead with the strongest proof point from triage.
- **Direct partner in the role** (a peer the user would work with daily): working-relationship fit, not technical depth. Prepare questions for them; treat it as mutual evaluation.
- **Peer in the same discipline**: reasoning structure. They will probe how the user thinks. Judgment sections of stories matter most here.
- **Skip-level or executive**: operating philosophy, judgment under ambiguity, whether the user can be trusted with scope. Fewer stories, more reflection.
- **Cross-functional stakeholder** (product, finance, security, customer-facing): the story where the user served that function's interest, with the tradeoff visible.
- **Unknown interviewer**: prepare the two most versatile stories and a question that draws out their relationship to the role in the first minute.

"What to avoid" is specific: a mechanism the interviewer owns and will know better than the user; a story that overstates ownership; a domain the user should not pretend to have depth in.

---

## 3. Story bank

Six to eight stories, each traced. More than that and the user rehearses breadth instead of depth.

For each story, a one-page card:

1. **Title** (the headline sentence, as it will be spoken).
2. **Question types it answers** (conflict, ambiguity, failure, influence without authority, scale, prioritization, and so on).
3. **The six beats** per `VOICE_GUIDE.md` 4.5: Headline, Context, Judgment, Action, Result, Reflection. Two or three lines each. Judgment is the longest.
4. **The number** (if any), with its evidence level.
5. **The boundary**: what the user did not do (did not command the incident; partnered rather than owned). Stated so the user does not overclaim under pressure.
6. **Follow-up the interviewer is likely to ask**, with the one-line answer.
7. **Time**: rehearsed under three minutes.

Trace every story. A Level B fact in a story is usable and goes to the back-population queue. A Level C fact is hedged in the spoken version. Nothing at D.

### 3.1 Coverage check
Map the story bank against the likely question types for this stage. Any type with no story gets one. Any story that covers nothing likely gets cut.

### 3.2 Rehearsal
If the user wants it, run a mock: the assistant asks, the user answers in text, the assistant times by word count (roughly 400 words is three minutes spoken), and critiques against the architecture. Two rounds per story, maximum. The third round is memorization, which reads as rehearsed.

---

## 4. Standing answers

Prepared once per company, reused across stages, adjusted for audience:

- **Tell me about yourself**: `VOICE_GUIDE.md` 4.4. Two or three sentences on big-picture fit for this role.
- **Why this company**: `VOICE_GUIDE.md` 4.2, spoken form. Company first.
- **Why are you leaving / why did you leave**: one honest sentence, forward-looking. From the onboarding narrative.
- **The probable gap**: named before they name it, with the transferring mechanism. From the Step 8 stub.
- **Level questions** ("this is an IC role; you have been a Director"): the answer from the leveling decision. Practiced until it sounds decided.
- **Compensation**: `CONFIG.md`.
- **Questions for them**: three per interviewer, specific to their role. At least one that tests whether the role is what the posting says it is.

---

## 5. Debrief (within 24 hours of each stage)

Log in the Prep chat and summarize in `STATE.md`:

1. Who was in the room and what they actually asked.
2. Which stories were used and how they landed. Where the user ran long. Where the interviewer pulled.
3. Anything the user learned about the role, team, or company that changes the fit read.
4. Anything the user said that they now think was inaccurate or overstated. Correct it in the story bank; if it touches a claim, re-trace.
5. New facts about the user's own history that surfaced under questioning. Level B; queue for back-population.
6. Concerns the interviewer raised, stated or implied. These drive the next stage's prep and the thank-you note.
7. One behavioral fix for next time. One only.

Debriefs are where the story bank gets better. Skipping them is the most common prep failure.

---

## 6. Notes to send

All governed by `modules/OUTREACH.md`; templates there.

### 6.1 Pre-interview ask
To the recruiter or hiring manager, when the panel is named but the rooms are not described: a two-line note asking what each interviewer is looking for and what to avoid. Send early; it is a normal question and the answer is usually specific.

### 6.2 Thank-you
Within 24 hours. One per interviewer if emails are available, otherwise one to the recruiter to forward. Three to five sentences: one specific thing from the conversation, one point worth adding or clarifying (especially if the debrief surfaced a concern), and a close on the work.

### 6.3 Post-rejection close
If the stage ends the process: a short, ungrudging note to the hiring manager and any contact who helped. Keeps the relationship for the next req.

---

## 7. Process discrepancies

When the described process does not match what is happening (a stage the recruiter did not mention; an assessment folded into a panel; a "conversation" that turns out to be a technical screen), flag it to the user immediately and propose a one-line clarifying note to the recruiter. Ambiguity about what a stage is for is the second most common reason a strong candidate underperforms in it.

---

*Opportunity System Interview Prep v1.0. MIT License. Copyright (c) 2026 Paul Lothridge.*
