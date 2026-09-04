# Opportunity System

A gated, evidence-first workflow for running a job search with Claude. It turns a scattered search into a pipeline: find roles, decide which deserve effort, tailor a resume you can defend in an interview, write in a voice that sounds like you, prepare for the panel, and log what happened so the next application is better.

Built by someone who used it to run his own search. Shared because friends asked.

**Version 1.0. Claude only.** Works in a Claude Project on any plan that supports Projects. Better with file creation and memory; usable without them.

---

## What it does

- **Sourcing**: builds a search profile once, then returns a ranked shortlist on demand.
- **Triage**: scores every role 1 to 10 and gives a verdict. Go, Stretch, or No-Go. No-Go means you do not apply, and the system tells you what to do with any contact you have there instead.
- **Leveling**: decides, explicitly, how to position seniority for each role. This is where experienced candidates get screened out, so it is its own step.
- **Tailoring with traceability**: every resume claim is tagged with an evidence level and traced to your master. Nothing ships that you cannot back up. Verbs match what you actually did.
- **Writing voice**: cover letters and application answers that sound like a person who understands the employer's problem, not a polished applicant. Built from the principles of seven respected career advisors.
- **Outside review**: export any artifact to a second chatbot with a reviewer brief, bring the findings back, and triage them. The reviewer cannot add claims about you; only you can.
- **Interview prep**: panel maps, a traced story bank, three-minute answer structure, and a debrief after every stage.
- **Outreach**: referral asks, follow-ups, thank-yous, close-outs. Referral before portal, always.
- **Tracking**: one tracker, one state file, resume-from-wherever-you-left-off.

## What it does not do

- Submit anything for you. You read everything before it goes out.
- Invent experience. If it is not in your master and you have not confirmed it, it gets cut.
- Write answers an employer requires you to author yourself. It critiques and edits those.
- Replace your judgment. It asks for approval at every step and stops when you say stop.

---

## Setup (about 10 minutes, then 1 to 3 hours of onboarding)

1. **Create a Claude Project.** Name it whatever you like.
2. **Upload the package.** Everything in this repo except `README.md`, `LICENSE`, `CHANGELOG.md`, and `examples/`: that is `SYSTEM.md`, `ONBOARDING.md`, `CONFIG_TEMPLATE.md`, `STATE_TEMPLATE.md`, `START_HERE_PROMPT.md`, and the `modules/` and `templates/` folders. Upload the files inside `modules/` and `templates/` individually; Projects do not preserve folders.
3. **Paste the instructions.** Open `START_HERE_PROMPT.md`, copy Part A, and paste it into the Project's Instructions field.
4. **Check your settings.** If you use Claude's memory feature, the system will use it to remember where you are. If not, it will hand you a `STATE.md` file to re-upload at checkpoints. Either works. Read the privacy note below first.
5. **Start a new chat in the Project** and send:
   ```
   [Onboarding] Run the Opportunity System bootstrap and start onboarding.
   ```
6. **Follow the prompts.** Onboarding has seven steps and shows you a progress indicator. The long step is the interview about your career history; you can split it across sittings. When it finishes you will have a locked master resume, one to three role-specific variants, a one-page networking summary, a `CONFIG.md`, and an empty tracker. Upload `CONFIG.md` (and `STATE.md`, if you are on file round-trip) to the Project when it tells you to.

From then on, each new application is a new chat starting with a pasted URL or job description. `START_HERE_PROMPT.md` Part B has the first message for each kind of chat.

---

## How it feels to use

Every step ends with a deliverable and a question. You answer in a word. See `examples/anonymized_walkthrough.md` for a full application run; the user's replies are "Yes," "Go," "Proceed," and "Confirm SLO. Export, redacted."

If Claude launches into a long explanation instead of a two-line bootstrap, the files did not load. Check the Project knowledge and try again.

---

## Files

| File | What it is |
|---|---|
| `SYSTEM.md` | The engine. Rules, workflow, entry points. Read by Claude at the start of every chat. |
| `ONBOARDING.md` | First-time setup: builds your master, variants, CONFIG. |
| `CONFIG_TEMPLATE.md` | Becomes your `CONFIG.md`: targets, constraints, comp, contacts, style. |
| `STATE_TEMPLATE.md` | Becomes your `STATE.md`: where you are, what is open. |
| `START_HERE_PROMPT.md` | Project instructions (Part A) and first messages (Part B). |
| `modules/SOURCING.md` | Search profile and shortlist runs. |
| `modules/EVIDENCE_STANDARD.md` | What you may claim and how strongly. Levels A to D. |
| `modules/VOICE_GUIDE.md` | How to write and speak to employers. |
| `modules/INTERVIEW_PREP.md` | Panel maps, story bank, debriefs. |
| `modules/OUTREACH.md` | Every message to a person. |
| `modules/RED_TEAM_REVIEW.md` | Export to a second chatbot and import the critique. |
| `modules/DOCX_BUILD.md` | Resume file spec, build, and QA. |
| `templates/tracker.md` | The pipeline record. |
| `templates/cover_letter.md` | Letter skeleton. |
| `examples/anonymized_walkthrough.md` | One full application, fictional. |

---

## Privacy

You will be telling a chatbot your full career history. Before you start:

- Know your Claude data settings and whether memory is on.
- Do not share anything you would not put on a resume: no government ID numbers, no salary documents, no confidential employer material.
- The outside-review export defaults to redacted (your name and contacts replaced). Use full mode only for a reviewer you control.
- The system never puts your whole master into an export; only the lines a specific artifact uses.

## Employer AI policies

Some employers require that you write application answers yourself. When a posting says so, the system flags it at intake and switches to critique-and-edit mode for that employer. Respect it. The system is a coach, and a coach does not sit the exam.

---

## Contributing and feedback

Open an issue with what broke or what you changed. The roadmap is in `CHANGELOG.md`. The most useful contributions are learnings from real applications: which step failed, what the recruiter said, what you had to override.

## License

MIT. Copyright (c) 2026 Paul Lothridge. See `LICENSE`.
