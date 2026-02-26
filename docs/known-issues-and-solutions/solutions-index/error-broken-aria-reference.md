# Error - Broken ARIA reference
- WAVE Category: Error
- WAVE Error: Broken ARIA reference

## Page Content Status
- [X] WAVE Error guidance text
- [X] Example of a DOM Snippet Generated From WAVE Tool
- Project Team Error guidance
    - [X] Project Team Page Details
    - [X] Project Team Issue and PR details
    - [X] Project Team Solution
- [X] Credits/Authors

## WAVE Error guidance

Click to see the WAVE Tool's Reference material on Broken ARIA reference. These guidelines may not specifically address your problem, but they might provide context for getting started.

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-02-26. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#aria_reference_broken" target="_blank">https://wave.webaim.org/api/docs?format=html#aria_reference_broken</a>

    <!-- Note For Wiki Author: WAVE Tool text content will use text that break markdown generation for the details dropdown. If the copy/pasted text includes angle brackets, surround them with backticks to avoid this problem. -->

    > ### WAVE Category
    > Error
    > ### WAVE Error
    > Broken ARIA reference
    > ### What It Means
    > An aria-labelledby or aria-describedby reference exists, but the target for the reference does not exist.
    > ### Why It Matters
    > ARIA labels and descriptions will not be presented if the element referenced does not exist in the page.
    > ### What To Do
    > Ensure the element referenced in the aria-labelledby or aria-describedby attribute value is present within the page and presents a proper label or description.
    > ### The Algorithm... in English
    > An element has an aria-labelledby or aria-describedby value that does not match the id attribute value of another element in the page.
    > ### Standards and Guidelines
    > - [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)
    > - [4.1.2 Name, Role, Value (Level A)](https://webaim.org/standards/wcag/checklist#sc4.1.2)

## Example of a DOM Snippet Generated From WAVE Tool

> ```html
> <span aria-describedby="popup-1" style="cursor: pointer;">
  > <a id="cy-login-menu-item" class="link-0-1-13 lastItem-0-1-18" href="/login">Login</a>
> </span>
> ```
## Project Team Error guidance

The following material covers how the TDM team has provided a solution to the Broken Aria reference WAVE error.

### Project Page Details
- TDM Page name: ALL
- TDM Staging URL: N/A
- Required User Role: ALL
### Project Team Issue and PR details
#### Related GitHub Issue, PR and React Component 1
- Related GitHub Issue 1:
    - https://github.com/hackforla/tdm-calculator/issues/2531
- Related Pull Request:
    - https://github.com/hackforla/tdm-calculator/pull/2786
        - follow-up commit: https://github.com/hackforla/tdm-calculator/commit/16072c43a7aa7d18656d133c302190d5a1e53ee9
- React Component:
    - `client/src/components/Layout/NavBarLogin.jsx`

### Project Team Solution

#### What is the specific problem that was occurring?
Dismissing the NavBarLogin's popup removes the Popup component from the DOM, but it does not also purge the `aria-describedby="popup-1"` attribute from NavBarLogin. At that point, a screen reader may attempt to process the DOM element with `id="popup-1"`, which no longer exists, leading to the “Broken ARIA reference” error.

Note: failure to remove `aria-describedby` is a bug in the `react-js-popup` open source project.

#### What is the proposed solution to this problem?
There are two workable patterns, depending on how reusable you need the fix to be:

1) **One-off fix (component-specific):** Augment the popup “close” handler so it removes the stray `aria-describedby` from the trigger element when the popup unmounts.

2) **Reusable fix (recommended):** Use a small custom hook (`useReplaceAriaAttribute`) to reliably remove the incorrect ARIA attribute added by `reactjs-popup` (typically `aria-describedby`) and replace it with a safer attribute (often `aria-controls`) that references a stable element ID you control.

This hook-based approach exists specifically because `reactjs-popup` may clone the trigger and strip attributes, making it difficult to set or override ARIA props directly on the trigger, and DOM manipulation can be subject to race conditions.

#### Step-By-Step Guide
<!-- Author Instructions: Replace details dropdown with N/A if this does not apply -->

??? Info "Click to see step-by-step guide"

    ## Option A: Component-specific fix (simple + local)

    1. Add a stable `id` to the trigger wrapper (the element that ends up receiving `aria-describedby`).
    2. In the popup `onClose` handler, call `removeAttribute("aria-describedby")` on that element before unmount completes.

    ## Option B: Reusable fix using `useReplaceAriaAttribute` (recommended)

    ### Step 1: Import the hook
    ```js
    import { useReplaceAriaAttribute } from "hooks/useReplaceAriaAttribute";
    ```

    ### Step 2: Add a unique `id` to your target element
    Recommended pattern (avoids mismatches):
    ```js
    const elementId = `context-menu-button-${project.id}`;
    ```

    Use it on the element:
    ```jsx
    <button id={elementId} aria-label="context menu button">
      <MdMoreVert />
    </button>
    ```

    ### Step 3: Call the hook in your component
    ```js
    useReplaceAriaAttribute({
      elementId,
      deps: [projectRules],
      attrToRemove: "aria-describedby",
      attrToAdd: "aria-controls",
      value: `popup-content-${elementId}`,
    });
    ```

    ### Step 4 (optional but common): Ensure the referenced element exists
    If you set `aria-controls` to some id, ensure the popup content uses that id:
    ```jsx
    <Popup trigger={...}>
      <div id={`popup-content-${elementId}`}>
        {/* popup content */}
      </div>
    </Popup>
    ```

    ### Dependency array tips
    Include in `deps` anything that could change whether:
    - the trigger exists / is re-rendered
    - the element id changes
    - the popup structure changes

#### Other Technical Details
<!-- Author Instructions: Write N/A if this does not apply -->

??? Info "Click to see other technical details"

    - `reactjs-popup` clones the trigger element and strips any attributes, which can prevent setting ARIA attributes or refs directly on the trigger.
    - Ad-hoc DOM manipulation can be subject to timing/race issues if you do it in many components.
    - A hook centralizes the workaround so components don’t each reinvent their own “removeAttribute” logic.

    Reference (discussion): https://github.com/hackforla/tdm-calculator/issues/2410#issuecomment-3561030939


#### Code Snippet With Solution
??? Info "Click to see code snippets"

    Component: `NavBarLogin.jsx`

    ```jsx
    const NavBarLogin = ({ ... }) => {
      const closeModal = () => { // 1. augment closeModal handler by removing `aria-describedby` attribute
        const loginLink = document.getElementById("login-link");
        loginLink.removeAttribute("aria-describedby");
        setTooltipOpen(false);
      };
      return (
        <Popup>
          <!-- ... -->
          onClose={closeModal}
          trigger={(
            <!-- 2. add a unique id, "login-link" to the span that will (eventually) receive the `aria-describedby` attribute
            <span id="login-link" style={{ cursor: "pointer" }}>
               {loginLink}
            </span>
          )}
        /> <!-- end Popup -->
      ) // end-return
    ```


    Reusable hook approach (`useReplaceAriaAttribute`)

    ```jsx
    import { useReplaceAriaAttribute } from "hooks/useReplaceAriaAttribute";
    import Popup from "reactjs-popup";

    function MyComponent({ project }) {
      const elementId = `context-menu-button-${project.id}`;
      const popupContentId = `popup-content-${elementId}`;

      useReplaceAriaAttribute({
        elementId,
        deps: [projectRules],
        attrToRemove: "aria-describedby",
        attrToAdd: "aria-controls",
        value: popupContentId,
      });

      return (
        <Popup
          trigger={
            <button id={elementId} aria-label="context menu button">
              Menu
            </button>
          }
        >
          <div id={popupContentId}>
            {/* Menu items */}
          </div>
        </Popup>
      );
    }
    ```

#### Why the Fix Works
By deleting (or replacing) the `aria-describedby` attribute when the modal is closed or when the trigger is rendered, assistive tech will no longer associate the trigger with a non-existent tooltip/popup element. This prevents the “broken ARIA reference” error and avoids confusing behavior in screen readers.

#### Where this solution is applicable 
- Pop-ups, modals, and UI that can be dismissed/unmounted by users
- Anytime an HTML element gets removed from the DOM by a user interaction
- Particularly relevant for libraries like `reactjs-popup` that may inject ARIA attributes and/or clone/strip trigger props

#### Screenshots of WAVE Error

??? Info "1.01 Login Popup"


    ## 1.A Login Popup, Screenshot
    > ![Image](https://github.com/user-attachments/assets/2b60b5a1-e88e-4558-a7af-7d02321d411b)

    ## 1.B Login Popup, Screenshot of WAVE Annotations
    - this signifies that this HTML node contains an attribute, `role="tooltip"` (unrelated to the WAVE error in the Action Items)

    > ![Image](https://github.com/user-attachments/assets/ed8ee92f-44f7-4507-9158-317032ed4f1b)

    ## 1.C Login Popup, Screenshot of HTML
    - note the attribute, `id="popup-1"`

    > ![Image](https://github.com/user-attachments/assets/67f6a6bb-21b4-41dc-8995-d88c5ce41908)


??? Info "2. Login Link"

    ## 2.A Login Link, Screenshot

    ![Image](https://github.com/user-attachments/assets/dbf6a9ba-b8c4-4d31-a6e2-7c304cca48ea)

    ## 2.B Login Link, Screenshot of WAVE Annotations
    - Styles were removed to adequately show the WAVE annotation for the Login link
    - the WAVE Tool can disrupt styles in order to display the info sidebar, which effectively hid the Login link

    ![Image](https://github.com/user-attachments/assets/badefdca-387c-436a-b347-ec35c56bfe90)

    ## 2.C Login Link, Screenshot of HTML
    - note the attribute, `aria-describedby="popup-1"`

    ![Image](https://github.com/user-attachments/assets/14472348-665a-4ec9-acb6-b25eb70ad98f)

## Credits/Authors
All HfLA members who contributed to this wiki page and/or contributed to Pull Requests that provided solutions for this page.

- @ryanfchase 
- @Tony-Villa 
