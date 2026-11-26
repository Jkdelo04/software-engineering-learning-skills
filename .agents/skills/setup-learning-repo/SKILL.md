---
name: setup-learning-repo
description: Install toolkit skills, coaching instructions, and learning log templates when the learner requests setup for a named Codex project.
---

# setup-learning-repo

An install request that names the target project authorizes the toolkit writes below in the same run. For a preview request, report the planned changes and stop before writing. If the target is missing or ambiguous, ask which project to set up.

1. Identify the source toolkit checkout and an existing target project by absolute path. When only this skill was copied into the target, ask for the original toolkit checkout path. Resolve destinations under the target. Report and skip any link or junction that would redirect a planned write.
2. Inspect the source skill folders, four learning templates, and marked coaching block in AGENTS.md. Inspect existing target files. Prefer the active root AGENTS.override.md if one already exists, otherwise use AGENTS.md. A conflicting existing skill folder stays in place. When the target contains an identical copy of the setup skill alone, preserve it and continue with the remaining plan.
3. Recheck the target paths before writing. Copy complete missing skill folders under .agents/skills/ and only missing log templates under learning/. Append the marked coaching block once, preserving existing instructions. If paths have changed or coaching markers are malformed, skip the affected write and report it.
4. Verify the resulting files and report the target, installed paths, skipped paths, and conflicts. Tell the learner to open a fresh Codex chat in the target and try `$stuck-what-next`.

Setup authorization covers only the toolkit files in the named target. Leave application code, dependencies, global settings, and publishing in the learner's hands.
