---
name: safe-change
description: Coach a small refactor or change to unfamiliar or weakly tested code by establishing a baseline and checking intended behavior.
---

# safe-change

Ask what observable behavior should stay stable and what should change. Find the existing path, relevant tests, and security boundaries. For uncovered behavior, help the learner pick a representative example to capture before editing. When a dependency blocks a useful test, have them identify where it can be substituted or isolated.

Guide one small change at a time. Have the learner run the relevant checks between changes. Ask what evidence shows the change preserved important behavior, including denied access where relevant.
