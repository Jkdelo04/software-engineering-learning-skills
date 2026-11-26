---
name: to-learning-plan
description: Turn a confirmed project-learning conversation or lesson brief into verifiable phases that the learner can approve and save as Markdown or publish as GitHub issues.
---

# To learning plan

Use the confirmed conversation or a supplied lesson brief. Carry forward the learner's goal, starting point, chosen language and frameworks, and evidence of success. Surface any unresolved decision that would materially change the phases and wait for the learner to settle it. For a lesson that still needs an interview, point the learner to `$lets-learn`.

Draft phases that each deliver a small, observable outcome the learner can build, test, or explain. Use end-to-end behaviors where practical so a learner can verify progress as each phase finishes. Give each phase a short title, a learning objective, one concrete learner-owned task, an observable completion check, and the phases that genuinely block it. Leave independent phases available to start. Close the plan with an interview-style prompt about a decision the learner will make, its trade-off, and the evidence behind it.

Show the proposed phases, their dependencies, and the intended destination. Invite the learner to adjust phase size, order, or checks. Wait for the learner to approve the breakdown and destination before saving or publishing.

- **Markdown by default.** Save one plan in `docs/learning-plan.md` in the learner's project, or at the Markdown path they agreed to. Include the lesson brief, phases, and closing prompt. If the file already contains a plan, confirm the intended update and preserve unrelated content.
- **GitHub Issues on request.** Confirm which GitHub repository belongs to the learner's project and obtain explicit approval to publish the previewed issue content there. Create one issue per phase in dependency order. Use native issue dependencies when supported, or link to prerequisite issues in the bodies. Include the closing prompt with the phase where the learner can answer it. Exclude credentials and personal data from issue content. If publishing stops partway through, report the created issues and what remains, and reuse the existing issues when resuming.

Return the saved plan path or issue links. The learner owns implementation, tests, and verification.
