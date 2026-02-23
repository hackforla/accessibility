This page is the home for issue and wiki templates

## Known Issues Wiki Page Template
The wiki pages created from this template will be used for future audits (across many teams) so that volunteers can easily identify and refer to technical solutions to WAVE accessibility errors.

### Instructions
1. Replace all bracketed `[placeholders]` with actual content
2. Update the date in `YYYY-MM-DD` format
3. Fill in the WAVE Tool Reference section with content from the official WAVE documentation
4. Provide specific details in the TDM Solution section based on your issue and PR
5. Add actual screenshot URLs to replace `IMAGE_URL` placeholders
6. Add all contributor GitHub handles in the Credits section (wiki page author, PR author and reviewers)
7. Remove or add screenshot sections as needed

### Wiki Page Template

Copy/paste this template into the new wiki page editor:

<details><summary>Title</summary>

```
WCAG: [REPLACE WITH WAVE CATEGORY]-[REPLACE WITH WAVE ERROR NAME]
```
</details>

<details><summary>Body</summary>

````
# WAVE Known Accessibility Issue: [REPLACE WITH WAVE CATEGORY] - [REPLACE WITH WAVE ERROR NAME]
- WAVE Category: [REPLACE WITH WAVE CATEGORY]
- WAVE Error: [REPLACE WITH WAVE ERROR NAME]

## WAVE Error guidance

WAVE Tool's Reference material on [REPLACE WITH WAVE ERROR NAME] may not specifically address your problem.  We provide it here for optional reading.

<details><summary>Click to see WAVE Tool Reference</summary>
<p>

<!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

### WAVE Category
[REPLACE WITH WAVE CATEGORY]

### WAVE Error
[REPLACE WITH WAVE ERROR NAME]

### What It Means
[REPLACE WITH WAVE CONTENT FOR What It Means]

### Why It Matters
[REPLACE WITH WAVE CONTENT FOR Why It Matters]

### What To Do
[REPLACE WITH WAVE CONTENT FOR What To Do]

### The Algorithm... in English
[REPLACE WITH WAVE CONTENT FOR The Algorithm... In English]

### Standards and Guidelines
[REPLACE WITH WAVE CONTENT FOR Standards and Guidelines]

</p>
</details> 

## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> [HTML snippet showing the problematic code structure that WAVE detected]
> ```


## TDM Error guidance

The following material covers how the TDM team has provided a solution to the [Error] WAVE error.

### TDM Calculator Page Details
- TDM Page name: [INSERT PAGE NAME or "ALL"]
- TDM Staging URL: [INSERT URL or "N/A"]
- Required User Role: [INSERT ONE OF: Visitor, Logged in user, Admin, Security Admin]
### TDM Calculator Issue and PR details
- Related GitHub Issue(s):
  - [INSERT ISSUE URL]
- Related Pull Request(s):
  - [INSERT PR URL]
- React Component(s)
  - [INSERT PATH: e.g. path/to/Component.jsx]

### TDM Solution

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

````
</details>
