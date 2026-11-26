---
name: codebase-conventions
description: Coach learners on file placement and readable code when drafting a project style guide, placing a feature or test, or reviewing a repository at a milestone.
---

# codebase-conventions

Help the learner choose conventions a contributor can use to find, read, and change code. The learner makes project decisions, edits code, and runs checks.

## Scan and ask

1. Start with a read-only scan. When establishing conventions or reviewing a milestone, inspect the repository tree, README, existing style or contribution guides, manifests, and formatter, linter, and test configuration. Sample source and tests to see how the conventions work in practice. For a file-placement question, focus on the affected package, adjacent files, and their tests. Use file listings and configuration to identify generated output, dependencies, and local secrets without opening their contents.
2. Summarize what the paths and files show about the stack and current conventions. Ask the learner to confirm what they are building and fill in context that affects the advice, such as audience, project stage, expected changes, or review scope. Use answers already given. If the repo is empty or sparse, say what exists and use the planned stack to discuss a starting layout.

## Draft or use the style guide

3. Use the current guide as the review baseline if there is one. Check it against framework-required paths, configured tooling, and actual code. Bring conflicts to the learner with an example and resolve them before treating a proposed convention as agreed. Create or revise guidance when the learner is establishing conventions or a real change exposes a gap.
4. When drafting or revising the guide, help the learner write a short set of conventions covering the conventions that matter now. Ground each choice in a project example and explain what it helps a contributor do.

   - **File placement and names.** Check whether someone can locate an entry point, its tests, and related configuration, assets, or data. Group files that change together and keep the layout proportional to the project. Compare feature folders with a flat or layered layout when that choice affects where the next change would go. Use descriptive names that match the language and framework.
   - **Code readability.** Use representative files to discuss names that communicate intent, focused functions and modules, and comments that explain decisions or constraints. Link to existing formatter and linter settings for rules they enforce. Document decisions contributors still have to make themselves.

5. Show the proposed guide or edits and wait for the learner to approve the content before saving. Update the existing reader-facing guide in place where project instructions permit. For a new guide, use `docs/style-guide.md`. Preserve unrelated content and verify the saved result.

## Practice on a real change

6. End each review with one exercise. For file placement, ask the learner to propose a location for the code and its test and explain where a teammate would look. For a milestone, use a concrete path or code sample and help the learner choose one improvement. Agree on an observable check, such as tracing a feature to its test, or running the existing build or targeted tests after a move. Have the learner perform the change and the check.

## References

- For layout choices, naming, and reproducibility across project sizes, use the [Broad Institute file structure guide](https://mitcommlab.mit.edu/broad/commkit/file-structure/).
- For web layout examples, use [GeeksforGeeks web project organization](https://www.geeksforgeeks.org/javascript/file-and-folder-organization-best-practices-for-web-development/).
- For language-specific readability conventions, start with the relevant [Google Style Guide](https://google.github.io/styleguide/) or the language or framework's official guidance.
