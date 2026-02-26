# test-file2
- WAVE Category: Alert
- WAVE Error: Orphaned form label

# Page Content Status
- [x] WAVE Error guidance text
- [x] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [x] Project Team Page Details
    - [x] Project Team Issue and PR details
    - [x] Project Team Solution
- [x] Credits/Authors

## WAVE Error guidance

WAVE Tool's Reference material on Orphaned form label may not specifically address your problem.  We provide it here for optional reading.

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-02-26. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#label_orphaned" target="_blank">https://wave.webaim.org/api/docs?format=html#label_orphaned</a>

    <!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

    > ### WAVE Category
    > Alert
    > ### WAVE Error
    > Orphaned form label
    > ### What It Means
    > A form label is present, but it is not correctly associated with a form control.
    > ### Why It Matters
    > An incorrectly associated label does not provide functionality or information about the form control to the user. It usually indicates a coding or other form labeling issues.
    > ### What To Do
    > Properly associate the label with its corresponding form control. If there is no corresponding form control, remove the label. Labels are not appropriate for image, submit, reset, button, or hidden form controls.
    > ### The Algorithm... in English
    > A `<label>` element
    > - does not surround a form control and the for attribute is missing/empty
    > - references an element that is not present in the page
    > - references an element that is not an <input>, <select> or <textarea> element
    > - references an <input> element with image, submit, reset, button, or hidden type
    > ### Standards and Guidelines
    > - 1.1.1 Non-text Content (Level A)
    > - 1.3.1 Info and Relationships (Level A)
    > - 2.4.6 Headings and Labels (Level AA)
    > - 3.3.2 Labels or Instructions (Level A)


## Example of a DOM Snippet Generated From WAVE Tool

test
