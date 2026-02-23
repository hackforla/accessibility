# Accessibility (WIP)

- Page Status: In Progress
- Current Authors: 
   - Ryan Chase
   - Bonnie Wolfe
---
## Table of Contents
- [Motivation for Accessibility Compliance](https://github.com/hackforla/tdm-calculator/wiki/Accessibility-Audits#motivation-for-accessibility-compliance)
- [TDM WAVE Audits](https://github.com/hackforla/tdm-calculator/wiki/Accessibility-Audits#tdm-wave-audits)

## Related page
- [WCAG: Known Issues and Solutions](known-issues-and-solutions/solutions-index/index.md)

### Motivation for Accessibility Compliance

As a site that will be managed by the city, we are committed to delivering a site that is compliant with modern accessibility standards. We will be using the WAVE browser extension to perform accessibility audits in order to ensure we meet WCAG2.2 standards.

#### WCAG 2.2 Accessibility Standards

> The WCAG documents explain how to make web content more accessible to people with disabilities. Web “content” generally refers to the information in a web page or web application
- https://www.w3.org/WAI/standards-guidelines/wcag/

> The WCAG 2.2 has 13 guidelines. The guidelines are organized under [4 principles: perceivable, operable, understandable, and robust](https://www.w3.org/WAI/WCAG22/Understanding/intro#understanding-the-four-principles-of-accessibility).
 For each guideline, there are testable success criteria. The success criteria are at [three levels: A, AA, and AAA](https://www.w3.org/WAI/WCAG22/Understanding/conformance#levels).

- https://www.w3.org/WAI/standards-guidelines/wcag/glance/

The success criteria are what determine “conformance” to WCAG. That is, in order to meet WCAG, the content needs to meet the success criteria. Details are in the [Conformance section of WCAG](https://www.w3.org/TR/WCAG22/#conformance).

#### WAVE Web Accessibility Evaluation Tools
> WAVE® is a suite of evaluation tools that helps authors make their web content more accessible to individuals with disabilities. WAVE can identify many accessibility and Web Content Accessibility Guideline (WCAG) errors, but also facilitates human evaluation of web content. Our philosophy is to focus on issues that we know impact end users, facilitate human evaluation, and to educate about web accessibility.
- https://wave.webaim.org/

> The WAVE Chrome, Firefox, and Edge extensions allows you to evaluate web content for accessibility issues directly within your browser. Because the extension runs entirely within your web browser, no information is sent to the WAVE server. This ensures 100% private and secure accessibility reporting.
- https://wave.webaim.org/extension/

### TDM WAVE Audits

#### How to Perform WAVE Audits
1. [Download the WAVE extension for your browser](https://wave.webaim.org/extension/)
2. Navigate to the page you want to run the extension on
3. Run the WAVE browser extension
   - "To run a WAVE report, simply click on the WAVE icon to the right of your browser address bar, or select "WAVE this page" from the context menu."
4. See the results from the Summary page and Details pane
   - see screenshots below

#### References

**Summary Pane**
<br/>
> <img height="670" alt="Summary pane" src="https://github.com/user-attachments/assets/e0eef2d2-6ae5-4c0f-87c9-7c6973398d86" />

<br/><br/>

**Details Pane**
<br/>
> <img height="670" alt="Details pane" src="https://github.com/user-attachments/assets/3681e541-6459-484a-9de2-d458991ad98a" />

---

#### Custom Screen Reader Only Class

We have created an `sr-only` class that will hide an element from the display for users that are not using a screen reader.
This is the same solution that libraries like `Bootstrap`
- https://getbootstrap.com/docs/5.0/getting-started/accessibility/
- Also broken down here: https://kinaole.co/en/sr-only-just-a-class/

**Link to css in repo**
- https://github.com/hackforla/tdm-calculator/blob/40cfb727672fd749980c7ff65d9272ba4f579cc7/client/src/styles/App.scss#L221

**Examples of when to use this solution**
- When WAVE calls for a label but the design does not have one
  - https://github.com/hackforla/tdm-calculator/blob/40cfb727672fd749980c7ff65d9272ba4f579cc7/client/src/components/Projects/ProjectsPage.jsx#L1148
- There is a table header that's empty but the column still has functionality to convey
  - https://github.com/hackforla/tdm-calculator/blob/40cfb727672fd749980c7ff65d9272ba4f579cc7/client/src/components/Projects/ProjectsPage.jsx#L1046





