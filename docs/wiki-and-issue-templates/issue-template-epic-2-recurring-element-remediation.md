# Issue Template: Epic 2 — Recurring Element Remediation

## What does this template do?

Guides the PM in creating one child fix-issue per recurring element (header,
nav, footer, etc.) and directs the developer to apply fixes for all WAVE
errors and alerts found in those elements during Epic 1.

## When should this template be used?

Use this template once Epic 1 is complete and the recurring-element findings
are documented in the audit spreadsheet. Create one issue per recurring
element using the child issue template embedded below.

---

## Labels

```
feature: Accessibility
```

## Title

```
Epic 2: WCAG Recurring Element Remediation — [REPLACE WITH PROJECT NAME]
```

## Body

```
<!-- Customize this epic issue by replacing all content in [ ] -->

### Overview

We need to fix all WAVE errors and alerts found in the recurring elements
(header, nav, footer, and any other site-wide elements) for
[REPLACE WITH PROJECT NAME] so that every page on the site inherits clean,
accessible shared components before individual page audits begin.

### Details
Project: [REPLACE WITH PROJECT NAME]
Recurring elements to remediate (from Epic 1 findings):
1. [REPLACE WITH RECURRING ELEMENT NAME — e.g., Global Header]
1. [REPLACE WITH RECURRING ELEMENT NAME — e.g., Global Footer]
1. [REPLACE WITH RECURRING ELEMENT NAME — e.g., Primary Navigation]
(add or remove rows as needed)

Audit Spreadsheet: [REPLACE WITH LINK TO AUDIT SPREADSHEET]

### Action Items

- [ ] For each recurring element listed above, create a child fix issue using
      the template in resource 1.05 and add it as a sub-issue below
- [ ] Assign each issue to a developer
- [ ] Once all child issues are closed, confirm with the developer that all
      recurring elements pass WAVE with no new errors (resource 1.03)
- [ ] Close this epic

### Sub-Issues

<!-- Add one sub-issue per recurring element once created -->

### Resources
- 1.01 WAVE Accessibility Audit Spreadsheet, tab: Audit Log:
       [REPLACE WITH LINK TO AUDIT SPREADSHEET]
- 1.02 [How to run the WAVE browser extension](https://hackforla.github.io/accessibility/getting-started/wave-browser-extension/)
- 1.03 [Perform a WAVE audit](https://hackforla.github.io/accessibility/getting-started/perform-wave-audit/)
- 1.04 [WCAG Known Issues and Solutions Index](https://hackforla.github.io/accessibility/known-issues-and-solutions/solutions-index/)

#### 1.05 Child Issue Template (one per recurring element)

Title
```
Dev: fix WAVE errors on [REPLACE WITH RECURRING ELEMENT NAME]
```
Body
```
### Overview
We need to fix all WAVE errors and alerts on the [REPLACE WITH RECURRING
ELEMENT NAME] for [REPLACE WITH PROJECT NAME] so that this recurring element
is WCAG compliant before individual page audits begin.

#### Details
Recurring Element: [REPLACE WITH ELEMENT NAME]
Representative page URL for testing: [REPLACE WITH URL]
User role required: [REPLACE WITH USER TYPE: visitor / user / admin / etc.]

### Action Items
- [ ] Review how to run the WAVE browser extension (resource 1.01)
   - [ ] Install the WAVE browser extension if not already installed
- [ ] Navigate to the representative page (resource 1.02.02)
- [ ] Open the audit spreadsheet and filter to this element (resource 1.03)
- [ ] Run WAVE with no elements focused or clicked (resource 1.01)
- [ ] Confirm all errors and alerts from the spreadsheet (resource 1.03) are visible
- [ ] For each error/alert:
   - [ ] Check the Known Issues Index for an existing solution (resource 1.04)
   - [ ] Apply the fix (following the known solution if one exists, or
         researching and implementing a new fix if not)
- [ ] Submit a PR and add the PR link to the audit spreadsheet row(s)
      for this element (resource 1.03)
- [ ] On this issue, add labels:
   - `ready for accessibility lead`
- [ ] Change status to: `Technical Review`

### Resources
- 1.01 [How to run the WAVE browser extension](https://hackforla.github.io/accessibility/getting-started/wave-browser-extension/)
- 1.02 Application details
   - 1.02.01 User Profile Required:
             [REPLACE WITH USER TYPE: visitor / user / admin / etc.]
   - 1.02.02 Representative page URL: [REPLACE WITH URL]
      - Requires sign in: [REPLACE WITH TRUE OR FALSE]
      - Can access page directly from URL: [REPLACE WITH TRUE OR FALSE]
- 1.03 WAVE Accessibility Audit Spreadsheet, tab: Audit Log,
       filter: [REPLACE WITH ELEMENT NAME]:
       [REPLACE WITH LINK TO SPREADSHEET]
   - Spreadsheet Row(s): [REPLACE WITH ROW NUMBERS]
- 1.04 [WCAG Known Issues and Solutions Index](https://hackforla.github.io/accessibility/known-issues-and-solutions/solutions-index/)
```
```
