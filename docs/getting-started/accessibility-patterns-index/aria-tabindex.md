# ARIA tabindex
- WAVE Category: ARIA
- WAVE ARIA: ARIA tabindex

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-03-23. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#aria_tabindex" target="_blank">https://wave.webaim.org/api/docs?format=html#aria_tabindex</a>

    > ### WAVE Category
    > ARIA
    > ### WAVE Error
    > ARIA tabindex
    > ### What It Means
    > A tabindex value of 0 or less is present.
    > ### Why It Matters
    > Tabindex can facilitate keyboard navigation for interactive elements. A tabindex attribute value of 0 places an item into the keyboard navigation order (i.e., you can navigate to it using the Tab key). A value of less than 0 (typically -1) removes an element from the keyboard flow (you cannot Tab to it), but allows it to receive programmatic focus (e.g., via scripting).
    > ### What To Do
    > Ensure that tabindex is being used correctly by navigating and interacting with the elements using only the keyboard. Positive tabindex values specify a distinct tab order and should typically be avoided.
    > ### The Algorithm... in English
    > A tabindex attribute is present and has a value of 0 or less.
    > ### Standards and Guidelines
    > - [2.1.1 Keyboard (Level A)](https://webaim.org/standards/wcag/checklist#sc2.1.1)

## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> [HTML snippet showing the problematic code structure that WAVE detected]
> ```

#### Screenshots of Accessibility Pattern in Use

<!-- Author Instructions: when including markdown images, ensure they are responsive by specifying EITHER width OR height. Do not provide both. -->

??? Info "1. Descriptive Title for Screenshot Set 1"

    Description/text for image

    [INSERT IMAGE HERE]

## Credits/Authors
<!-- Author Instructions: Add bullet points with GitHub handles of all HfLA members who contributed to this wiki page and/or contributed to Pull Requests that provided solutions for this page -->
- @Rabia2219
- [INCLUDE Contributor 2]
- [INCLUDE Contributor N]
