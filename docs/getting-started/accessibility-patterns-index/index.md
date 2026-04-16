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


<details><summary>Example: Expand/Collapse Section (Accordion)</summary>

A user expands or collapses a section to show or hide content.

- **Structural Element**  
  Use semantic elements such as `<button>` for the trigger and headings or sections to organize content.

- **Feature**  
  Allow users to toggle visibility of content in a predictable and accessible way.

- **ARIA**  
  Use `aria-expanded` and `aria-controls` to communicate the current state and relationship between the trigger and the content region.

Use the table below to explore individual patterns, understand their purpose, and learn how to implement them correctly to support accessible, standards-compliant experiences.
</details>


<details><summary>Example: Navigation with Skip Link</summary>

A user navigates a page and wants to skip repetitive navigation to reach the main content.

- **Structural Element**  
  Use landmarks such as `<nav>` and `<main>` to define navigation and primary content areas.

- **Feature**  
  Provide a skip link that allows users to jump directly to the main content.

- **ARIA**  
  Use ARIA landmarks or labels only if needed to further clarify regions when multiple similar elements exist.
</details>

[INSERT TABLE]

---

- Page Status: In Progress
- Authors: 
    - Bonnie Wolfe
