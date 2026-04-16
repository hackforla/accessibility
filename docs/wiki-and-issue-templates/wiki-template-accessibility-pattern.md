# WIKI template: accessibility pattern

## What does this template do?
This WIKI template creates a new WIKI page in the Accessibility Patterns index.  The wiki pages created from this template will be used for self guided learning of accessibility patterns.

## When should this template be used?
Only use this template when you have confirmed that there isn't already a page in the [Accessibility Patterns index](../getting-started/accessibility-patterns-index/)

If this is not the correct template, see [WIKI and Issue templates](index.md) for a list of other templates available.

## Instructions
1. Replace all bracketed `[placeholders]` with actual content
1. Update the date in `YYYY-MM-DD` format
1. Fill in the area below "Click to see WAVE Accessibility Pattern" with content from the official WAVE documentation
    1. Replace [YYYY-MM-DD] with the date the content was added or reviewed
    1. Go to https://wave.webaim.org/api/docs?format=html
    1. Find the section that matches the WAVE guidance referenced in this file (e.g. Link to PDF document)
    1. Copy the anchor name from the end of that section (e.g. link_pdf)
    1. Replace both [REPLACE ANCHOR NAME] in the link with that anchor name
    1. For each header under that (e.g. ### WAVE Category), add the content from the relevant WAVE guidance section
1. Add actual screenshot URLs to replace `IMAGE_URL` placeholders
1. Add all contributor GitHub handles in the Credits section (wiki page author, PR author and reviewers)
1. Remove or add screenshot sections as needed

## Template
Copy/paste this template to create a wiki page in the folder: /getting-started/accessibility-patterns-index

### File Name
The filename should be all lowercase and without brackets

```
[REPLACE WITH WAVE CATEGORY]-[REPLACE WITH WAVE ACCESSIBILITY PATTERN NAME].md
```

### Body
````
# [REPLACE WITH WAVE CATEGORY] - [REPLACE WITH WAVE ACCESSIBILITY PATTERN NAME]
- WAVE Category: [REPLACE WITH WAVE CATEGORY]
- WAVE ACCESSIBILITY PATTERN: [REPLACE WITH NAME]

## Page Content Status
- [ ] WAVE Accessibility Pattern text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Accessibility Pattern 

??? Info "Click to see WAVE Accessibility Pattern "

    This content added [YYYY-MM-DD]. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#[REPLACE ANCHOR NAME]" target="_blank">https://wave.webaim.org/api/docs?format=html#[REPLACE ANCHOR NAME]</a>

    > ### WAVE Category
    > [REPLACE WITH WAVE CATEGORY]

    > ### WAVE ACCESSIBILITY PATTERN
    > [REPLACE WITH WAVE ACCESSIBILY PATTERN NAME]

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
> [HTML snippet showing the code structure that WAVE detected]
> ```

## Screenshots of Accessibility Pattern in Use

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
