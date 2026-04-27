
# Structural Element - Generic region
- WAVE Category: Structural Element
- WAVE ACCESSIBILITY PATTERN: Generic region

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-04-27. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#region" target="_blank">https://wave.webaim.org/api/docs?format=html#region</a>

    > ### WAVE Category
    > Structural Elements
    > ### WAVE Error
    > Generic region
    > ### What It Means
    > An ARIA region is present
    > ### Why It Matters
    > Generic ARIA regions identify significant page areas that do not align to other region or ARIA landmark semantics - such as main, header, footer, etc. Regions support keyboard navigation and screen reader identification of page areas.
    > ### What To Do
    > Ensure the region identifies a significant page area. If the semantics for another region or landmark type aligns with the content (e.g., `<nav>` or `<aside>`), use it instead. Ensure the region has a descriptive label using aria-labelledby (typically referencing a heading at the beginning of the region) or aria-label.
    > ### The Algorithm... in English
    > An element has role="region" and an aria-label or aria-labelledby attribute.
    > ### Standards and Guidelines
    > - [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)
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





