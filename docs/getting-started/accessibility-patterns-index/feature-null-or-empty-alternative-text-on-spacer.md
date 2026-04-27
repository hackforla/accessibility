
# Feature - Null or empty alternative text on spacer
- WAVE Category: Feature
- WAVE ACCESSIBILITY PATTERN: Null or empty alternative text on spacer

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-04-27. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#alt_spacer" target="_blank">https://wave.webaim.org/api/docs?format=html#alt_spacer</a>

    > ### WAVE Category
    > Features
    > ### WAVE Error
    > Null or empty alternative text on spacer
    > ### What It Means
    > Alternative text is null or empty (alt="") on a spacer image.
    > ### Why It Matters
    > Spacer images are used to control layout or positioning. Because they do not convey content, they should be given empty/null alternative text (alt="") to ensure that the content is not presented to screen reader users and is hidden when images are disabled or unavailable.
    > ### What To Do
    > Ensure that the image is a spacer image and that it does not convey content. Consider using CSS instead of spacer images for better control of positioning and layout.
    > ### The Algorithm... in English
    > An images with width and/or height of 3 pixels or less or file name of spacer.*, space.*, or blank.* has empty/null alt attribute         value (alt="").
    > ### Standards and Guidelines
    > - [1.1.1 Non-text Content (Level A)](https://webaim.org/standards/wcag/checklist#sc1.1.1)

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





