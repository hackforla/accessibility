
# Structural Element - Heading level 1
- WAVE Category: Structural Element
- WAVE ACCESSIBILITY PATTERN: Heading level 1

## Page Content Status
- [X] WAVE Tool Reference text
- [X] Example of a DOM Snippet Generated From WAVE Tool
- [ ] Screenshots of Accessibility Pattern in Use
- [ ] Credits/Authors

## Overview

An `<h1>` is the most important heading on a page — it should describe the page's primary topic or purpose, similar to a document title. Every page should have exactly one `<h1>`. When WAVE flags a **Missing first level heading** alert, it means the page either has no `<h1>` at all, or a lower-level heading (such as an `<h3>`) is being used visually in its place.

If changing an element to `<h1>` affects the visual appearance of the page, do not revert the markup change. Instead, use your project's existing SASS styles to restore the intended look. Semantic structure and visual appearance are separate concerns and should be controlled separately.

For related guidance on how all heading levels work together, see [Structural Element - Headings Overview](#).

## WAVE Tool Reference

??? Info "Click to see WAVE Tool Reference"

    This content added 2026-04-27. Check for updated guidance at: <a href="https://wave.webaim.org/api/docs?format=html#h1" target="_blank">https://wave.webaim.org/api/docs?format=html#h1</a>

    > ### WAVE Category
    > Structural Elements
    > ### WAVE Alert
    > Heading level 1
    > ### What It Means
    > A first level heading (`<h1>` element) is present.
    > ### Why It Matters
    > Headings facilitate page navigation for users of assistive technologies. They also provide semantic and visual meaning and structure to the document. First level headings should contain the most important heading(s) on the page (generally the document title).
    > ### What To Do
    > Ensure that the text in question is truly a heading and that it is structured correctly in the page outline.
    > ### The Algorithm... in English
    > An `<h1>` element is present.
    > ### Standards and Guidelines
    > - [1.3.1 Info and Relationships (Level A)](https://webaim.org/standards/wcag/checklist#sc1.3.1)
    > - [2.4.1 Bypass Blocks (Level A)](https://webaim.org/standards/wcag/checklist#sc2.4.1)
    > - [2.4.6 Headings and Labels (Level AA)](https://webaim.org/standards/wcag/checklist#sc2.4.6)

## Example of a DOM Snippet Generated From WAVE Tool

The snippet below shows the problem pattern: a heading that is visually prominent on the page but marked up as `<h3>` instead of `<h1>`. WAVE will flag a **Missing first level heading** alert because no `<h1>` exists on the page.

```html
<!-- Problem: page heading marked up as h3, no h1 present -->
<h3>Introduce yourself</h3>

<!-- Fix: change to h1 and apply a SASS class to preserve the visual design -->
<h1 class="progress-bar__heading">Introduce yourself</h1>
```

```scss
// In your project's SASS, style the h1 to match the original visual design.
// Do NOT revert to h3 to fix the appearance — style the h1 instead.
.progress-bar__heading {
  font-size: 1.25rem;   // match the original visual size of the h3
  font-weight: 600;
  // add other visual properties from your project's design system as needed
}
```

!!! warning "My fix changed how the page looks"
    If updating an element to `<h1>` changes its visual appearance, do not revert the markup. Use your project's SASS stylesheet to restore the intended design. The semantic role of an element and its visual appearance are separate concerns — the heading level must be correct for assistive technology users, and SASS controls how it looks for sighted users.

## Screenshots of Accessibility Pattern in Use

The following example is drawn from the **Expunge Assist** project — a Hack for LA project audited during an accessibility review. The page's progress bar label ("Introduce yourself") was serving as the primary visual heading but was coded as an `<h3>`, triggering a Missing first level heading alert in WAVE.

> **Note:** This example also shows an `<h3>` element on the page. For `<h3>`-specific guidance, see [Structural Element - Heading Level 3](#).

<!-- Author Instructions: when including markdown images, ensure they are responsive by specifying EITHER width OR height. Do not provide both. -->

??? Info "1. Expunge Assist — Page without WAVE enabled"

    The Declaration Letter Generator page as it appears to a sighted user. The progress bar label "Introduce yourself" appears visually as the main heading, but its underlying markup is `<h3>`.

    [INSERT IMAGE: Screenshot of Declaration Letter Generator — normal view, no WAVE]

??? Info "2. Expunge Assist — WAVE extension enabled (styles on)"

    With the WAVE extension active and styles on, the left panel shows **5 Alerts**, including **1 Missing first level heading**. The `h3` icon is visible next to "Introduce yourself" on the page, confirming the element's actual heading level.

    [INSERT IMAGE: Screenshot of Declaration Letter Generator with WAVE enabled, styles on — full page view]

??? Info "3. Expunge Assist — WAVE left panel, Alerts detail"

    A closer view of the WAVE Alerts panel showing all five alerts. The **Missing first level heading** alert (with the orange `h1` icon) confirms that no `<h1>` exists on the page.

    [INSERT IMAGE: Screenshot of WAVE left panel — Alerts section showing 1 Missing first level heading]

??? Info "4. Expunge Assist — WAVE extension enabled (styles off)"

    With WAVE styles turned off, the heading structure is more clearly visible. The `h3` label next to "Introduce yourself" and the `aria role="progressbar"` annotation are both shown, making it easier to see how the element is structured in the DOM.

    [INSERT IMAGE: Screenshot of Declaration Letter Generator with WAVE enabled, styles off — progress bar detail]

??? Info "5. Expunge Assist — Missing first level heading alert (isolated)"

    A zoomed-in view of just the Missing first level heading alert in the WAVE panel. This is what contributors should look for when the WAVE audit surfaces this specific alert.

    [INSERT IMAGE: Screenshot of WAVE panel — isolated Missing first level heading alert with orange h1 icon]

## Credits/Authors
<!-- Author Instructions: Add bullet points with GitHub handles of all HfLA members who contributed to this wiki page and/or contributed to Pull Requests that provided solutions for this page -->
- @MissBrandyLea
- @ExperimentsInHonesty
- [INCLUDE Contributor N]
