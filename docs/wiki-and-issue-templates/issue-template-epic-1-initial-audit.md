# Issue Template: Epic 1 — Initial Audit

## What does this template do?

Directs the developer to inventory all pages and recurring elements (header,
nav, footer, etc.), run a WAVE audit on the recurring elements, and document
all findings in the project's audit spreadsheet.

## When should this template be used?

Use this template once, immediately after the Initiative is set up. Epic 1
must be complete before Epic 2 (Recurring Element Remediation) begins.

---

## Labels

```
feature: Accessibility
```

```
role: front-end
```

## Title

```
Epic 1: WCAG Initial Audit — [REPLACE WITH PROJECT NAME]
```

## Body

```
<!-- Customize this epic issue by replacing all content in [ ] -->

### Overview

We need to inventory all pages and recurring elements for
[REPLACE WITH PROJECT NAME], run WAVE audits on the recurring elements, and
document all findings in the audit spreadsheet so the team has a complete
picture of the site's accessibility state before remediation begins.

### Details
Project: [REPLACE WITH PROJECT NAME]
Site URL: [REPLACE WITH SITE URL]
Audit Spreadsheet: [REPLACE WITH LINK TO AUDIT SPREADSHEET]
Page Access by Role Spreadsheet: [REPLACE WITH LINK TO PAGE ACCESS SPREADSHEET]

### Action Items

#### Inventory
- [ ] Review the Page Access by Role spreadsheet (resource 1.01) to identify
      every page and every recurring element (e.g., header, nav, footer,
      sidebar)
- [ ] Confirm the spreadsheet (resource 1.01) lists all pages and update it
      if any are missing

#### WAVE Audit — Recurring Elements
- [ ] Review how to run the WAVE browser extension (resource 1.02)
- [ ] Install the WAVE browser extension if not already installed
- [ ] For each recurring element listed in the spreadsheet:
  - [ ] Load a representative page that contains the element
  - [ ] Run WAVE with no elements focused or clicked (resource 1.03)
  - [ ] Record all Errors, Contrast Errors, and Alerts for that element
        in the audit spreadsheet (resource 1.01.01)
  - [ ] Note the user role required to view the element (resource 1.01)

#### Documentation
- [ ] Ensure every recurring element's findings are logged in the spreadsheet
      (resource 1.01.01) with at minimum: page/element name, error/alert name,
      category, and user role
- [ ] Flag any pages that appear to require a non-default user role (resource 1.01)
      so the PM can plan audits accordingly
- [ ] Notify PM that Epic 1 is complete and the findings are ready for review

### Resources
- 1.01 Page Access by Role spreadsheet:
       [REPLACE WITH LINK TO PAGE ACCESS SPREADSHEET]
   - 1.01.01 WAVE Accessibility Audit Spreadsheet, tab: Audit Log:
             [REPLACE WITH LINK TO AUDIT SPREADSHEET]
- 1.02 [How to run the WAVE browser extension](https://hackforla.github.io/accessibility/getting-started/wave-browser-extension/)
- 1.03 [Perform a WAVE audit](https://hackforla.github.io/accessibility/getting-started/perform-wave-audit/)
- 1.04 [WCAG Known Issues and Solutions](https://hackforla.github.io/accessibility/known-issues-and-solutions/)
```
