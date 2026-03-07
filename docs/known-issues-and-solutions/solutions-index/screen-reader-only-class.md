# Custom Screen Reader Only Class

We have created an `sr-only` class that will hide an element from the display for users that are not using a screen reader.
This is the same solution that libraries like `Bootstrap`

- <a href="https://getbootstrap.com/docs/5.0/getting-started/accessibility/">https://getbootstrap.com/docs/5.0/getting-started/accessibility</a>
- Also broken down here: <a href="https://kinaole.co/en/sr-only-just-a-class/">https://kinaole.co/en/sr-only-just-a-class</a>

## Example scss in TDM repo

- <a href="https://github.com/hackforla/tdm-calculator/blob/40cfb727672fd749980c7ff65d9272ba4f579cc7/client/src/styles/App.scss#L221">https://github.com/hackforla/tdm-calculator/blob/40cfb727672fd749980c7ff65d9272ba4f579cc7/client/src/styles/App.scss#L221</a>

## When to use this solution
- When WAVE calls for a label but the design does not have one
   - <a href="https://github.com/hackforla/tdm-calculator/blob/40cfb727672fd749980c7ff65d9272ba4f579cc7/client/src/components/Projects/ProjectsPage.jsx#L1148">https://github.com/hackforla/tdm-calculator/blob/40cfb727672fd749980c7ff65d9272ba4f579cc7/client/src/components/Projects/ProjectsPage.jsx#L1148</a>
- There is a table header that's empty but the column still has functionality to convey
   - <a href="https://github.com/hackforla/tdm-calculator/blob/40cfb727672fd749980c7ff65d9272ba4f579cc7/client/src/components/Projects/ProjectsPage.jsx#L1046">https://github.com/hackforla/tdm-calculator/blob/40cfb727672fd749980c7ff65d9272ba4f579cc7/client/src/components/Projects/ProjectsPage.jsx#L1046</a>
