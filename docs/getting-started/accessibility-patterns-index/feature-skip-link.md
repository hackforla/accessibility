
# Feature - Skip link
- WAVE Category: Feature
- WAVE ACCESSIBILITY PATTERN: Skip link

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

This content added 2026-04-27. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#link_skip" target="_blank">https://wave.webaim.org/api/docs?format=html#link_skip</a>

    > ### WAVE Category
    > Features
    > ### WAVE Error
    > Skip link
    > ### What It Means
    > A link is present which allows users to skip over navigation or other content.
    > ### Why It Matters
    > A link that provides functionality for the user to jump over navigation or other elements or jump to the main content of the page greatly assists keyboard users in navigating the web page.
    > ### What To Do
    > Ensure that the link is functioning properly and that the link text adequately describes the link functionality. If the skip link is hidden from sighted users, it should be made visible within the page when it has keyboard focus and must be accessible via the keyboard (do not use CSS display:none or visibility:hidden).
    > ### The Algorithm... in English
    > An in-page link:
    > - starts with the words "skip" or "jump"
    > - has an href attribute value and that value matches the id value of another element within the page or the name attribute value of an anchor element within the page.
    > - is NOT hidden with CSS display:none or visibility:hidden (this would result in a inaccessible "skip" link)
    > ### Standards and Guidelines
    > - [2.4.1 Bypass Blocks (Level A)](https://webaim.org/standards/wcag/checklist#sc2.4.1)

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
- @MissBrandyLea
- [INCLUDE Contributor 2]
- [INCLUDE Contributor N]





