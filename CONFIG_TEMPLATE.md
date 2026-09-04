# CONFIG.md

User-specific settings for the Opportunity System. Completed during Onboarding Step 4. The assistant reads this at every bootstrap. Edit freely; nothing here is locked.

Fields marked REQUIRED must be filled before Live Fire runs.

---

## Identity

- **Full name** (REQUIRED): 
- **Filename form** (REQUIRED, `First_Last`): 
- **Location** (REQUIRED, as it should appear on the resume): 
- **Phone**: 
- **Email**: 
- **LinkedIn URL**: 
- **Other links** (portfolio, GitHub, publications): 

## Status line

- **Current status** (REQUIRED, one line for the resume header; examples: "Open to new opportunities," "Currently consulting," "Co-founder, [venture], and open to the right full-time role"): 
- **Most recent role ended**: 

## Targets

List one to three role families. Each becomes a variant.

| # | Role family (title range) | Level | Variant filename |
|---|---|---|---|
| 1 |  | IC / Manager / Director / Executive |  |
| 2 |  |  |  |
| 3 |  |  |  |

- **Primary target** (REQUIRED, the number above): 
- **Industries or domains preferred**: 
- **Industries or domains excluded**: 
- **Company stage preference** (startup, growth, enterprise, any): 

## Constraints

- **Remote stance** (REQUIRED: remote only / hybrid OK / onsite OK): 
- **Commutable radius**: 
- **Relocation** (REQUIRED: no / yes / yes for these locations only): 
- **Travel tolerance**: 
- **Work authorization** (REQUIRED, exactly as it should be answered on a portal): 
- **Start date availability**: 

## Compensation

- **Floor** (below this, No-Go regardless of fit): 
- **Target**: 
- **Portal answer when a number is required** (a range or a single figure): 
- **Portal answer when a text field allows it** (for example "Open to discussing based on total compensation and scope"): 

## Education (REQUIRED, verbatim)

Copied character for character from the locked master. Every artifact is checked against this block. If this block is wrong, every resume is wrong.

```
[Institution]
[Degree, Major, Honors]
[Additional credential]
```

## Certifications

| Certification | Issuer | Year | Current or lapsed |
|---|---|---|---|
|  |  |  |  |

Lapsed certifications render with the year only.

## Companies

- **Excluded** (do not source or intake): 
- **Prior history to flag at intake** (company, req, outcome, guidance received):
  - 

## Contacts

Referral and warm contacts. The assistant checks this at intake and proposes referral routing before portal submission.

| Name | Company | Relationship | Strength (warm / close) | Notes |
|---|---|---|---|---|
|  |  |  |  |  |

## Style

Defaults from `SYSTEM.md` 8.3 apply unless overridden here.

- **Em-dash rule** (default: none in employer-facing artifacts): 
- **Additional forbidden phrases**: 
- **Phrases the user wants kept** (things the default list would strip but the user uses deliberately): 
- **Font** (default per DOCX_BUILD): 
- **Page target** (default 2): 
- **Communication style** (default: terse, numbered, decisions labeled): 

## Persistence

- **Mode** (set at bootstrap: connector / built-in memory / file round-trip): 
- **Connector name, if any**: 

## Employer AI policies

Companies that require candidate-authored written answers, discovered at intake. The assistant critiques and edits only for these.

- 

---

*Opportunity System CONFIG template v1.0. MIT License. Copyright (c) 2026 Paul Lothridge.*
