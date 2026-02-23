# WAVE Known Accessibility Issue: Alert - Skipped heading level
- WAVE Category: Alert
- WAVE Error: Skipped heading level

## Page Content Status
- [X] WAVE Error guidance text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
   - [ ] Project Team Page Details
   - [ ] Project Team Issue and PR details
   - [ ] Project Team Solution
- [ ] Credits/Authors

## WAVE Error guidance

WAVE Tool's Reference material on Skipped heading level may not specifically address your problem.  We provide it here for optional reading.

<details><summary>Click to see WAVE Tool Reference</summary>
<p>

<!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

> ### WAVE Category
> Alerts
> ### WAVE Error
> Skipped heading level
> ### What It Means
> A heading level is skipped.
> ### Why It Matters
> Headings provide document structure and facilitate keyboard navigation by users of assistive technology. These users may be confused or experience difficulty navigating when heading levels are skipped.
> ### What To Do
> Restructure the document headings to ensure that heading levels are not skipped.
> ### The Algorithm... in English
> A heading level is skipped (e.g., an `<h1>` is followed by an `<h3>`, with no intermediate `<h2>`). Note that an `<h1>` is not required to be the first heading within the document.
> ### Standards and Guidelines
> - [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)
> -  [2.4.1 Bypass Blocks (Level A)](https://webaim.org/standards/wcag/checklist#sc2.4.1)
> - [2.4.6 Headings and Labels (Level AA)](https://webaim.org/standards/wcag/checklist#sc2.4.6)


</p>
</details> 

## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> [HTML snippet showing the problematic code structure that WAVE detected]
> ```

## Project Team Error guidance

The following material covers how the Project Team has provided a solution to the [Error] WAVE error.

### Project Page Details
- Project Page name: Privacy Policy
- Project Staging URL: http://tdm-dev.azurewebsites.net/privacypolicy
- Requires sign in: FALSE
   - Required User Role: Visitor
   - Can access page directly from URL: TRUE
   - Accepts URL parameters: FALSE

### Project Team Issue and PR details
- Related GitHub Issue(s):
  - https://github.com/hackforla/tdm-calculator/issues/2716
- Related Pull Request(s):
  - PR: https://github.com/hackforla/tdm-calculator/pull/2760
- React Component(s)
  - [INSERT PATH: e.g. path/to/Component.jsx]
 
### Project Page Details
- Project Page name: Forgot Password
- Project Staging URL: https://tdm-dev.azurewebsites.net/forgotpassword
- Requires sign in: FALSE
   - Required User Role: All Users
   - Can access page directly from URL: TRUE
   - Accepts URL parameters: FALSE
 
### Project Team Issue and PR details
- Related GitHub Issue(s):
  - https://github.com/hackforla/tdm-calculator/issues/2701
- Related Pull Request(s):
  - https://github.com/hackforla/tdm-calculator/pull/2779
- React Component(s)
  - [INSERT PATH: e.g. path/to/Component.jsx]
 
### Project Page Details
- Project Page name: Manage Submissions
- Project Staging URL: https://tdm-dev.azurewebsites.net/managesubmissions
- Requires sign in: TRUE
   - Required User Role: Admin
   - Can access page directly from URL: FALSE
   - Accepts URL parameters: FALSE

### Project Team Issue and PR details
- Related GitHub Issue(s):
  - https://github.com/hackforla/tdm-calculator/issues/2705
- Related Pull Request(s):
  - https://github.com/hackforla/tdm-calculator/pull/2799
- React Component(s)
  - [INSERT PATH: e.g. path/to/Component.jsx]

### Project Team Solution

#### What is the specific problem that was occurring?
<!-- Author Instructions: Add a detailed explanation of the specific accessibility problem, including context about when/where it occurs, what elements are involved, and why it's problematic for assistive technology users -->
[INSERT CONTENT]

#### What is the proposed solution to this problem?
<!-- Author Instructions: Add a few sentences describing the fix. "Why the Fix Works" comes later (see below). If there are lots of instructions required to explain the solution, include them in Developer Resources below -->
[INSERT CONTENT]

#### Step-By-Step Guide
<!-- Author Instructions: Replace details dropdown with N/A if this does not apply -->

<details><summary>Click to see step-by-step guide</summary>
<p>

[ADD DETAILED INSTRUCTIONS HERE]

</p>
</details> 

#### Other Technical Details
<!-- Author Instructions: Write N/A if this does not apply -->

<details><summary>Click to see other technical details</summary>
<p>

[ INSERT OTHER DETAILS e.g. Prop References, Return Value ]

</p>
</details> 

#### Code Snippet With Solution
<details><summary>Click to see code snippets...</summary>

[INSERT PATH file/path/to/Snippet.jsx]

```jsx
[Code example showing the fix/solution]
```

</details>

#### Why the Fix Works
<!-- Author Instruction: Add an explanation of how the code changes resolve the accessibility issue and why this approach was chosen -->
[INSERT CONTENT]

#### Where this solution is applicable 
<!-- Author Instruction: Add a bullet point list of scenarios that might trigger this error and would be fixed by applying the provided solution, e.g. particular groupings of html elements, user interactivity, code-specific edge cases -->
- [INSERT SCENARIO 1]
- [INSERT SCENARIO 2]
- [INSERT SCENARIO N]

#### Screenshots of WAVE Error

<!-- Author Instructions: when including markdown images, ensure they are responsive by specifying EITHER width OR height. Do not provide both. -->

<details><summary>1. [Descriptive Title for Screenshot Set 1]</summary>

<img width="400" alt="Image" src="https://github.com/user-attachments/assets/123456789" />

</p>
</details> 

## Credits/Authors
<!-- Author Instructions: Add bullet points with GitHub handles of all HfLA members who contributed to this wiki page and/or contributed to Pull Requests that provided solutions for this page -->
- [INCLUDE Contributor 1]
- [INCLUDE Contributor 2]
- [INCLUDE Contributor N]
