# Alert - Orphaned form label
- WAVE Category: Alert
- WAVE Alert: Orphaned form label

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
    > - references an element that is not an `<input>`, `<select>` or `<textarea>` element
    > - references an `<input>` element with image, submit, reset, button, or hidden type
    > ### Standards and Guidelines
    > - 1.1.1 Non-text Content (Level A)
    > - 1.3.1 Info and Relationships (Level A)
    > - 2.4.6 Headings and Labels (Level AA)
    > - 3.3.2 Labels or Instructions (Level A)


## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> <label for="APN">Assessor Parcel Number</label>
> <input type="checkbox" value="true">
> ```

(where the input element lacks an `id` attribute matching the label's `for="APN"` attribute)

## Project Team Error guidance

The following material covers how the TDM team has provided a solution to the Orphaned form label WAVE alert.

### Project Page Details
- TDM Page name: Create Project
- TDM Staging URL: https://tdm-dev.azurewebsites.net/calculation/1/0
- Required User Role: Logged in user

### Project Team Issue and PR details
#### Related GitHub Issue, PR and React Component 1
- Related GitHub Issue 1:
    - https://github.com/hackforla/tdm-calculator/issues/2572
- Related Pull Request:
    - https://github.com/hackforla/tdm-calculator/pull/2611
- React Component:
    - `client/src/components/ProjectWizard/RuleInput/MultiInput.jsx`

#### Related GitHub Issue, PR and React Component 2
- Related GitHub Issue 2:
    - https://github.com/hackforla/tdm-calculator/issues/2572
- Related Pull Request:
    - https://github.com/hackforla/tdm-calculator/pull/2611
- React Component:
    - `client/src/components/ProjectWizard/RuleInput/MultiInput.jsx`

### Project Team Solution

#### What is the specific problem that was occurring?
This error occurred on the Create Project page where form labels were present but not properly associated with their corresponding form controls. The `<label>` element's `for` attribute did not match the `id` value of the input element, meaning screen readers could not communicate the purpose or function of the form field to users relying on assistive technology. The input element within the `MultiInput` component was missing both `id` and `name` attributes that would connect it to its paired label (e.g., a label with `for="APN"` but no input with `id="APN"`).

#### What is the proposed solution to this problem?
Add the `id` and `name` attributes to the input element with values matching the `for` attribute of the associated label.

#### Step-By-Step Guide
- N/A

#### Other Technical Details
- N/A

#### Code Snippet With Solution
??? Info "Click to see code snippets"

    ```jsx
    // client/src/components/ProjectWizard/RuleInput/MultiInput.jsx
    
    const Input = props => {
     // ...
    
      return (
        <div {/* ... */}>
          <InputMask
            {/* ... */}
            id={props.code} // Modified this so that we can reserve props.code for input.id below
            {/* ... */}
          >
            {inputProps => (
              <input
                id={props.code} // Added id attribute to match the "paired" label.for attribute (value will be props.code, e.g., "APN")
                name={props.code} // Added name attribute to match the "paired" label.for attribute
                {...inputProps}
                {/* ... */}
              />
            )}
          </InputMask>
        </div>
      );
    };
    ```

#### Why the Fix Works
By adding the `id` and `name` attributes to the input element with values matching the `for` attribute of the associated label (using `props.code` which would be "APN" for Assessor Parcel Number), screen readers can now correctly identify and announce the label when users navigate to the form control. This creates the proper programmatic association required by WCAG standards, ensuring assistive technology can communicate the input's purpose to users.

#### Where this solution is applicable 
- Form inputs with separate `<label>` elements that need explicit association
- Multi-input components where labels and inputs are rendered separately
- Any form control (input, select, textarea, checkbox, radio) requiring a descriptive label
- Dynamic form fields generated by React components where IDs need to be programmatically assigned
- Create Project wizard forms and similar multi-step form interfaces

#### Screenshots of WAVE Error

??? Info "1. Descriptive Title for Screenshot Set 1"

    Description/text for image

    [INSERT IMAGE HERE]
    
    Description/text for image

    [INSERT IMAGE HERE]

??? Info "1. Descriptive Title for Screenshot Set 2"

    Descriptoin/text for image

    [INSERT IMAGE HERE] 

## Credits/Authors
All HfLA members who contributed to this wiki page and/or contributed to Pull Requests that provided solutions for this page.

- @heejung-hong 
- @eburdekin 
- @geolunalg
- @Rabia2219
