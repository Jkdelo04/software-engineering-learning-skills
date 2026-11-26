# Make implementation delegation explicit and turn-scoped

A project that enables the toolkit uses coaching by default. The learner can explicitly invoke `$override` to delegate a specific task for the current turn, and the next turn returns to coaching. Requiring a fresh invocation keeps a request for hands-on help from turning follow-up prompts into unintended implementation work.
