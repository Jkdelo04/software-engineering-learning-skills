# Software-Engineering-Learning-skills

An open-source, security-first Codex coaching toolkit for computer science students and early-career software engineers. Use AI to learn coding and system design through your own projects. Make decisions, verify how your software behaves, and practice explaining your reasoning for interviews.

## The Main Flow

Follow this order to turn a project idea into something you can build, verify, and explain. The prompts below follow one example, a Python command-line to-do list. Paste them into Codex chat and adapt them to your project.

1. **Set up the toolkit with `$setup-learning-repo`.** Create a project folder if you need one. Open this toolkit folder in Codex and send `$setup-learning-repo Install the toolkit in <absolute path to my project folder>.` Replace the placeholder with your project’s full path. Review and approve the proposed file changes, then open a fresh Codex chat in your project folder. If you already installed the toolkit there, start at step 2. See [setup details](#set-up-another-project).
2. **Choose what to learn with `$lets-learn`.** Send `$lets-learn I want to build a Python command-line to-do list and learn to test it.` Decide with Codex what the first version should do and confirm the lesson brief.
3. **Make a plan with `$to-learning-plan`.** In the same chat, send `$to-learning-plan Turn our brief into phases I can verify.` Review the phases and their completion checks, then approve saving the plan to `docs/learning-plan.md`. You can also ask for one GitHub issue per phase and approve the issue content before publishing.
4. **Build and verify with `$test-first`.** Start with a phase you can work on and send `$test-first After I add "Buy milk", listing tasks should show "Buy milk".` Write and run the smallest test for that behavior, check that it fails for the expected reason, then implement the behavior and run the test again. Repeat for the next behavior.
5. **Explain what you learned with `$test-me`.** Answer the plan’s closing interview question, then try `$test-me Ask me why I chose that first test and what it leaves uncovered.` Use `$technical-interview` when you want a full mock interview on your project.

If you get stuck at any step, tell `$stuck-what-next` what you tried and what happened.

The interview and planning workflow draws on [Matt Pocock’s engineering skills](https://github.com/mattpocock/skills#readme).

## Start coaching

Open this folder in Codex and invoke `$stuck-what-next` with a project question, or start with `$learn` and a topic. Codex can inspect files and guide you. You write the solution, run the checks, and explain what you learned.

## Set up another project

1. Clone or download this toolkit. Open its folder in Codex so it can discover `$setup-learning-repo`.
2. Invoke `$setup-learning-repo` and give it the existing target project's absolute path. Review the file plan and approve the changes. If the session cannot write to the target, copy just `.agents/skills/setup-learning-repo/` into the target's `.agents/skills/`, open the target in Codex, and invoke the skill there with the source toolkit's absolute path.
3. Open a fresh Codex chat in the target and invoke `$stuck-what-next`. If you have nested project instructions, check that they preserve coaching where you want it.

For manual installation, copy the skill folders under `.agents/skills/` and the missing Markdown templates under `learning/` into your project. Copy the marked coaching block from [AGENTS.md](AGENTS.md) into your active root instructions. Preserve existing files and resolve overlapping skill names before copying.

## Skills

| Skill | Use it when |
| --- | --- |
| `$stuck-what-next` | You need one next action and a guide to the available skills. |
| `$learn` | You need a concept, vocabulary, or syntax explained with a small practice task. |
| `$lets-learn` | You want to decide what to build and what to learn through a project. |
| `$to-learning-plan` | You want to turn an agreed lesson into verifiable phases you can save or track in GitHub. |
| `$hint` | You want one hint for a blocker you are working through. |
| `$secure-design` | You are planning a feature that touches trust, permissions, or sensitive data. |
| `$security-review` | You want to review existing work for security risks. |
| `$system-design` | You need to compare designs and think through boundaries and trade-offs. |
| `$debugging` | The observed behavior differs from what you expected. |
| `$test-first` | You want to express a behavior as a small test before implementing it. |
| `$safe-change` | You need to change unfamiliar or weakly tested code. |
| `$test-me` | You want to recall or apply an idea and get feedback one question at a time. |
| `$technical-interview` | You want a mock technical interview using your codebase, with a grade and practice plan. |
| `$setup-learning-repo` | You want to install the toolkit in a project. |
| `$override` | You want Codex to carry out one named task this turn. |

During coaching, Codex can write reader-facing prose in `README.md`, `GLOSSARY.md`, and documentation files under `docs/`.

Code, tests, scripts, configuration, and agent instructions require `$override`. For example, `$override fix the failing CI configuration` delegates that task for the current turn. A follow-up such as “now fix the linter” starts in coaching. Setup and individual log entries have their own approvals. These workflow instructions work alongside Codex tool permissions.

## Learning logs

- [Mistakes](learning/mistakes.md) records bugs, misconceptions, and patterns to watch for.
- [Concepts](learning/concepts.md) records durable understanding.
- [Questions](learning/questions.md) tracks open questions worth revisiting.
- [Review](learning/review.md) holds retrieval prompts and review dates.

When something is worth recording, Codex names the file and asks before adding an entry. You can also write your own notes. Keep credentials and personal data out of the logs.

See the [reading guide](docs/reading.md) for the five books, Matt Pocock's skills, and defensive security references. Use the [example conversations](docs/behavior-checks.md) to evaluate changes to coaching.

[MIT License](LICENSE)
