# modules/OUTREACH.md

Every message the candidate sends to a person, as opposed to a portal: referral asks, follow-ups, thank-you notes, role-mapping requests, and close-outs. Triggered by `/outreach [contact or company]` and by Steps 8, 9, and 10.

Inherits `modules/VOICE_GUIDE.md`. Outreach is where enthusiasm filler and gratitude inflation creep back in; the forbidden-phrase list applies in full.

---

## 1. Principles

1. **Referral before portal.** If a contact exists, the ask goes out before the portal submission, and the portal submission waits for the contact's guidance on timing. Many applicant-tracking systems auto-close a duplicate record; a referral that lands after a portal application can be wasted.
2. **Make it easy to say yes.** Every ask includes the exact link, the one-pager attached or linked, a two-sentence summary of fit the contact can forward verbatim, and a stated out ("if it is not a fit for you to pass along, no problem").
3. **One ask per contact per role.** Do not stack requests. If the contact redirects (for example, "I am in a different division"), take the redirect and ask for role mapping instead.
4. **Contact budget is finite.** A warm contact spent on a No-Go role is gone for the Go role that appears next month. Triage before outreach, never after.
5. **Close every loop.** Every contact who helped hears the outcome, including rejections. The close-out is what makes the next ask possible.
6. **Log relationship state.** Every message and reply updates the Contacts table in `CONFIG.md` (strength, last touch, what they offered, what they declined) and the tracker row.

---

## 2. Message types and templates

All templates are skeletons. The assistant fills them from CONFIG, the tracker, and the Live Fire triage, in the candidate's register. Length guidance is firm; short outreach gets answered.

### 2.1 Referral ask (warm or close contact)

Subject: [Role title] at [Company]

> [Name], I am applying for [role title] on [team] at [Company] and wanted to ask whether you would be comfortable putting my name in.
>
> The short version of the fit: [one sentence, the strongest proof point in the JD's own terms]. [One sentence on the second proof point or the reason this role specifically.]
>
> Link to the posting: [URL]. One-pager attached. If it is easier, here are two lines you could forward as-is: "[two-sentence forwardable summary]."
>
> If it is not something you can pass along, no problem at all. Either way, it would be good to catch up.

Five to eight sentences. No apology for asking.

### 2.2 Referral ask (second-degree, via an intermediary)

To the intermediary:

> [Name], you mentioned you know [Contact] at [Company]. I am applying for [role] there and would value an introduction if you think it is appropriate. Here is a two-line summary you could forward: "[summary]." Posting: [URL]. Happy to send a one-pager if that helps.

To the second-degree contact, after the intro lands: a compressed 2.1 with a reference to the intermediary in the first sentence.

### 2.3 Role-mapping request (contact at a company with no matching req)

> [Name], I am looking at [Company] and the roles that map to what I do are probably [two or three title patterns]. Before I apply cold, would you be willing to point me at the team or hiring manager where that work actually lives? Two lines on me: "[summary]."

This is the right ask when triage returns No-Go on the posted req but the company is a fit.

### 2.4 Pre-interview ask (to recruiter or hiring manager)

> [Name], thank you for setting up the [stage] with [interviewers]. Is there anything you would want me to make sure I cover with each of them, or anything to steer clear of? It helps me use their time well.

Two sentences. Send as soon as the panel is named.

### 2.5 Status follow-up (no response after a submission or a stage)

Timing: seven to ten business days after the last activity, once. A second follow-up only if a date was promised and missed.

> [Name], checking in on the [role] process. I remain interested and wanted to make sure nothing is needed from my side. If the timeline has shifted, that is useful to know too.

Three sentences. No "just," no "sorry to bother."

### 2.6 Thank-you (after any interview stage)

Within 24 hours. `VOICE_GUIDE.md` 4.8.

> [Name], thank you for the conversation [day]. [One specific thing they said or asked that the candidate has thought about since, with a sentence of what they think now.] [If the debrief surfaced a concern: one or two sentences adding the point or clarification, stated as a fact, not a defense.] [Close on the work: one sentence on what the candidate would want to do first in the role.]

Three to five sentences. One per interviewer where emails are known; otherwise one to the recruiter with a request to forward.

### 2.7 Close-out after rejection (to the hiring manager or recruiter)

> [Name], thank you for letting me know. I enjoyed learning about [specific thing about the team or problem]. If the team's needs change or a related role opens, I would welcome hearing about it.

Three sentences. No request for feedback in the same note; if feedback is wanted, a separate short note a few days later.

### 2.8 Close-out to a contact who referred (any outcome)

> [Name], wanted to close the loop: [outcome, one sentence]. Thank you for [what they did specifically]. [If rejected: one sentence on what was learned or where the process ended, without complaint.] [If advanced or hired: one sentence on next step.]

This note is not optional. It is the deposit that makes the next withdrawal possible.

### 2.9 Recruiter decline (candidate withdrawing)

> [Name], thank you for the time on [role]. I have decided not to continue in the process because [one honest sentence: level, location, comp, or fit]. I appreciated the conversations and would be glad to stay in touch.

---

## 3. Sequencing for one application

1. Triage returns Go or Stretch. Check Contacts.
2. Contact exists: send 2.1 or 2.2. Wait for guidance on timing before portal submission. Log.
3. No contact: portal submission per Step 8. Log.
4. Silence at ten business days: 2.5, once. Log.
5. Interview scheduled: 2.4 to the recruiter. Prep per `INTERVIEW_PREP.md`.
6. After each stage: 2.6 within 24 hours. Log.
7. Outcome: 2.7 to the company, 2.8 to any contact. Log. Update the Contacts table.

---

## 4. Contact table maintenance

After every message or reply, update the row in `CONFIG.md`:

| Name | Company | Relationship | Strength | Last touch | Offered | Declined | Notes |

"Offered" and "Declined" are what makes the table useful six months later. A contact who declined to refer but offered role mapping is a different asset from one who referred once and went quiet.

Flag any contact likely to leave their company soon. Referral timing becomes urgent, and the asset expires.

---

## 5. What not to send

- A message that could be sent to any company. Run the competitor-substitution test.
- A referral ask with no link, no summary, and no out.
- A second follow-up with no new information.
- A thank-you that thanks and nothing else.
- Anything with a forbidden phrase from `VOICE_GUIDE.md` section 5.
- Anything the candidate has not read.

---

*Opportunity System Outreach v1.0. MIT License. Copyright (c) 2026 Paul Lothridge.*
