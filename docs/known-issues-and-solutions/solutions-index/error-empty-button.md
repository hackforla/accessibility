# Error - Empty Button
- WAVE Category: Error
- WAVE Error: Empty Button

## Page Content Status
- [x] WAVE Error guidance text
- [x] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [x] Project Team Page Details
    - [x] Project Team Issue and PR details
    - [x] Project Team Solution
- [x] Credits/Authors

## WAVE Error guidance

WAVE Tool's Reference material on Empty Button may not specifically address your problem.  We provide it here for optional reading.

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-02-26. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#button_empty" target="_blank">https://wave.webaim.org/api/docs?format=html#button_empty</a>

    <!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

    > ### WAVE Category
    > Error
    > ### WAVE Error
    > Empty Button
    > ### What It Means
    > A button is empty or has no value text.
    > ### Why It Matters
    > When navigating to a button, descriptive text must be presented to screen reader users to indicate the function of the button.
    > ### What To Do
    > Place text content within the `<button>` element or give the `<input>` element a value attribute.
    > ### The Algorithm... in English
    > A `<button>` element is present that contains no text content (or alternative text), or an `<input type="submit">`, `<input type="button">`, or `<input type="reset">` has an empty or missing value attribute.
    > ### Standards and Guidelines
    > - 1.1.1 Non-text Content (Level A)
    > - 2.4.4 Link Purpose (In Context) (Level A)

## Example of a DOM Snippet Generated From WAVE Tool

```html
<button class="button-0-1-47 outlined-0-1-54 controlButton-0-1-416" type="button" id="edit-about-title-134">
  <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" color="#0F2940" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg" style="color: rgb(15, 41, 64);">
    <path fill="none" d="M0 0h24v24H0z"></path>
    <path d="M3 17.25V21h3.75L17.81 9.94l-3.75-3.75L3 17.25zM20.71 7.04a.996.996 0 0 0 0-1.41l-2.34-2.34a.996.996 0 0 0-1.41 0l-1.83 1.83 3.75 3.75 1.83-1.83z"></path>
  </svg>
</button>
```


## TDM Error guidance

The following material covers how the TDM team has provided a solution to the Empty Button WAVE error.

### TDM Calculator Page Details
- TDM Page name: all Create Project Pages
- TDM Staging URL: https://tdm-dev.azurewebsites.net/calculation/1/0
- Required User Role: Logged in user
### TDM Calculator Issue and PR details
- Related GitHub Issue(s):
  - https://github.com/hackforla/tdm-calculator/issues/2571
- Related Pull Request(s):
  - https://github.com/hackforla/tdm-calculator/pull/2602
- React Component(s)
  - `client/src/components/Button/NavButton.jsx`
  - `client/src/components/Button/Button.jsx`

### TDM Solution

#### What is the specific problem that was occurring?
<!-- Author Instructions: Add a detailed explanation of the specific accessibility problem, including context about when/where it occurs, what elements are involved, and why it's problematic for assistive technology users -->
This error occurred on the Create Project page navigation buttons (next/previous). The buttons contain only SVG icons (chevron left/right) without any text content or accessible labels. This means that screen readers cannot describe the function of these navigation buttons to users relying on assistive technology, especially in a multi-step form where understanding navigation is critical.

#### What is the proposed solution to this problem?
<!-- Author Instructions: Add a few sentences describing the fix. "Why the Fix Works" comes later (see below). If there are lots of instructions required to explain the solution, include them in Developer Resources below -->
The fix adds an `aria-label` attribute to each icon-only navigation button. This retains the design while ensuring screen readers announce meaningful labels such as “project creation next page” and “project creation previous page.” No visual changes were required; only the accessibility layer was updated.

#### Step-By-Step Guide
<!-- Author Instructions: Replace details dropdown with N/A if this does not apply -->

<details><summary>Click to see step-by-step guide</summary>
<p>

1. Open `client/src/components/Button/Button.jsx`.  
2. Ensure the component accepts an `ariaLabel` prop and applies it to the underlying `<button>` element.  
3. Open `client/src/components/Button/NavButton.jsx`.  
4. Pass a descriptive `aria-label` value based on navigation direction:
   - `"project creation previous page"` for the left/previous button  
   - `"project creation next page"` for the right/next button  
5. Confirm through WAVE and screen readers (NVDA/VoiceOver) that each button is now announced correctly.


</p>
</details> 

#### Other Technical Details
<!-- Author Instructions: Write N/A if this does not apply -->

<details><summary>Click to see other technical details</summary>
<p>

[ INSERT OTHER DETAILS e.g. Prop References, Return Value ]

</p>
</details> 

#### Code Snippet With Solution

<details><summary>Click to see code snippets...</summary>


```jsx
// client/src/components/Button/Button.jsx
const Button = ({
  ariaLabel = undefined,
  children
}) => {
  return (
    <button aria-label={ariaLabel}>
      {children}
    </button>
  );
};

// client/src/components/Button/NavButton.jsx
return (
  <Button
    aria-label={
      navDirection === "previous"
        ? "project creation previous page"
        : "project creation next page"
    }
  >
    {/* SVG icon for left/right navigation */}
  </Button>
);
```

</details>

#### Why the Fix Works
<!-- Author Instruction: Add an explanation of how the code changes resolve the accessibility issue and why this approach was chosen -->
By providing an `aria-label` attribute, the button remains visually unchanged but is correctly announced by screen readers. The `aria-label` provides descriptive text that allows all users to understand the button's purpose and use navigation effectively, even though the visual content is only an SVG icon. This is preferable to adding visible text since the icon-only design is intentional.

#### Where this solution is applicable 
<!-- Author Instruction: Add a bullet point list of scenarios that might trigger this error and would be fixed by applying the provided solution, e.g. particular groupings of html elements, user interactivity, code-specific edge cases -->

- Icon-only navigation buttons
- Buttons containing only SVG icons
- Close buttons (X icons), menu toggles, collapsible panels
- Multi-step form navigation
- Any interactive element lacking visible text


#### Screenshots of WAVE Error

<!-- Author Instructions: when including markdown images, ensure they are responsive by specifying EITHER width OR height. Do not provide both. -->


<details><summary>1. Create Project, Page 1: Empty Button</summary>
<p>

WAVE Error modal on Create Projects Page

> ![Image](https://github.com/user-attachments/assets/941a2b01-f902-414a-a227-927a34217f53)

WAVE Error modal on Create Projects Page (styles turned off)

> ![Image](https://github.com/user-attachments/assets/83fd0eea-7106-4a85-b438-e72a4d17189b)

</p>
</details> 

<details><summary>2. Create Project, Page 1 and Page 4: Empty Button (No Action Required)</summary>
<p>

Hidden Navigation Buttons
- Note: These buttons have `display: none` and are hidden from assistive technologies. No action required for these instances.

> ![Image](https://github.com/user-attachments/assets/71bd3cfa-22d9-4c99-89a9-fe6a0a9b8f68)

Same WAVE Icon but also showing Dev Tools Inspector

> ![Image](https://github.com/user-attachments/assets/7e93fc43-4f18-4efd-86e4-cddda94941ca)

</p>
</details> 

<details><summary>3. Visuals After PR changes Were Applied</summary>
  
> <img width="611" height="256" alt="after-label" src="https://github.com/user-attachments/assets/176da5c1-7b48-47db-983b-4cd74dc98fbd" />

</details>

## Credits/Authors
<!-- Author Instructions: Add bullet points with GitHub handles of all HfLA members who contributed to this wiki page and/or contributed to Pull Requests that provided solutions for this page -->
- @JRParryY 
- @nchanyal 
- @anh628 
- @ryanfchase
