# Alert - Possible heading
- WAVE Category: Alert
- WAVE Error: Possible heading

## Page Content Status
- [X] WAVE Error guidance text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [ ] Project Team Page Details
    - [ ] Project Team Issue and PR details
    - [ ] Project Team Solution
- [ ] Credits/Authors

## WAVE Error guidance

WAVE Tool's Reference material on Possible heading may not specifically address your problem.  We provide it here for optional reading.

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-02-26. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#heading_possible" target="_blank">https://wave.webaim.org/api/docs?format=html#heading_possible</a>

    <!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

    > ### WAVE Category
    > Alerts
    > ### WAVE Error
    > Possible heading
    > ### What It Means
    > Text appears to be a heading but is not a heading element.
    > ### Why It Matters
    > Heading elements (`<h1>-<h6>`) provide important document structure, outlines, and navigation functionality to assistive technology users. If heading text is not a true heading, this information and functionality will not be available for that text.
    > ### What To Do
    > If the paragraph is a section heading, use a heading element instead (`<h1>-<h6>`).
    > ### The Algorithm... in English
    > A `<p>` element contains less than 50 characters and is either:
    > - 20 pixels or bigger
    > - 16 pixels or bigger and bold and/or italicized
    > ### Standards and Guidelines
    > - [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)
    > - [2.4.1 Bypass Blocks (Level A)](https://webaim.org/standards/wcag/checklist#sc2.4.1)
    > - [2.4.6 Headings and Labels (Level AA)](https://webaim.org/standards/wcag/checklist#sc2.4.6)

## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> [HTML snippet showing the problematic code structure that WAVE detected]
> ```


## Project Team Error guidance

The following material covers how the Project Team has provided a solution to the [Error] WAVE error.

### Project Page Details
- Project Page name: [INSERT PAGE NAME or "ALL"]
- Project Staging URL: [INSERT URL or "N/A"]
- Requires sign in: [TRUE OR FALSE]
   - Required User Role: [INSERT ONE OF: Visitor, Logged in user, Admin, Security Admin]
   - Can access page directly from URL: [TRUE OR FALSE]
   - Accepts URL parameters: [TRUE OR FALSE]

### Project Team Issue and PR details
- Related GitHub Issue(s):
  - [INSERT ISSUE URL]
- Related Pull Request(s):
  - [INSERT PR URL]
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
- @Rabia2219
- [INCLUDE Contributor 2]
- [INCLUDE Contributor N]
