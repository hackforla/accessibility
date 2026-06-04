# Alert - Layout table

- WAVE Category: Alert
- WAVE Alert: Layout table

## Page Content Status
- [X] WAVE Error guidance text
- [X] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [X] Project Team Page Details
    - [X] Project Team Issue and PR details
    - [X] Project Team Solution
- [X] Credits/Authors

## WAVE Error guidance

WAVE Tool's Reference material on Layout table may not specifically address your problem.  We provide it here for optional reading.

??? Info "Click to see WAVE Tool Reference"

    <!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

    This content added 2026-02-26. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#table_layout" target="_blank">https://wave.webaim.org/api/docs?format=html#table_layout</a>

    > ### WAVE Category
    > Alerts
    > ### WAVE Error
    > Layout table
    > ### What It Means
    > A layout table is present.
    > ### Why It Matters
    > Layout tables exist merely to position content visually - to create columns, insert spacing, or align content neatly for sighted users. Their content is not at all tabular in nature. Layout tables should not be used in HTML5. They can introduce reading and navigation order issues. Screen readers may interpret them as data tables (i.e., announcing column and row numbers), especially if they contain table header (`<th>`) cells. This introduces significant overhead on screen reader users.
    > ### What To Do
    > In almost every case, layout tables can be replaced with other HTML elements and styled with CSS to achieve the desired visual presentation. If the table contains tabular data, provide appropriate header (`<th>`) cells. If the layout table remains, verify that the reading and navigation order of table content (based on underlying source code order) is logical and give it role="presentation" to ensure it is not identified as a table to screen reader users.
    > ### The Algorithm... in English
    > A `<table>` element is present that does not contain any header (`<th>`) cells.
    > ### Standards and Guidelines
    > - [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)
    > - [1.3.2 Meaningful Sequence (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.2)
</details> 

## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> <table class="table-0-2-25">
>   <thead class="thead-0-2-28">
>     <tr class="tr-0-2-26">
>       <td class="td-0-2-27">Name</td>
>       <td class="td-0-2-27">Address</td>
>       <td class="td-0-2-27">Created By</td>
>       <td class="td-0-2-27">Created On</td>
>       <td class="td-0-2-27">Last Saved</td>
>       <td class="td-0-2-27">Archive Date</td>
>     </tr>
>   </thead>
>   <tbody class="tbody-0-2-29">
>     <!-- ... -->
>   </tbody>
> </table>
> ```


## Project Team Error guidance

The following material covers how the Project Team has provided a solution to the layout table WAVE alert.

### Project Page Details
- Project Page name: Archived Projects
- Project Staging URL: https://tdm-dev.azurewebsites.net/archivedprojects
- Requires sign in: TRUE
    - Required User Role: Security Admin
    - Can access page directly from URL: FALSE
    - Accepts URL parameters: FALSE

### Project Team Issue and PR details
- Related GitHub Issue(s):
    - https://github.com/hackforla/tdm-calculator/issues/2837
- Related Pull Request(s):
    - https://github.com/hackforla/tdm-calculator/pull/3068
- React Component(s)
    - client\src\components\ArchiveDelete\ProjectsArchive.jsx

### Project Team Solution

#### What is the specific problem that was occurring?
<!-- Author Instructions: Add a detailed explanation of the specific accessibility problem, including context about when/where it occurs, what elements are involved, and why it's problematic for assistive technology users -->
This alert occurred on the Archived Projects page, caused by a table using td elements in the header, instead of the expected th elements. In this case, the table is really a data table, and the error was triggered since the wrong tag was used.
If the table is used to set the layout of content on the page, it is recommended to use other CSS features such as Grid or Flexbox to achieve this.

#### What is the proposed solution to this problem?
<!-- Author Instructions: Add a few sentences describing the fix. "Why the Fix Works" comes later (see below). If there are lots of instructions required to explain the solution, include them in Developer Resources below -->
Ensure that the table contains a header and `<th>` elements.

#### Step-By-Step Guide
<!-- Author Instructions: Replace details dropdown with N/A if this does not apply -->

??? Info "Click to see step-by-step guide"

  - n/a


#### Other Technical Details
<!-- Author Instructions: Write N/A if this does not apply -->

??? Info "Click to see other technical details"

  - n/a

#### Code Snippet With Solution
??? Info "Click to see code snippets"

    ```jsx
    // client\src\components\ArchiveDelete\ProjectsArchive.jsx

    const ProjectsArchive = () => {
    // ...
        return (
            // ...
                <table className={classes.table}>
                <thead className={classes.thead}>
                    <tr className={classes.tr}>
                        <th className={classes.td}>Name</th> // ensure that the table has a header and th elements
                    // ...
                    </tr>
                </thead>
                <tbody className={classes.tbody}>
                    // ...
                </tbody>
            // ...
        );
    ```

#### Why the Fix Works
<!-- Author Instruction: Add an explanation of how the code changes resolve the accessibility issue and why this approach was chosen -->
Adding a header and th elements to the table fixes the error by making sure the table is interpreted as a data table.

#### Where this solution is applicable 
<!-- Author Instruction: Add a bullet point list of scenarios that might trigger this error and would be fixed by applying the provided solution, e.g. particular groupings of html elements, user interactivity, code-specific edge cases -->
- tables

#### Screenshots of WAVE Error

<!-- Author Instructions: when including markdown images, ensure they are responsive by specifying EITHER width OR height. Do not provide both. -->

??? Info "1. Descriptive Title for Screenshot Set 1"

    Description/text for image

    [INSERT IMAGE HERE]
    
    Description/text for image

    [INSERT IMAGE HERE]

??? Info "1. Descriptive Title for Screenshot Set 2"

    Descriptoin/text for image

    [INSERT IMAGE HERE]

## Credits/Authors
<!-- Author Instructions: Add bullet points with GitHub handles of all HfLA members who contributed to this wiki page and/or contributed to Pull Requests that provided solutions for this page -->
- @Rabia2219
- @Philc90
