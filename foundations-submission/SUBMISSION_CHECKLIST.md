# Submission checklist

- [ ] Create `round-1-vague` from the common base and run the one-line prompt in Claude Code or Cursor; commit and push the result.
- [ ] Create `round-2-specified` from the same base; open a fresh AI session and use `ROUND_2_PROMPT.md`; commit and push.
- [ ] Run both branches and record actual behavior and test output.
- [ ] Run `git diff round-1-vague..round-2-specified -- .` and add specific file/line references to `WORKFLOW.md`.
- [ ] Replace the hypothetical AI-mistake examples with one real observed mistake and its fix.
- [ ] Record review times and test results in `WORKFLOW.md`.
- [ ] Commit and push the updated `CLAUDE.md` and final `WORKFLOW.md`.
- [ ] Submit the repository URL with both remote branches.

These starter files are not evidence that the AI runs, branch pushes, or tests happened.
