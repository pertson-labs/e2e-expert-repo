---
reviewers:
  - xena+staging@aswritten.ai
---

# Deployment Gate Decision: Meridian Release Train

**Date:** 2026-07-02
**Participants:** Quinton Fairweather (CTO)

Quinton: "Every Meridian deployment now requires a signed release
manifest before it ships. We saw two unsigned artifacts reach staging
last quarter and that is the whole reason for the gate."

Key decisions:
- **Gate**: signed release manifest required for Meridian deploys
- **Scope**: applies to staging and production
- **Owner**: Quinton Fairweather