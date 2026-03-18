# Issue Template for Epic to apply solution

## What does this template do?
This issue template creates an epic issue and will direct the person working on the epic issue in how to create child issues (using a template that is customized during the epic creation). The scope of work of the epic will fix a specific Alert/Aria/Contrast Error/Error found on your website.

## When should this template be used?
- Only use this template if there is a solution in the index.
- If this is not the correct template, see [WIKI and Issue templates](index.md) for a list of other templates available.   

## Template

### Labels
Add the following labels and any missing labels that apply
```
feature: Accessibility
```
```
p-feature: [REPLACE WITH PAGE NAME(s)]
```
### Title
```
Epic: WAVE: [REPLACE WITH Alert/Aria/Contrast Error/Error]
```
### Body

`````
### Overview
We need to make issues that will apply a solution for [REPLACE WITH Alert/Aria/Contrast Error/Error] so that it can get fixed across the site.

### Details
Category: [REPLACE WITH ONE OF THESE CATEGORIES Alert/Aria/Contrast Error/Error]
Name: [REPLACE WITH NAME OF Alert/Aria/Contrast Error/Error]
(There is already a solution for this issue, it just needs to be applied to the pages)

known pages (there might be others):
1. [REPLACE WITH NAME OF PAGE NAME 1]
1. [REPLACE WITH NAME OF PAGE NAME N]

This epic will do the following
- create issues to fix any occurrences of this problem

### Action Items
- [ ] Go to the Solutions Index (resource 1.02) and add the link to the specific page for this problem 1.02.01
- [ ] Copy the issue template (resource 1.04)
- [ ] Use the template content to create a new issue(s) for the pages under Known pages above
- [ ] Customize the draft
   - [ ] Add the following labels
      - role: front-end
      - size: missing
      - p-feature: [REPLACE WITH FIRST PAGE NAME]
      - feature: Accessibility
      - level: missing
      - deck: add to staging
      - ready for dev lead
      - priority: MUST HAVE
   - Customize the draft issue resoures
      - [ ] In this issue use the content in resource Product Documentation 1.03.01 to update the draft's issue resource 1.02.01, 1.02.02
      - [ ] In this issue use the content in resource 1.01.01 (spreadsheet) to update the link to the spreadsheet in draft issue's resource 1.03
         - [ ] open the spreadsheet link and find the row number, and add it to the draft issues's resource 1.03.01
- [ ] Once all the issues are closed, run WAVE and check all other pages for this alert; ignore all other alerts.  Check user interactions on the page to ensure that the alert isn't hidden by an interaction. Check one of the following below:
   - [ ] No additional instances of this alert found
   - [ ] New instances of these alerts found
      - [ ] Make additional issues


### Resources
- 1.01 [TDM WAVE Accessibility Audit Spreadsheet, tab: 2. Audit Log](https://docs.google.com/spreadsheets/d/1qiAqR9LH-Gd4LO3aOs0yUy174o5LOmnuU6Bz671mKsY/edit?gid=0#gid=0)
   - 1.01.01 [TDM WAVE Accessibility Audit Spreadsheet, tab: 2. Audit Log, filter: [REPLACE WITH NAME OF FILTER FOR Alert/Aria/Contrast Error/Error]
- 1.02 [WCAG: Known Issues and Solutions](https://hackforla.github.io/accessibility/known-issues-and-solutions)
  - 1.02.01 https://hackforla.github.io/accessibility/known-issues-and-solutions/solutions-index/[REPLACE WITH PAGE NAME WITH DASHES]/
- 1.03 WIKI: Product Documentation: https://github.com/hackforla/tdm-calculator/wiki/Product-Documentation
   - 1.03.01 WIKI: Product Documentation, [REPLACE WITH PAGE NAME] page: 

#### 1.04 Issue Template
Title
```
Dev: fix [REPLACE WITH Alert/Aria/Contrast Error/Error] on [REPLACE WITH PAGE NAME] page
```
Body
````
### Overview
We need to fix the Alert: [REPLACE WITH Alert/Aria/Contrast Error/Error](s) on [REPLACE WITH PAGE NAME] so that page can be WCAG compliant.

#### Details
Category: [REPLACE WITH ONE OF THESE CATEGORIES Alert/Aria/Contrast Error/Error]
Name: [REPLACE WITH NAME OF Alert/Aria/Contrast Error/Error]
(The Accessibility wiki for this Alert has a solution)

Page that will be worked on:
[REPLACE WITH NAME OF PAGE NAME]

### Action Items
- [ ] Review wiki page: Accessibility, How to run the WAVE browser extension (Resource 1.01)
   - [ ] Install the WAVE browser extension
- [ ] Log in as the user indicated (resource 1.02.01) 
- [ ] navigate to the page you are going to fix (resource 1.02.02)
- [ ] Open the TDM WAVE Accessibility Audit Spreadsheet, for this Alert (resource 1.03) and find the row that relates to this  issues page.
- [ ] Run the WAVE extension with no elements focused, or clicked
- [ ] Find the Alert referenced in the Spreadsheet (1.03)
- [ ] This alert has been resolved on other pages, so review `Project Team Solution` section (resource 1.04.01.01)
- [ ] Apply solution
- [ ] Submit PR
- [ ] Add PR to spreadsheet in PR column next to Alert (resource 1.03)
- [ ] On this issue
   - [ ] Add labels: 
      - `ready for accessibility lead`
   - [ ] Change status to: `Technical Review`
   - to the epic #2897
     - [ ] Add the label `ready for product`
      - [ ] Add this comment 
         ```
          - [#REPLACE WITH THIS ISSUE NUMBER] is closed.  Please review to see if there are any remaining instances of this problem
         ```

### Resources/Instructions
- 1.01[How to run the WAVE browser extension](https://github.com/hackforla/accessibility/blob/main/docs/getting-started/wave-browser-extension.md)
- 1.02 Application details
   - 1.02.01 User Profile Required: [REPLACE WITH USER TYPE: visitor (not logged in)/user/admin/security admin/]
   - 1.02.02 Page URL: http://tdm-dev.azurewebsites.net/[REPLACE WITH PAGE URL]
      - Requires sign in: [REPLACE WITH TRUE OR FALSE]
      - Can access page directly from URL: [REPLACE WITH TRUE OR FALSE]
- 1.03 [TDM WAVE Accessibility Audit Spreadsheet, tab: 2. Audit Log, filter: Alert: [REPLACE WITH FILTER NAME]]
   -  Spreadsheet Row(s): [REPLACE WITH ROW NUMBERS]
- 1.04 [Accessibility Known Issues Index](https://github.com/hackforla/accessibility/blob/main/docs/known-issues-and-solutions/solutions-index/index.md)
    - 1.04.01 [WAVE Known Accessibility Issue: [REPLACE WITH ONE OF THESE CATEGORIES Alert/Aria/Contrast Error/Error] - [REPLACE WITH NAME OF Alert/Aria/Contrast Error/Error]]
        - 1.04.01.01 [WAVE Known Accessibility Issue: [REPLACE WITH ONE OF THESE CATEGORIES Alert/Aria/Contrast Error/Error] - [REPLACE WITH NAME OF Alert/Aria/Contrast Error/Error], project-team-solution]

Additional reading (optional)
- https://hackforla.github.io/accessibility/

#### Slides
- [Staging Deck](https://docs.google.com/presentation/d/1crZ3IxqA4hAu3qzD7ns93Ieuqjwh6wyEtuX_46cP-fg)
   - [Staging Deck, slide ]
- Release deck
   - [2026-01-20 Release deck, slide ]
````

#### Slides
- [Staging Deck](https://docs.google.com/presentation/d/1crZ3IxqA4hAu3qzD7ns93Ieuqjwh6wyEtuX_46cP-fg)
   - [Staging Deck, slide 2897] - N/A
- Release deck
   - [2026-01-20 Release deck, slide 2897] - N/A
`````
