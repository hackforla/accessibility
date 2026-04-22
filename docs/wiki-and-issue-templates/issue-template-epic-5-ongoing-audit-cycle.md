# Issue Template: Epic 5 — Ongoing Audit Cycle

## What does this template do?

Creates the Epic 5 issue that drives the final (and ongoing) re-audit of all
pages. If errors are found, the developer reports the affected pages and the
PM creates new Epic 3/4 issues to address them. If no errors remain, this epic
becomes the final sign-off that marks the Initiative complete.

## When should this template be used?

Use this template once Epic 4 is complete (all known errors and alerts have
been fixed). Epic 5 repeats as a loop until a clean audit is achieved.

---

## Labels

```
feature: Accessibility
```

## Title

```
Epic 5: WCAG Ongoing Audit & Sign-Off — [REPLACE WITH PROJECT NAME]
```

## Body

```
<!-- Customize this epic issue by replacing all content in [ ] -->

### Overview

We need to re-audit all pages of [REPLACE WITH PROJECT NAME] with WAVE to
confirm that all previously identified errors and alerts have been resolved.
If new or remaining issues are found, the team will loop back through the
Epic 3 and Epic 4 workflow. If no issues are found, this epic serves as the
final accessibility sign-off and closes the Initiative.

### Details
Project: [REPLACE WITH PROJECT NAME]
Site URL: [REPLACE WITH SITE URL]
Audit Spreadsheet: [REPLACE WITH LINK TO AUDIT SPREADSHEET]

### Action Items

#### Re-Audit
- [ ] Create a child re-audit issue using the template in resource 1.04 and
      add it as a sub-issue below
- [ ] Assign the re-audit issue to a developer

#### Review Findings
After the re-audit issue is closed, check the result:

- [ ] **Errors found** — PM creates new Epic 3 and/or Epic 4 issues for the
      affected pages (resources 1.05, 1.06), links them here as sub-issues,
      and repeats this epic when those issues are resolved
- [ ] **No errors found** — proceed to sign-off below

#### Sign-Off (complete only when re-audit is clean)
- [ ] Accessibility lead reviews and signs off
- [ ] Product lead reviews and signs off
- [ ] Add label: `accessibility: complete`
- [ ] Close this epic
- [ ] Close the parent Initiative issue

### Sub-Issues

<!-- Add the re-audit issue and any follow-on fix issues here -->

### Resources
- 1.01 WAVE Accessibility Audit Spreadsheet, tab: Audit Log:
       [REPLACE WITH LINK TO AUDIT SPREADSHEET]
- 1.02 [How to run the WAVE browser extension](https://hackforla.github.io/accessibility/getting-started/wave-browser-extension/)
- 1.03 [Perform a WAVE audit](https://hackforla.github.io/accessibility/getting-started/perform-wave-audit/)
- 1.04 See child issue template below
- 1.05 Epic 3 issue template:
       [REPLACE WITH LINK TO YOUR EPIC 3 ISSUE OR TEMPLATE]
- 1.06 Epic 4 issue template:
       [REPLACE WITH LINK TO YOUR EPIC 4 ISSUE OR TEMPLATE]

#### 1.04 Child Issue Template (re-audit)

Title
```
Dev: WAVE re-audit — all pages — [REPLACE WITH PROJECT NAME]
```
Body
```
### Overview
We need to re-audit all pages of [REPLACE WITH PROJECT NAME] with WAVE to
confirm that all previously identified WAVE errors and alerts have been
resolved.

### Action Items
- [ ] Review how to run the WAVE browser extension (resource 1.01)
   - [ ] Install the WAVE browser extension if not already installed
- [ ] For each page in the audit spreadsheet (resource 1.02):
   - [ ] Log in as the required user role (from spreadsheet, resource 1.02)
   - [ ] Navigate to the page (resource 1.02)
   - [ ] Run WAVE with no elements focused or clicked (resource 1.03)
   - [ ] Check user interaction states (dropdowns, modals, accordions, etc.)
         and re-run WAVE for each (resource 1.03)
   - [ ] Record results in the audit spreadsheet (resource 1.02) — note any
         remaining or new Errors, Contrast Errors, or Alerts
- [ ] After auditing all pages, check one of the following:
   - [ ] **No errors or alerts found** — add label `ready for accessibility lead`,
         change status to `Technical Review`, and notify PM
   - [ ] **Errors or alerts found** — list the affected pages and error names
         in a comment on this issue, add label `ready for pm`, and notify PM
         so they can create new Epic 3/4 issues

### Resources
- 1.01 [How to run the WAVE browser extension](https://hackforla.github.io/accessibility/getting-started/wave-browser-extension/)
- 1.02 WAVE Accessibility Audit Spreadsheet:
       [REPLACE WITH LINK TO AUDIT SPREADSHEET]
- 1.03 [Perform a WAVE audit](https://hackforla.github.io/accessibility/getting-started/perform-wave-audit/)
- 1.04 [WCAG Known Issues and Solutions Index](https://hackforla.github.io/accessibility/known-issues-and-solutions/solutions-index/)
```
```
