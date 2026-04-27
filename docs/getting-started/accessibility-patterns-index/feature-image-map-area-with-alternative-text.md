
# Feature - Image map area with alternative text
- WAVE Category: Feature
- WAVE ACCESSIBILITY PATTERN: Image map area with alternative text

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

This content added 2026-04-27. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#alt_area" target="_blank">https://wave.webaim.org/api/docs?format=html#alt_area</a>

    > ### WAVE Category
    > Features
    > ### WAVE Error
    > Image map area with alternative text
    > ### What It Means
    > Alternative text is present for an image map area (hot spot).
    > ### Why It Matters
    > Presenting the functionality of image map areas (hot spots) in the `<area>` element's alt attribute value ensures that this information is presented to screen reader users or when images are disabled or unavailable.
    > ### What To Do
    > Ensure the alternative text for the area element describes the function of the image map hot spot. Additionally, ensure that the area elements are listed in the code in a logical, intuitive order (e.g., matching the visual order, alphabetically, etc.).
    > ### The Algorithm... in English
    > An image uses an image map containing an area element with a non-empty alt attribute value.
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





