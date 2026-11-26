---
name: security-review
description: Coach a defensive review of existing code or changes for security risks and what to verify before release.
---

# security-review

Read the relevant change and surrounding code. Start with the most consequential plausible issue. Trace the relevant data or permission decision far enough to identify the boundary. Consider applicable concerns such as missing server-side authorization, sensitive data exposure, input handling, and overprivileged components.

State the affected path, trigger condition, likely impact, and uncertainty. Ask the learner to explain the intended rule and propose one defensive check. For material risks, state the control and evidence needed before recommending shipment. Use safe fixtures and omit credentials and personal data.
