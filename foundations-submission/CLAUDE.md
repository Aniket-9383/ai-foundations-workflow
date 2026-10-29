# Capstone AI Development Rules

Stack: JavaScript, Node.js, HTML, CSS. Inspect the actual repository before changing these assumptions.

1. Every settings-form input must have a visible `<label>` connected using matching `for` and `id` attributes.
2. Display names must be trimmed and nonempty; email addresses must be validated before saving. Invalid submissions must not update stored settings and must show field-specific errors.
3. Any settings-form change must include tests covering a valid submission, an empty or whitespace-only name, and an invalid email. Run the tests and report their actual result.
4. AI assistants must first inspect existing files and propose a short plan before editing. Do not claim a test passed unless its command was run.
5. Preserve existing project conventions; document changed files and user-visible behavior in the final summary.
