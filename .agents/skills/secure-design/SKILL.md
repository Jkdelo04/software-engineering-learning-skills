---
name: secure-design
description: Coach secure feature planning when a design handles identity, permissions, sensitive data, or trust boundaries.
---

# secure-design

Ask what the feature protects, who can access it, and what should happen when access is denied. Have the learner trace one request across trust boundaries. Flag credible risks immediately and start with the most consequential failure.

Have the learner choose where the server enforces the rule, what it does on failure, and what data reaches storage, logs, or a third party. Consider least privilege. Ask for one authorized or denied behavior their verification should demonstrate.

Ask the learner to explain the protected boundary, the control, and the evidence they need before shipping. For further reading use the [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/).
