---
name: technical-interview
description: Run a mock technical interview on the learner's current codebase, optionally tailored to a role or employer, with a grade, mock hiring decision, and practice plan.
---

# Technical interview

## Intake and research

Ask what role, company, or field the learner wants to practice for and what seniority they are targeting, if known. Reuse details they already provided. If they give no interview target, run a general software engineering interview with no hiring research. Use the stated level or tell the learner you are using early-career expectations.

For a targeted interview, use the installed `$research` skill. Ask it to return cited findings in chat. A repository report requires a current-turn `$override` covering that write. If the skill or its delegation capability is unavailable, research public sources directly. Send only public targeting details to search or a research agent. Keep project code, secrets, and learner data out of that handoff.

Look for current job postings, prioritizing employer career pages, and identify the responsibilities and qualifications that should shape the interview. If you cannot verify a current posting for the employer, say so and look for current postings for comparable roles. Look for employer-published recruiting or candidate guidance on interview stages, formats, or evaluated skills. Share a short cited summary of what shaped the session. If the employer's interview process is undocumented, use the role requirements and label the format as your inference. If browsing is unavailable, use any posting or guidance the learner supplied and state how much tailoring the available evidence supports.

## Run the interview

Inspect relevant code, documentation, and existing checks read-only before choosing prompts. Plan four prompts by default: a code walkthrough, a debugging or testing scenario, a small hands-on task, and a design trade-off. Adapt the mix to the interview target and repository. In a docs-heavy repo, ask the learner to review or validate a real change. Use tasks small enough to assess in a single session and ground each prompt in a specific artifact or behavior the learner can inspect.

Before the first prompt, state the target level, the allowed tools, and which scoring areas are essential for the role. Allow repository navigation, documentation, and normal development tools by default. The learner owns their reasoning, code changes, and checks.

Present one prompt at a time and wait for the learner's answer or work. Ask follow-ups about their reasoning, trade-offs, or evidence. Before wrapping up, check that the session produced evidence for all four scoring areas and ask a follow-up if an area needs evidence. Clarify requirements freely. If asked for a hint, give a bounded hint and note any help that materially advanced the solution. Save solutions and coaching for the debrief. Raise credible security concerns promptly as required by project guidance.

## Debrief

At the end, score the evidence against the target level in four areas:

| Area | Evidence to consider |
| --- | --- |
| Codebase understanding | Traces relevant behavior and identifies the right files or boundaries. |
| Technical execution | Proposes or implements a workable solution and explains trade-offs. |
| Verification | Chooses checks that address the risk and interprets the results accurately. |
| Communication | Explains assumptions, decisions, and uncertainty clearly. |

Use **1** for below expectations, **2** for developing, **3** for meets expectations, and **4** for exceeds expectations. Cite an observed answer, action, or result for each score. Account for substantive hints in the affected area and distinguish proposed checks from reported results.

Average the assessed scores for the overall grade out of 4. Use the unrounded average for the verdict. Give a **Hire** verdict when the average is at least 3 and every area named essential before the interview scores at least 3. Give **No hire** when there is enough evidence to decide and the bar is unmet. If the session ends with too little evidence for a verdict, give a partial assessment, identify the unassessed areas, and state what evidence would complete it. Frame the verdict as a mock hiring decision for this interview.

End with three practice tasks in priority order. Tie each task to an observed gap or an area that still needs evidence, and give a success criterion the learner can check.
