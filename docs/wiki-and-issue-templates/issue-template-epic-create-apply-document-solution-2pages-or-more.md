# Issue Template: Epic 4 Sub-Template — Create, Apply & Document Solution (2+ Pages)

## What does this template do?

Creates a child fix-epic inside Epic 4. The scope of work is to research and
develop a new solution for one specific WAVE error or alert, apply it to the
first affected page, document the solution in the Known Issues Index, then
create individual fix issues for every remaining affected page.

## When should this template be used?

Use this template inside Epic 4 when:

- There is **no solution** in the [Known Issues and Solutions Index](https://hackforla.github.io/accessibility/known-issues-and-solutions/solutions-index/), **and**
- **2 or more pages** are known to be affected.

If this is not the correct template, see the [Wiki and Issue Templates page](https://hackforla.github.io/accessibility/wiki-and-issue-templates/) for all available templates.

---

## Labels

```
feature: Accessibility
```

```
p-feature: [REPLACE WITH PAGE NAME(S)]
```

## Title

```
Epic: WAVE: [REPLACE WITH ONE OF: Alert / Contrast Error / Error]: [REPLACE WITH NAME OF Alert/Contrast Error/Error]
```

## Body

```
<!-- Customize this epic issue by replacing all content in [ ] -->

### Overview

We need to research, create, and document a solution for
[REPLACE WITH ONE OF: Alert / Contrast Error / Error]:
[REPLACE WITH NAME OF Alert/Contrast Error/Error] and apply it to all affected
pages so the site can be WCAG compliant and so the solution is available for
future teams.

### Details
Category: [REPLACE WITH ONE OF: Alert / Contrast Error / Error]
Name: [REPLACE WITH NAME OF Alert/Contrast Error/Error]
(The Known Issues Index has no solution yet for this issue)

Known pages (there might be others):
1. [REPLACE WITH PAGE NAME 1]
1. [REPLACE WITH PAGE NAME 2]
(add or remove rows as needed)

This epic will:
- Create a document+fix issue for the first page to develop and document the
  solution
- Once that solution is accepted, create individual fix issues for each
  remaining page using the existing-solution template

### Action Items
- [ ] Go to the Known Issues Solutions Index (resource 1.02) and add the link
      to the specific solutions page for this issue as resource 1.02.01
- [ ] Copy the first-page child issue template (resource 1.04) and create a
      new issue for `[REPLACE WITH FIRST PAGE NAME]`
   - [ ] Add the following labels to the new child issue:
      - `role: front-end`
      - `size: missing`
      - `p-feature: [REPLACE WITH FIRST PAGE NAME]`
      - `feature: Accessibility`
      - `level: missing`
      - `ready for dev lead`
      - `priority: MUST HAVE`
   - [ ] Add milestone: [REPLACE WITH MILESTONE NAME, if applicable]
   - Customize the child issue resources:
      - [ ] Update the child issue's resource 1.02.01 and 1.02.02 using
            the application details for the first page
      - [ ] Find the spreadsheet row for this page and error, and update
            the child issue's resource 1.03 with the correct link and
            row number(s)
- [ ] Add the new issue as a sub-issue of this epic
- [ ] Once the first-page issue is merged and the wiki is updated, create one
      fix issue per remaining page using the
      [Epic: Apply code solution for 1 or more pages](https://hackforla.github.io/accessibility/wiki-and-issue-templates/issue-template-epic-apply-solution/)
      child issue template and add each as a sub-issue below
- [ ] Once all sub-issues are closed, run WAVE on all other pages for this
      [REPLACE WITH ONE OF: Alert / Contrast Error / Error] only — ignore all
      other errors and alerts. Check user interaction states as well.
   - [ ] No additional instances found — close this epic
   - [ ] Additional instances found — create new fix issues and add as
         sub-issues

### Sub-Issues

<!-- Add child issues as they are created -->

### Resources
- 1.01 WAVE Accessibility Audit Spreadsheet, tab: Audit Log:
       [REPLACE WITH LINK TO AUDIT SPREADSHEET]
   - 1.01.01 Audit Spreadsheet, filter:
             [REPLACE WITH FILTER NAME FOR THIS ALERT/ERROR]
- 1.02 [WCAG Known Issues and Solutions](https://hackforla.github.io/accessibility/known-issues-and-solutions/)
   - 1.02.01 https://hackforla.github.io/accessibility/known-issues-and-solutions/solutions-index/[REPLACE WITH SLUG-WITH-DASHES]/
- 1.03 Project documentation / page inventory:
       [REPLACE WITH LINK TO YOUR PROJECT'S PAGE DOCS OR WIKI]
   - 1.03.01 Documentation for [REPLACE WITH PAGE NAME] page:
             [REPLACE WITH LINK OR LEAVE BLANK]

#### 1.04 Child Issue Template (first page — creates the solution)

Title
```
Dev: fix [REPLACE WITH Alert/Contrast Error/Error] on [REPLACE WITH FIRST PAGE NAME] page and document solution
```
Body
```
### Overview
We need to fix the [REPLACE WITH ONE OF: Alert / Contrast Error / Error]:
[REPLACE WITH NAME OF Alert/Contrast Error/Error] on [REPLACE WITH PAGE NAME]
and document the solution in the Known Issues Index so it can be reused for
the remaining affected pages.

#### Details
Category: [REPLACE WITH ONE OF: Alert / Contrast Error / Error]
Name: [REPLACE WITH NAME OF Alert/Contrast Error/Error]
(No solution exists in the Known Issues Index yet — this issue will create one)

Page to fix:
[REPLACE WITH PAGE NAME]

Additional pages affected (to be fixed in follow-on issues once this is
merged):
- [REPLACE WITH OTHER PAGE NAMES]

### Action Items
- [ ] Review how to run the WAVE browser extension (resource 1.01)
   - [ ] Install the WAVE browser extension if not already installed
- [ ] Log in as the required user role (resource 1.02.01)
- [ ] Navigate to the page (resource 1.02.02)
- [ ] Open the audit spreadsheet and find the row for this page and error
      (resource 1.03)
- [ ] Run WAVE with no elements focused or clicked (resource 1.04)
- [ ] Locate the [REPLACE WITH ONE OF: Alert / Contrast Error / Error] in the
      WAVE output
- [ ] Research a solution; if related issues have been solved on other pages,
      review those PRs for guidance (resource 1.05.01)
- [ ] Apply the solution
- [ ] Document the solution in the Known Issues Index wiki page for this error
      (resource 1.05.01) — add it to the `Project Team Solution` section
- [ ] Submit a PR and include the link to the `Project Team Solution` section
      (resource 1.05.01.01) in the PR description
- [ ] Add the PR link to the audit spreadsheet in the PR column for this row
      (resource 1.03)
- [ ] On this issue, add labels:
   - `ready for accessibility lead`
   - `ready for product`
- [ ] Change status to: `Technical Review`
- [ ] Get sign-off on the wiki solution page from:
   - [ ] Accessibility lead
   - [ ] Product lead
- [ ] Release dependencies on:
   - [INSERT LINK TO NEXT ISSUE(S)]
   - [INSERT LINK TO EPIC]

### Resources
- 1.01 [How to run the WAVE browser extension](https://hackforla.github.io/accessibility/getting-started/wave-browser-extension/)
- 1.02 Application details
   - 1.02.01 User Profile Required:
             [REPLACE WITH USER TYPE: visitor / user / admin / etc.]
   - 1.02.02 Page URL: [REPLACE WITH PAGE URL]
      - Requires sign in: [REPLACE WITH TRUE OR FALSE]
      - Can access page directly from URL: [REPLACE WITH TRUE OR FALSE]
- 1.03 WAVE Accessibility Audit Spreadsheet, tab: Audit Log,
       filter: [REPLACE WITH FILTER NAME]:
       [REPLACE WITH LINK TO SPREADSHEET]
   - Spreadsheet Row(s): [REPLACE WITH ROW NUMBERS]
- 1.04 [Perform a WAVE audit](https://hackforla.github.io/accessibility/getting-started/perform-wave-audit/)
- 1.05 [WCAG Known Issues and Solutions Index](https://hackforla.github.io/accessibility/known-issues-and-solutions/solutions-index/)
   - 1.05.01 WAVE Known Accessibility Issue:
             [REPLACE WITH ONE OF: Alert / Contrast Error / Error] —
             [REPLACE WITH NAME OF Alert/Contrast Error/Error]:
             [REPLACE WITH WIKI PAGE LINK]
      - 1.05.01.01 Project Team Solution section:
                   [REPLACE WITH DIRECT ANCHOR LINK TO SOLUTION SECTION]
```
```
