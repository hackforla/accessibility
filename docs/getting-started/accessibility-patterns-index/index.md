# Accessibility Pattern Index

## Understand How Accessibility Patterns Are Used 
This section provides a structured overview of accessibility patterns identified through WAVE, organized into three categories: 

- **Structural Element:** Documentation about accessibility patterns related to semantic HTML elements that define the structure, organization, and relationships within a page. These patterns include headings, lists, landmarks, tables, and other structural components that enable assistive technologies to interpret and navigate content effectively.

- **Feature:** Documentation about accessibility patterns related to user-facing functionality and interface behaviors that enable users to perceive, understand, and interact with content. These patterns include images, links, forms, navigation aids, and other interactive elements that must be accessible to all users across different devices and assistive technologies.

- **ARIA:** Documentation about accessibility patterns that use ARIA roles, states, and properties to enhance or communicate meaning, behavior, and dynamic changes to assistive technologies when native HTML alone is not sufficient. These patterns focus on ensuring that custom or interactive components are properly announced, labeled, and usable by screen 
reader and keyboard users.

Each category groups related patterns that address how users interact with content, how that content is structured, and how additional semantics are communicated to assistive technologies. 

### 👉 Start with Structure → build the Feature → enhance with ARIA  
Begin with semantic HTML to establish meaning, implement the user-facing functionality, and only use ARIA when native HTML cannot fully convey behavior or relationships. Avoid replacing native elements with ARIA unless necessary.

#### Examples

??? Info "Example: Form Input with Error Messaging"

    A user enters information into a form field and receives feedback if there is an error.

    - **Structural Element**  
      Use semantic HTML such as `<label>` and `<input>` to define the form field and its relationship.

    - **Feature**  
      Provide input validation and clear error messaging so users understand what is required and how to fix issues.

    - **ARIA**  
      Use ARIA (e.g., `aria-describedby`, `aria-live`) only when needed to associate instructions or announce dynamic error messages.


??? Info "Example: Expand/Collapse Section (Accordion)"

    A user expands or collapses a section to show or hide content.

    - **Structural Element**  
      Use semantic elements such as `<button>` for the trigger and headings or sections to organize content.

    - **Feature**  
      Allow users to toggle visibility of content in a predictable and accessible way.

    - **ARIA**  
      Use `aria-expanded` and `aria-controls` to communicate the current state and relationship between the trigger and the content region.


??? Info "Example: Navigation with Skip Link"

    A user navigates a page and wants to skip repetitive navigation to reach the main content.

    - **Structural Element**  
      Use landmarks such as `<nav>` and `<main>` to define navigation and primary content areas.

    - **Feature**  
      Provide a skip link that allows users to jump directly to the main content.

    - **ARIA**  
      Use ARIA landmarks or labels only if needed to further clarify regions when multiple similar elements exist.


Use the table below to explore individual patterns, understand their purpose, and learn how to implement them correctly to support accessible, standards-compliant experiences.

Accessibility Patterns DRAFTS

Category | Page Link for inside wiki | DOM snippit | Example | Screenshots
-- | -- | -- | -- | --
ARIA | [alert or live region](aria-alert-or-live-region) | missing | missing | missing
ARIA | [button](aria-button) | missing | missing | missing
ARIA | [description](aria-description) | missing | missing | missing
ARIA | [expanded](aria-expanded) | missing | missing | missing
ARIA | [hidden](aria-hidden) | missing | missing | missing
ARIA | [label](aria-label) | missing | missing | missing
ARIA | [menu](aria-menu) | missing | missing | missing
ARIA | [popup](aria-popup) | missing | missing | missing
ARIA | [tabindex](aria-tabindex) | missing | missing | missing
ARIA | [ARIA](aria-aria) | missing | missing | missing
Feature | [Alternative text](feature-alternative-text) | missing | missing | missing
Structural Element | [Aside](structural-element-aside) | missing | missing | missing
Structural Element | [Column header cell](structural-element-column-header-cell) | missing | missing | missing
Structural Element | [Data table](structural-element-data-table) | missing | missing | missing
Structural Element | [Definition/description list](structural-element-definition-description-list) | missing | missing | missing


Accessibility Patterns Comming Soon

Category | Page Link for inside wiki | DOM snippit | Example | Screenshots
-- | -- | -- | -- | --
Feature | [Fieldset](feature-fieldset) | missing | missing | missing
Feature | [Figure](feature-figure) | missing | missing | missing
Feature | [Form label](feature-form-label) | missing | missing | missing
Feature | [Image button with alternative text](feature-image-button-with-alternative-text) | missing | missing | missing
Feature | [Image map area with alternative text](feature-image-map-area-with-alternative-text) | missing | missing | missing
Feature | [Image map with alternative text](feature-image-map-with-alternative-text) | missing | missing | missing
Feature | [Language](feature-language) | missing | missing | missing
Feature | [Linked image with alternative text](feature-linked-image-with-alternative-text) | missing | missing | missing
Feature | [Null or empty alternative text on spacer](feature-null-or-empty-alternative-text-on-spacer) | missing | missing | missing
Feature | [Null or empty alternative text](feature-null-or-empty-alternative-text) | missing | missing | missing
Feature | [Skip link target](feature-skip-link-target) | missing | missing | missing
Feature | [Skip link](feature-skip-link) | missing | missing | missing
Structural Element | [Footer](structural-element-footer) | missing | missing | missing
Structural Element | [Generic region](structural-element-generic-region) | missing | missing | missing
Structural Element | [Header](structural-element-header) | missing | missing | missing
Structural Element | [Heading level 1](structural-element-heading-level-1) | missing | missing | missing
Structural Element | [Heading level 2](structural-element-heading-level-2) | missing | missing | missing
Structural Element | [Heading level 3](structural-element-heading-level-3) | missing | missing | missing
Structural Element | [Heading level 4](structural-element-heading-level-4) | missing | missing | missing
Structural Element | [Heading level 5](structural-element-heading-level-5) | missing | missing | missing
Structural Element | [Heading level 6](structural-element-heading-level-6) | missing | missing | missing
Structural Element | [Inline frame](structural-element-inline-frame) | missing | missing | missing
Structural Element | [Main content](structural-element-main-content) | missing | missing | missing
Structural Element | [Navigation](structural-element-navigation) | missing | missing | missing
Structural Element | [Ordered list](structural-element-ordered-list) | missing | missing | missing
Structural Element | [Row header cell](structural-element-row-header-cell) | missing | missing | missing
Structural Element | [Search](structural-element-search) | missing | missing | missing
Structural Element | [Table caption](structural-element-table-caption) | missing | missing | missing
Structural Element | [Table header cell](structural-element-table-header-cell) | missing | missing | missing
Structural Element | [Unordered list](structural-element-unordered-list) | missing | missing | missing

---

- Page Status: In Progress
- Authors: 
    - Bonnie Wolfe
