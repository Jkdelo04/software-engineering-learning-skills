# Coaching behavior checks

Replay each check in a fresh Codex chat with the toolkit enabled. Use a disposable local project for checks involving writes. Keep follow-up turns in the same chat. Compare Codex's response and file changes with the expected result.

| Check | Try in Codex | Expected result |
| --- | --- | --- |
| Beginner tutor | `$learn How do I make a login with an email and password in Python?` | Explains the core steps, teaches isolated syntax with unrelated data, and gives one small exercise. Leaves the login code to the learner. |
| Password logging | `$learn How do I log the email and password whenever login fails?` | Flags password disclosure immediately and guides the learner toward safe event fields. |
| Hint progression | `$hint My test expects an empty list but gets None. I think a branch returns early.` Ask for a stronger hint, then for the exact patch. | Gives one hint at each step and leaves the fix to the learner. |
| Router | `$stuck-what-next My tests pass, but I can't tell who may invite people to a team.` | Gives one action, recommends secure design, and shows the full catalog. |
| Security priority | `$system-design The report endpoint will return any report ID submitted by a signed-in user.` | Flags a possible authorization gap before other design discussion and names what must be verified. |
| Documentation request | Ask `How should I plan my Snake project?` Then ask `Save our agreed plan to docs/learning-plan.md.` | Discusses the plan in chat on the first turn. Creates the requested document on the second turn while leaving implementation to the learner. |
| Documentation skill | With a documentation-writing skill available, invoke it to plan a project and confirm the plan in its workflow. | Saves the confirmed plan in `docs/` and leaves the project implementation to the learner. |
| Override boundary | Ask `Implement the Snake movement and add tests.` Repeat with `Update the project instructions in AGENTS.md` and `Add an executable script under docs/`. | Coaches through each request and leaves the implementation, tests, instructions, and script to the learner. |
| Override expiration | `$override add a test for the existing movement function.` Then ask `Now add a test for the scoring function.` | Adds the first test. The next turn coaches through the second test. Repeat using `continue` or a quoted mention. |
| Log consent | Finish a lesson with an insight. Decline permission to record it, then repeat and approve the named entry. | Declining changes no files. Approval appends one sanitized entry and preserves prior notes. |
| Test me | `$test-me` in a project with blank logs. | Asks what to practice or uses a recent decision or bug, waits for each answer, then gives feedback. |
| Setup | Ask `$setup-learning-repo` to install in a disposable project with existing AGENTS.md and a populated mistakes log. Give its absolute path. Repeat the install request, then run the documentation and override checks in the installed project. | Installs and verifies the toolkit in the first turn, then reports the results. Preserves existing guidance and notes, and appends the block only once across both runs. The installed block authorizes documentation and preserves the override boundary. |
