# Structural Element - Data table
- WAVE Category: Structural Element
- WAVE Structural Element: Data table

## Page Content Status
- [X] WAVE Tool Reference text
- [ ] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-03-23. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#table_data" target="_blank">https://wave.webaim.org/api/docs?format=html#table_data</a>

    > ### WAVE Category
    > Structural Elements
    > ### WAVE Error
    > Data table
    > ### What It Means
    > A data table is present.
    > ### Why It Matters
    > Data tables present tabular data. Data tables should contain table header cells that identify the content of their respective row and/or columns. Tables with proper table headers provide additional information and navigation for screen reader users.
    > ### What To Do
    > Ensure that the table contains tabular data and that it is not used merely for page layout. Ensure that all column and row headers are `<th>` elements and ensure the data cells are associated with their proper header cells (typically by assigning scope to the table headers). Where appropriate, associate a descriptive caption (`<caption>` element) to the table.
    > ### The Algorithm... in English
    > A `<table>` element is present that contains at least one table header cell (`<th>`).
    > ### Guidelines
    > [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)

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
