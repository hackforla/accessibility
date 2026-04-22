# Issue Template: Epic 4 — Error & Alert Fixes (Epic of Epics)

## What does this template do?

Creates the top-level Epic 4 container issue. The PM uses it to track one
child fix-epic per distinct WAVE error or alert type found during Epic 3.
Each child epic is then created using one of the three Epic 4 sub-templates
(see resources 1.03.01–1.03.03).

## When should this template be used?

Use this template once, after Epic 3 is complete, to create the Epic 4
parent issue. Then use the appropriate sub-template for each individual
error/alert type depending on whether a solution already exists and how many
pages are affected.

---

## Labels

```
feature: Accessibility
```

## Title

```
Epic 4: WCAG Error & Alert Fixes — [REPLACE WITH PROJECT NAME]
```

## Body

```
<!-- Customize this epic issue by replacing all content in [ ] -->

### Overview

We need to fix all WAVE errors and alerts found during Epic 3 for
[REPLACE WITH PROJECT NAME]. This epic is a container (epic of epics) — each
child epic below targets one specific error or alert type across all pages
where it appears.

### Details
Project: [REPLACE WITH PROJECT NAME]
Audit Spreadsheet: [REPLACE WITH LINK TO AUDIT SPREADSHEET]

Error/alert types to fix (from Epic 3 audit spreadsheet):
| # | Category | Error/Alert Name | Pages Affected | Solution in Index? |
|---|----------|-----------------|---------------|-------------------|
| 1 | [CATEGORY] | [NAME] | [COUNT] | [YES / NO] |
| 2 | [CATEGORY] | [NAME] | [COUNT] | [YES / NO] |
(add or remove rows as needed)

### Action Items

- [ ] For each row in the table above, check the Known Issues Index
      (resource 1.02) to determine whether a solution exists
- [ ] For each error/alert type, create the appropriate child epic using
      the correct template (resource 1.03) and add it as a sub-issue below:
   - No solution exists, 1 page affected → use resource 1.03.01
   - No solution exists, 2+ pages affected → use resource 1.03.02
   - Solution already exists → use resource 1.03.03
- [ ] Assign each child epic to a developer
- [ ] Once all child epics are closed, close this epic

### Sub-Issues

<!-- Add one child fix-epic per error/alert type once created -->

### Resources
- 1.01 WAVE Accessibility Audit Spreadsheet, tab: Audit Log:
       [REPLACE WITH LINK TO AUDIT SPREADSHEET]
- 1.02 [WCAG Known Issues and Solutions Index](https://hackforla.github.io/accessibility/known-issues-and-solutions/solutions-index/)
- 1.03 Child epic issue templates
   - 1.03.01 Epic — create, apply & document solution (1 page):
             https://hackforla.github.io/accessibility/wiki-and-issue-templates/issue-template-epic-create-apply-and-document-solution-1page/
   - 1.03.02 Epic — create, apply & document solution (2+ pages):
             https://hackforla.github.io/accessibility/wiki-and-issue-templates/issue-template-epic-create-apply-and-document-solution-2pages-or-more/
   - 1.03.03 Epic — apply existing solution:
             https://hackforla.github.io/accessibility/wiki-and-issue-templates/issue-template-epic-apply-solution/
```
