# Application Tracker

One row per application. Created empty at the end of onboarding. Updated at every Live Fire step change and every outreach event. The permanent record; `STATE.md` holds only what is active.

Status values: Sourced / Intake / Triage / Leveling / Draft / Trace gate / Letter / Build / Submitted / Screen / HM / Panel / Onsite / Offer / Rejected / Withdrawn / No-Go / Closed by employer

| # | Company | Role title | Level | Location / remote | Link | Fit | Verdict | Leveling | Variant + imports | Route | Contact | Status | Submitted | Last activity | Next action | Outcome | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |

## Column notes

- **Fit**: the Step 2 score (1 to 10). Sourcing's provisional score goes in Notes until triage replaces it.
- **Verdict**: Go / Stretch / No-Go.
- **Leveling**: Down / At / Up, from Step 3.
- **Route**: referral via [name] / portal / both, with the order actually used.
- **Outcome**: filled at close. Include the stage reached and one line of feedback if any.
- **Notes**: recruiter guidance, reposts, employer AI policy, anything future-you needs at re-engagement.

## Weekly review (5 minutes)

Run `/status`. For each active row: is the next action still right, and is it overdue? Any row silent for ten business days gets a follow-up per `modules/OUTREACH.md` 2.5, once. Any row with an outcome not yet logged gets logged. Then run `/sourcing`.

---

*Opportunity System tracker template v1.0. MIT License. Copyright (c) 2026 Paul Lothridge.*
