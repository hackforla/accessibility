# Alerts - Broken same-page link
- WAVE Category: Alerts
- WAVE Alerts: Broken same-page link

## Page Content Status
- [X] WAVE Error guidance text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [ ] Project Team Page Details
    - [ ] Project Team Issue and PR details
    - [ ] Project Team Solution
- [ ] Credits/Authors

## WAVE Guidance

WAVE Tool's Reference material on Broken same-page link may not specifically address your problem.  We provide it here for optional reading.

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-03-23. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#link_internal_broken" target="_blank">https://wave.webaim.org/api/docs?format=html#link_internal_broken</a>

    > ### WAVE Category
    > Alerts
    > ### WAVE Error
    > Broken same-page link
    > ### What It Means
    > A link to another location within the page is present but does not have a corresponding target.
    > ### Why It Matters
    > A link to jump to another position within the page assists users in navigating the web page, but only if the link target exists.
    > ### What To Do
    > Ensure that the target for the link exists or remove the same-page link.
    > ### The Algorithm... in English
    > An in-page link has an href attribute (starting with a #), but does not match either the id value of another element or the name attribute value of an anchor element within the page.
    > ### Standards and Guidelines
    > - [2.1.1 Keyboard (Level A)](https://webaim.org/standards/wcag/checklist#sc2.1.1)
    
## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> [HTML snippet showing the problematic code structure that WAVE detected]
> ```


## Project Team Error guidance

The following material covers how the Project Team has provided a solution to the Broken same-page link WAVE Alert.

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
