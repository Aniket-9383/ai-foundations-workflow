# AI-Assisted Feature Development: Workflow Comparison

## Feature and experiment
The selected feature is a small settings form that saves a display name and an email address. The purpose of this exercise is to compare a one-sentence request with a structured, verifiable specification. The two implementations should be generated in separate AI sessions and saved to independent branches named `round-1-vague` and `round-2-specified`. This document is a **comparison worksheet**, not a claim that those branches have already been created or tested.

## Round one: vague prompt
Prompt: “Build a settings form for a user's name and email.”

Save the assistant's first working output without adding requirements. Record the exact files changed, whether the form starts, and the amount of time spent reviewing or fixing it. Check whether inputs have associated labels, whether empty values are accepted, whether invalid email addresses are rejected, and whether saving produces useful feedback. Do not assume any of these behaviors exist until you inspect the code and run it.

## Round two: precise prompt and verification
Start a fresh session on a branch created from the same base commit. Use the supplied `ROUND_2_PROMPT.md`, which specifies files, accessible labels, validation, boundary conditions, and automated tests. Ask the assistant to inspect the repository, outline a plan, implement the feature, write tests, and run them. Capture the actual test output and review the code before accepting it.

## Correctness, accessibility, and edge cases
Compare both implementations against the same checklist: nonempty trimmed name, valid email, no save when inputs are invalid, visible field-specific errors, keyboard-operable submit, programmatically associated labels, and confirmation after successful save. Compare the exact code changes using `git diff round-1-vague..round-2-specified -- .` after both branches are committed. Cite file paths and changed lines from that diff in the final version of this report. A more detailed prompt is not proof of higher quality; tests and review must demonstrate the difference.

## Review effort and AI mistakes
Record total elapsed time for each round, including prompting, code review, tests, and fixes. Identify at least one **actual** mistake found in AI output, such as a missing label or validation that only checks for `@`, and describe the correction. Do not present those examples as observed defects unless they really occurred. Add the precise diff references, test counts, and timing figures before submission.

## Lessons incorporated into project rules
The updated `CLAUDE.md` establishes three reviewable rules: settings fields must have associated labels, invalid inputs must block saving with field-specific feedback, and every settings-form change must include and run tests for valid and invalid input. These rules translate the exercise into a repeatable verification loop for later capstone work.
