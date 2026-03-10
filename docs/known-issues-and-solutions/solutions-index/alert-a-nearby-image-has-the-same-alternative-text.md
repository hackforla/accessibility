Alert - A nearby image has the same alternative text
- WAVE Category: Alert
- WAVE Alert: A nearby image has the same alternative text

## Page Content Status
- [X] WAVE Error guidance text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [ ] Project Team Page Details
    - [ ] Project Team Issue and PR details
    - [ ] Project Team Solution
- [ ] Credits/Authors

## WAVE Guidance

WAVE Tool's Reference material on A nearby image has the same alternative text may not specifically address your problem.  We provide it here for optional reading.

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-03-10. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#alt_duplicate" target="_blank">https://wave.webaim.org/api/docs?format=html#alt_duplicate</a>

    <!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

    > ### WAVE Category
    > Alerts
    > ### WAVE Error
    > A nearby image has the same alternative text
    > ### What It Means
    > Two images near each other have the same alternative text.
    > ### Why It Matters
    > When two images have the same alternative text, this often causes redundancy or indicates incorrect alternative text.
    > ### What To Do
    > Ensure that the alternative text for each image or image button is appropriate while removing unnecessary redundancy. If the content of the image is already conveyed elsewhere (through text or the alternative text of a nearby image) or if the image does not convey content, the image may generally be given empty/null alternative text (alt=""). Image buttons always convey a specific function, and thus cannot be given null alternative text.
    > ### The Algorithm... in English
    > The same alternative text (case insensitive, but not null/empty) is present for two images or image buttons (`<input type='image'>`) near each other (no more than 2 other images separate them).
    > ### Standards and Guidelines
    > - [1.1.1 Non-text Content (Level A)](https://webaim.org/standards/wcag/checklist#sc1.1.1)

## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> [HTML snippet showing the problematic code structure that WAVE detected]
> ```


## Project Team Error guidance

The following material covers how the Project Team has provided a solution to the [Alert/ARIA/Contrast Error/Error Name] WAVE [Alert/ARIA/Contrast Error/Error].

### Project Page Details
- Project Page name: [INSERT PAGE NAME or "ALL"]
- Project Dev URL: [INSERT URL or "N/A"]
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

??? Info "Click to see step-by-step guide"

    [ADD DETAILED INSTRUCTIONS HERE]

#### Other Technical Details
<!-- Author Instructions: Write N/A if this does not apply -->

??? Info "Click to see other technical details"

    [INSERT OTHER DETAILS e.g. Prop References, Return Value ]

#### Code Snippet With Solution
??? Info "Click to see code snippets"

    [INSERT PATH file/path/to/Snippet.jsx]

    ```jsx
    [Code example showing the fix/solution]
    ```

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

??? Info "1. Descriptive Title for Screenshot Set 1"

    Description/text for image

    [INSERT IMAGE HERE]

## Credits/Authors
<!-- Author Instructions: Add bullet points with GitHub handles of all HfLA members who contributed to this wiki page and/or contributed to Pull Requests that provided solutions for this page -->
- @Rabia2219
- [INCLUDE Contributor 2]
- [INCLUDE Contributor N]
