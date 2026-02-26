# Contrast Errors - Very low contrast
- WAVE Category: Contrast Errors
- WAVE Error: Very low contrast

## Page Content Status
- [X] WAVE Error guidance text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [ ] Project Team Page Details
    - [ ] Project Team Issue and PR details
    - [ ] Project Team Solution
- [ ] Credits/Authors

## WAVE Error guidance

WAVE Tool's Reference material on Very low contrast may not specifically address your problem.  We provide it here for optional reading.

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-02-26. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#contrast" target="_blank">https://wave.webaim.org/api/docs?format=html#contrast</a>

    <!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

    > ### WAVE Category
    > Contrast Errors
    > ### WAVE Error
    > Very low contrast
    > ### What It Means
    > Very low contrast between text and background colors.
    > ### Why It Matters
    > Adequate contrast of text is necessary for all users, especially users with low vision.
    > ### What To Do
    > Increase the contrast between the foreground (text) color and the background color. Large text (larger than 18 point or 14 point bold) does not require as much contrast as smaller text.
    > ### The Algorithm... in English
    > Text is present that has a contrast ratio less than 4.5:1, or large text (larger than 18 point or 14 point bold) has a contrast ratio less than 3:1. WCAG requires that page elements have both foreground AND background colors defined (or inherited) that provide sufficient contrast. When text is presented over a background image, the text must have a background color defined (typically in CSS) that provides adequate text contrast when the background image is disabled or unavailable. WAVE does not identify contrast issues in text with CSS transparency, gradients, or filters. WCAG Level AAA requires a contrast ratio of at least 7:1 for normal text and 4.5:1 for large text.
    > ### Standards and Guidelines
    > - [1.4.3 Contrast (Minimum) (Level AA)](https://webaim.org/standards/wcag/checklist#sc1.4.3)

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
