# WIKI page template: known issue
The wiki pages created from this template will be used for future audits (across many teams) so that volunteers can easily identify and refer to technical solutions to WAVE accessibility errors.

## What does this template do?
It 

## When should this template be used?

## Instructions
1. Replace all bracketed `[placeholders]` with actual content
1. Update the date in `YYYY-MM-DD` format
1. Fill in the area below "Click to see WAVE Tool Reference" with content from the official WAVE documentation
    1. Replace [YYYY-MM-DD] with the date the content was added or reviewed
    1. Go to https://wave.webaim.org/api/docs?format=html
    1. Find the section that matches the WAVE guidance referenced in this file (e.g. Link to PDF document)
    1. Copy the anchor name from the end of that section (e.g. link_pdf)
    1. Replace both [REPLACE ANCHOR NAME] in the link with that anchor name
    1. For each header under that (e.g. ### WAVE Category), add the content from the relevant WAVE guidance section
1. Provide specific details in the Project Team Solution section based on your issue and PR
1. Add actual screenshot URLs to replace `IMAGE_URL` placeholders
1. Add all contributor GitHub handles in the Credits section (wiki page author, PR author and reviewers)
1. Remove or add screenshot sections as needed

## Template
Copy/paste this template to create a wiki page in the folder: /known-issues-and-solutions/solutions-index

### File Name
The filename should be all lowercase and without brackets
```
[REPLACE WITH WAVE CATEGORY]-[REPLACE WITH WAVE ERROR NAME].md
```

### Body
````
# [REPLACE WITH WAVE CATEGORY] - [REPLACE WITH WAVE NAME]
- WAVE Category: [REPLACE WITH WAVE CATEGORY]
- WAVE [Error/Contrast Error/Alert/ARIA]: [REPLACE WITH NAME]

## Page Content Status
- [ ] WAVE Error guidance text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [ ] Project Team Page Details
    - [ ] Project Team Issue and PR details
    - [ ] Project Team Solution
- [ ] Credits/Authors

## WAVE Guidance

WAVE Tool's Reference material on [REPLACE WITH WAVE ERROR NAME] may not specifically address your problem.  We provide it here for optional reading.

??? Info "Click to see WAVE Tool Reference"

    This content added [YYYY-MM-DD]. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#[REPLACE ANCHOR NAME]" target="_blank">https://wave.webaim.org/api/docs?format=html#[REPLACE ANCHOR NAME]</a>

    > ### WAVE Category
    > [REPLACE WITH WAVE CATEGORY]

    > ### WAVE Error
    > [REPLACE WITH WAVE ERROR NAME]

    > ### What It Means
    > [REPLACE WITH WAVE CONTENT FOR What It Means]

    > ### Why It Matters
    > [REPLACE WITH WAVE CONTENT FOR Why It Matters]

    > ### What To Do
    > [REPLACE WITH WAVE CONTENT FOR What To Do]

    > ### The Algorithm... in English
    > [REPLACE WITH WAVE CONTENT FOR The Algorithm... In English]

    > ### Standards and Guidelines
    > [REPLACE WITH WAVE CONTENT FOR Standards and Guidelines]

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
- [INCLUDE Contributor 1]
- [INCLUDE Contributor 2]
- [INCLUDE Contributor N]

````


---

- Page Status: In Progress
- Authors: 
    - Bonnie Wolfe
    - Rabia Shaikh
