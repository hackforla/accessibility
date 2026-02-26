# Error - Empty Table Header
- WAVE Category: Error
- WAVE Error: Empty Table Header

## Page Content Status
- [x] WAVE Error guidance text
- [x] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [x] Project Team Page Details
    - [x] Project Team Issue and PR details
    - [x] Project Team Solution
- [x] Credits/Authors

## WAVE's Error Guidance

WAVE Tool's Reference material on Empty Table Header may not specifically address your problem.  We provide it here for optional reading.

<details><summary>Click to see WAVE Tool Reference</summary>
<p>

### WAVE Category
Error

### WAVE Error
Empty Table Header

### What it Means
A `<th>` (table header) contains no text.

### Why It Matters
The `<th>` element helps associate table cells with the correct row/column headers. A `<th>` that contains no text may result in cells with missing or incorrect header information.

### What To Do
If the table cell is a header, provide text within the cell that describes the column or row. If the cell is not a header or must remain empty (such as the top-left cell in a data table), make the cell a `<td>` rather than a `<th>`.

### The Algorithm In English
A `<th>` element does not contain any text (or contains only spaces) and no images with alternative text.

### Standards and Guidelines
- [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)

</p>
</details> 

## Example of a DOM Snippet Generated From WAVE Tool

```html
<th>
    <div style="width: 100%; height: 100%;">
        <span>
            <input type="checkbox" style="height: 15px;">
        </span>
    </div>
</th>
```


## TDM Error guidance

The following material covers how the TDM team has provided a solution to the [Error] WAVE error.

### TDM Calculator Page Details
- TDM Page name: Projects Page
- TDM Staging URL: http://tdm-dev.azurewebsites.net/projects
- Required User Role: User (logged in)

### TDM Calculator Issue and PR details
- Related GitHub Issue(s):
  - n/a
- Related Pull Request(s):
  - https://github.com/hackforla/tdm-calculator/pull/2723
- React Component(s)
  - `client/src/components/Projects/ColumnHeaderPopups/ProjectTableColumnHeader.jsx`

### TDM Solution

#### What is the specific problem that was occurring?
Some table headers did not have text content, which violates WCAG 2.2 guidelines: For all table headers that do not portray visible text, we should supply an AT-friendly CSS class to table headers so that screen readers can still access and dictate a useful description.

#### What is the proposed solution to this problem?
Any tables that does not provide text in the column header column as a control, rather than text content, should apply a special class, `.sr-only` to an inner span or div.

#### Step-By-Step Guide
- simply add `sr-only` to the class list of the offending span or div

#### Other Technical Details
- n/a

#### Code Snippet With Solution
<details><summary>Click to see code snippets...</summary>

Example of `.sr-only` in source code...
```jsx
/* client/src/components/Projects/ProjectsPage.jsx */
        <>
          <label htmlFor="SelectAllProject" className="sr-only">
            Select All Projects on Page
          </label>
          <input
            style={{
              height: "15px"
            }}
            id="SelectAllProject"
            type="checkbox"
            checked={selectAllChecked}
            onChange={handleHeaderCheckbox}
          />
        </>
```

```scss
/* client/src/styles/App.scss */
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
```

</details>

#### Why the Fix Works
When applying this class to a span or div, the inner text will not render onto the screen, yet it remains accessible to AT for screen reader capability.
- Source: https://webaim.org/techniques/css/invisiblecontent/

#### Where this solution is applicable
  - checkboxes with no text (e.g. a "select-all" checkbox in left-most column of table)
  - columns whose cells provide on-hover option menus
  - images with special on-click behavior


#### Screenshots of WAVE Error

<details><summary>Screenshot 1: Projects Page with Empty Table Header highlighted</summary>
<p>

<img width="3379" alt="Image" src="https://github.com/user-attachments/assets/91adfff5-6942-436a-99be-d3a1b9d7b319" />

</p>
</details> 

<details><summary>Screenshot 2: My Projects page with WAVE annotations on</summary>
<p>

<img width="3387" alt="Image" src="https://github.com/user-attachments/assets/7d4b76c5-177d-4951-89d5-6372f85bcf38" />

</p>
</details> 

## Credits / Authors
All HfLA members who contributed to this wiki page and/or contributed to Pull Requests that provided solutions for this page.

- @ryanfchase 
- @Tony-Villa 
- @entrotech 
- @geolunalg 
- @JRParryY 
- @experimentsinhonesty
