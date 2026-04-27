
# Feature - Linked image with alternative text
- WAVE Category: Feature
- WAVE ACCESSIBILITY PATTERN: Linked image with alternative text

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

This content added 2026-04-27. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#alt_link" target="_blank">https://wave.webaim.org/api/docs?format=html#alt_link</a>

    > ### WAVE Category
    > Features
    > ### WAVE Error
    > Linked image with alternative text
    > ### What It Means
    > Alternative text is present for an image that is within a link.
    > ### Why It Matters
    > Including appropriate alternative text on an image within a link ensures that the function and purpose of the link and the content of the image is available to screen reader users or when images are unavailable.
    > ### What To Do
    > Ensure that the alternative text presents the content of the image and/or the function of the link. If the full content and function of the link is presented in text within the link (an image and a text caption both within the same link, for example), then the image should generally be given empty/null alternative text (alt="") to avoid redundancy.
    > ### The Algorithm... in English
    > An image element has non-empty alternative text, is within a link, and no other text (or images with alternative text) is present within the link.
    > ### Standards and Guidelines
    > - [1.1.1 Non-text Content (Level A)](https://webaim.org/standards/wcag/checklist#sc1.1.1)
    > - [2.4.4 Link Purpose (In Context) (Level A)](https://webaim.org/standards/wcag/checklist#sc2.4.4)

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





