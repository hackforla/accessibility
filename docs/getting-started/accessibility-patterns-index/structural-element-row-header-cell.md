
# Structural Element - Row header cell
- WAVE Category: Structural Element
- WAVE ACCESSIBILITY PATTERN: Row header cell

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-04-27. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#th_row" target="_blank">https://wave.webaim.org/api/docs?format=html#th_row</a>

    > ### WAVE Category
    > Structural Elements
    > ### WAVE Error
    > Row header cell
    > ### What It Means
    > A table row header (`<th scope="row">`) is present.
    > ### Why It Matters
    > Adding a row scope to a table header ensures the cells within that row will be programmatically associated to that header, particularly with complex tables. This facilitates screen reader navigation and orientation within the data table.
    > ### What To Do
    > Ensure that the cell is actually a header cell for tabular data and that it is a row header.
    > ### The Algorithm... in English
    > A table header cell (`<th>`) is present that has a scope attribute value of "row".
    > ### Standards and Guidelines
    > - [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)

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





