# Structural Element - Column header cell
- WAVE Category: Structural Element
- WAVE Structural Element: Column header cell

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-03-23. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#th_col" target="_blank">https://wave.webaim.org/api/docs?format=html#th_col</a>

    > ### WAVE Category
    > Structural Elements
    > ### WAVE Error
    > Column header cell
    > ### What It Means
    > A table column header (`<th scope="col">`) is present.
    > ### Why It Matters
    > Adding a column scope to a table header ensures the cells within that column will be programmatically associated to that header, particularly with complex tables. This facilitates screen reader navigation and orientation within the data table.
    > ### What To Do
    > Ensure that the cell is actually a header cell for tabular data and that it is a column header.
    > ### The Algorithm... in English
    > A table header cell (`<th>`) is present that has a scope attribute value of "col".
    > ### Standards and Guidelines
    > - [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)

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
