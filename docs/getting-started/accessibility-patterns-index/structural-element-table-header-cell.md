
# Structural Element - Table header cell
- WAVE Category: Structural Element
- WAVE ACCESSIBILITY PATTERN: Table header cell

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-04-27. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#th" target="_blank">https://wave.webaim.org/api/docs?format=html#th</a>

    > ### WAVE Category
    > Structural Elements
    > ### WAVE Error
    > Table header cell
    > ### What It Means
    > A table header cell (`<th>`) is present.
    > ### Why It Matters
    > Table headers describe the content of their respective row or column. They can be identified by screen readers when data cells are encountered.
    > ### What To Do
    > Ensure the cell is a table header, otherwise change it to a data cell (`<td>`). For complex tables (particularly when there are spanned cells), the relationship between header and data cells may need to be defined using scope (e.g., `<th scope="col">` or `<th scope="row">`) or headers and id attributes.
    > ### The Algorithm... in English
    > A `<th>` element is present that does not have a scope attribute value of "row" or "col".
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





