---
name: setup-learning-repo
description: Install toolkit skills, coaching instructions, and learning log templates in a target Codex project after the learner approves the file plan.
---

# setup-learning-repo

1. Identify the source toolkit checkout and an existing target project by absolute path. When only this skill was copied into the target, ask for the original toolkit checkout path. Resolve destinations under the target. Report and skip any link or junction that would redirect a planned write.
2. Inspect the source skill folders, four learning templates, and marked coaching block in AGENTS.md. Inspect existing target files. Prefer the active root AGENTS.override.md if one already exists, otherwise use AGENTS.md. A conflicting existing skill folder stays in place. When the target contains an identical copy of the setup skill alone, preserve it and continue with the remaining plan.
3. Show the target and exact files or folders to create, append to, skip, or flag. Ask for approval. Recheck approved paths before writing. Copy complete missing skill folders under .agents/skills/ and only missing log templates under learning/. Append the marked coaching block once, preserving existing instructions. If paths have changed or coaching markers are malformed, skip the affected write and report it.
4. Verify the approved writes and report conflicts. Tell the learner to open a fresh Codex chat in the target and try `$stuck-what-next`.

Setup approval covers only the named toolkit files and target. Leave application code, dependencies, global settings, and publishing in the learner's hands.
