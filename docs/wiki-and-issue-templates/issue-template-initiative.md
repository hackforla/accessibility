# Issue Template: Initiative (PM Setup)

## What does this template do?

Creates the top-level Initiative issue that kicks off the entire WCAG compliance
workflow for a project. The PM uses this issue to track the creation of Google
Drive assets and the five child Epics that make up the full workflow.

## When should this template be used?

Use this template once, at the very start of the accessibility remediation effort
for a project, before any auditing or fixing work begins.

---

## Labels

```
feature: Accessibility
```
```
role: pm
```
```
size: 0.25pt
```
```
priority: MUST HAVE
```
```
milestone: missing
```
```
level: easy
```

## Title

```
Initiative: WCAG Compliance — [REPLACE WITH PROJECT NAME]
```

## Body

```
<!-- Customize this initiative issue by replacing all content in [ ] -->

### Overview

We need to set up the WCAG compliance workflow for [REPLACE WITH PROJECT NAME]
so that the team can systematically audit and fix accessibility issues across
the site and bring it into WCAG compliance.

### Action Items

#### Google Drive Setup
- [ ] Open the team's Google Drive (resource 1.01) and create a new folder
      called "Accessibility Project"; update resource 1.01.01 with the folder link
- [ ] Create the **[PROJECT NAME] WAVE Accessibility Audit Spreadsheet**
      from the shared template and save it in the Accessibility Project folder
      (resource 1.01.01); update resource 1.02.01 with the spreadsheet link
      - Columns are pre-named with data validation already set up;
        no content needs to be added yet
- [ ] Create the **Page Access by Role** spreadsheet from the shared template
      and save it in the Accessibility Project folder (resource 1.01.01); update
      resource 1.02.02 with the spreadsheet link
      - List all pages and global features with the user roles required
        to access each one

#### GitHub Setup
- [ ] Create Epic 1 — Initial Audit (resource 1.03.01) and add as a sub-issue
      to this Initiative
- [ ] Create Epic 2 — Recurring Element Remediation (resource 1.03.02) and add
      as a sub-issue to this Initiative
- [ ] Create Epic 3 — Page Audits (resource 1.03.03) and add as a sub-issue
      to this Initiative
- [ ] Create Epic 4 — Error & Alert Fixes (resource 1.03.04) and add as a
      sub-issue to this Initiative
- [ ] Create Epic 5 — Ongoing Audit Cycle (resource 1.03.05) and add as a
      sub-issue to this Initiative


### Resources
- 1.01 [REPLACE WITH LINK TO TEAM'S GOOGLE DRIVE]
   - 1.01.01 Accessibility Project folder:
             [REPLACE WITH LINK TO FOLDER ONCE CREATED]
- 1.02 Spreadsheets
   - 1.02.01 [[PROJECT NAME] WAVE Accessibility Audit Spreadsheet](REPLACE WITH LINK TO SPREADSHEET ONCE CREATED)
   - 1.02.02 [[PROJECT NAME] Page Access by Role spreadsheet](REPLACE WITH LINK TO SPREADSHEET ONCE CREATED)
- 1.03 Epic issue templates
   - 1.03.01 Epic 1 — Initial Audit:
             [REPLACE WITH LINK TO EPIC 1 ISSUE ONCE CREATED]
   - 1.03.02 Epic 2 — Recurring Element Remediation:
             [REPLACE WITH LINK TO EPIC 2 ISSUE ONCE CREATED]
   - 1.03.03 Epic 3 — Page Audits:
             [REPLACE WITH LINK TO EPIC 3 ISSUE ONCE CREATED]
   - 1.03.04 Epic 4 — Error & Alert Fixes:
             [REPLACE WITH LINK TO EPIC 4 ISSUE ONCE CREATED]
   - 1.03.05 Epic 5 — Ongoing Audit Cycle:
             [REPLACE WITH LINK TO EPIC 5 ISSUE ONCE CREATED]
- 1.04 [WCAG Compliance Workflow Overview](https://hackforla.github.io/accessibility/getting-started/hackforla-wcag-compliance-workflow-system-overview/)
```

---

- Page Status: Complete
- Authors: 
    - Bonnie Wolfe
    - Rabia Shaikh
