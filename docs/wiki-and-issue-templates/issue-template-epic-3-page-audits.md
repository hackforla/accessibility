# Issue Template: Epic 3 — Page Audits

## What does this template do?

Guides the PM in creating one audit issue per page and directs the developer
to run WAVE on each page and log all findings in the audit spreadsheet.
**No fixes are applied during Epic 3** — this is an audit-only phase.

## When should this template be used?

Use this template after Epic 2 is complete. Create one child audit issue per
page using the child issue template embedded below.

---

## Labels

```
feature: Accessibility
```

## Title

```
Epic 3: WCAG Page Audits — [REPLACE WITH PROJECT NAME]
```

## Body

```
<!-- Customize this epic issue by replacing all content in [ ] -->

### Overview

We need to run a WAVE audit on every page of [REPLACE WITH PROJECT NAME] and
document all errors and alerts in the audit spreadsheet so the team has a
complete and current issue inventory before fix work (Epic 4) begins.

No fixes should be applied during this epic — document only.

### Details
Project: [REPLACE WITH PROJECT NAME]
Site URL: [REPLACE WITH SITE URL]
Audit Spreadsheet: [REPLACE WITH LINK TO AUDIT SPREADSHEET]

Pages to audit (from Page Access by Role spreadsheet):
1. [REPLACE WITH PAGE NAME]
1. [REPLACE WITH PAGE NAME]
(add or remove rows as needed)

### Action Items

- [ ] For each page listed above, create a child audit issue using the
      template in resource 1.05 and add it as a sub-issue below
- [ ] Assign issues to developers
- [ ] Once all child issues are closed, confirm all pages have been logged
      in the audit spreadsheet (resource 1.02)
- [ ] Notify PM that Epic 3 is complete — PM will proceed to create Epic 4
      fix epics based on the spreadsheet findings (resource 1.02)
- [ ] Close this epic

### Sub-Issues

<!-- Add one sub-issue per page once created -->

### Resources
- 1.01 Page Access by Role spreadsheet:
       [REPLACE WITH LINK TO PAGE ACCESS SPREADSHEET]
- 1.02 WAVE Accessibility Audit Spreadsheet, tab: Audit Log:
       [REPLACE WITH LINK TO AUDIT SPREADSHEET]
- 1.03 [How to run the WAVE browser extension](https://hackforla.github.io/accessibility/getting-started/wave-browser-extension/)
- 1.04 [Perform a WAVE audit](https://hackforla.github.io/accessibility/getting-started/perform-wave-audit/)

#### 1.05 Child Issue Template (one per page)

Title
```
Dev: WAVE audit — [REPLACE WITH PAGE NAME] page
```
Body
```
### Overview
We need to run a WAVE audit on the [REPLACE WITH PAGE NAME] page for
[REPLACE WITH PROJECT NAME] and log all findings in the audit spreadsheet
so errors and alerts can be fixed in Epic 4.

**Do not apply any fixes during this issue — document only.**

#### Details
Page: [REPLACE WITH PAGE NAME]
Page URL: [REPLACE WITH PAGE URL]
User role required: [REPLACE WITH USER TYPE: visitor / user / admin / etc.]

### Action Items
- [ ] Review how to run the WAVE browser extension (resource 1.01)
   - [ ] Install the WAVE browser extension if not already installed
- [ ] Log in as the required user role (resource 1.02.01)
- [ ] Navigate to the page (resource 1.02.02)
- [ ] Run WAVE with no elements focused or clicked (resource 1.01)
- [ ] Check user interactions on the page (dropdowns, modals, accordions, etc.)
      and re-run WAVE for each interaction state to catch hidden errors
      (resource 1.03)
- [ ] Log all Errors, Contrast Errors, and Alerts in the audit spreadsheet
      (resource 1.04) including:
   - Page name
   - Error/alert category and name
   - Number of instances
   - Any relevant notes
- [ ] On this issue, add label: `ready for pm`
- [ ] Close this issue

### Resources
- 1.01 [How to run the WAVE browser extension](https://hackforla.github.io/accessibility/getting-started/wave-browser-extension/)
- 1.02 Application details
   - 1.02.01 User Profile Required:
             [REPLACE WITH USER TYPE: visitor / user / admin / etc.]
   - 1.02.02 Page URL: [REPLACE WITH PAGE URL]
      - Requires sign in: [REPLACE WITH TRUE OR FALSE]
      - Can access page directly from URL: [REPLACE WITH TRUE OR FALSE]
- 1.03 [Perform a WAVE audit](https://hackforla.github.io/accessibility/getting-started/perform-wave-audit/)
- 1.04 WAVE Accessibility Audit Spreadsheet, tab: Audit Log:
       [REPLACE WITH LINK TO SPREADSHEET]
   - Spreadsheet Row(s): [REPLACE WITH ROW NUMBERS IF ALREADY KNOWN]
```
```
