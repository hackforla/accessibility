# Error - Missing Form Label
- WAVE Category: Error
- WAVE Error: Missing Form Label

## Page Content Status
- [x] WAVE Error guidance text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
   - [x] Project Team Page Details
   - [x] Project Team Issue and PR details
   - [ ] Project Team Solution
- [x] Credits/Authors

## WAVE Error guidance

WAVE Tool's Reference material on Missing Form Label may not specifically address your problem.  We provide it here for optional reading.

<details><summary>Click to see WAVE Tool Reference</summary>
<p>

<!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

> ### WAVE Category
> Error
> 
> ### WAVE Error
> Missing form label
> 
> ### What It Means
> A form control does not have a corresponding label.
> 
> ### Why It Matters
> If a form control does not have a properly associated text label, the function or purpose of that form control may not be presented to screen reader users. Form labels also provide visible descriptions and larger clickable targets for form controls.
> 
> ### What To Do
> If a text label for a form control is visible, use the `<label>` element to associate it with its respective form control. If there is no visible label, either provide an associated label, add a descriptive title attribute to the form control, or reference the label(s) using aria-labelledby. Labels are not required for image, submit, reset, button, or hidden form controls.
> 
> ### The Algorithm... in English
> An `<input>` (except types of image, submit, reset, button, or hidden), `<select>`, or `<textarea>` does not have a properly associated label. A properly associated label is:
> 
> - a non-hidden `<label>` element with a for attribute value that is equal to the id of a unique form control
> - a `<label>` element that surrounds the form control, does not surround any other form controls, and does not reference another element with its for attribute
> - a non-empty title attribute, or
> - a non-empty aria-labelledby attribute
> 
> ### Standards and Guidelines
> - 1.1.1 Non-text Content (Level A)
> - 1.3.1 Info and Relationships (Level A)
> - 2.4.6 Headings and Labels (Level AA)
> - 3.3.2 Labels or Instructions (Level A)

</p>
</details> 

## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> [HTML snippet showing the problematic code structure that WAVE detected]
> ```


## Project Team Error guidance

The following material covers how the Project Team has provided a solution to the [Error] WAVE error.

### Project Page Details
- Project Page name: Security
- Project Staging URL: http://tdm-dev.azurewebsites.net/roles
- Requires sign in: true
   - Required User Role: Security Admin
   - Can access page directly from URL: false

### Project Team Issue and PR details
- Related GitHub Issue:
  - https://github.com/hackforla/tdm-calculator/issues/2709
- Related Pull Request:
  - https://github.com/hackforla/tdm-calculator/pull/2803

### Project Page Details
- Project Page name: Update Account
- Project Staging URL: https://tdm-dev.azurewebsites.net/updateaccount
- Requires sign in: true
   - Required User Role: Logged in user
   - Can access page directly from URL: TRUE (But should be FALSE See issue https://github.com/hackforla/tdm-calculator/issues/2857)
   - Accepts URL parameters? TRUE (but should be false.  See issue https://github.com/hackforla/tdm-calculator/issues/2857)
     e.g. /updateaccount/example@hfla.com pre-populates email form field

- Related GitHub Issue:
  - https://github.com/hackforla/tdm-calculator/issues/2697
- Related Pull Request:
  - https://github.com/hackforla/tdm-calculator/pull/2784
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
- @experiementsinhonesty
