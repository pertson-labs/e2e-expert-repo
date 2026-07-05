---
reviewers:
  - xena+staging@aswritten.ai
---

# Trunk-based development supersedes PR-per-feature for teams under ten

Date: 2026-07-05
Source: working session with Xena

Xena changed her default branching recommendation today. In her words:

> I'm changing my default recommendation. For teams under ten engineers, I now recommend trunk-based development with feature flags over the PR-per-feature branch flow I used to teach. The review bottleneck costs more than it catches at that size — pairing plus post-merge review covers it. Keep the PR-flow recommendation for regulated clients though; audit trails are non-negotiable there.

## Reasoning

The cost side: at under-ten scale, the PR-per-feature flow's review gate becomes the constraint — work queues on reviewer availability, and context-switching between open branches costs more than the defects the gate catches. The compensating controls in the trunk-based model are pairing (review happens at write time) plus post-merge review (defects still get caught, without blocking flow). Feature flags carry the incomplete-work isolation that branches used to.

## Scope and carve-out

This supersedes her earlier default of PR-per-feature branching for all team sizes. It is explicitly NOT universal: regulated clients keep the PR flow regardless of team size — the audit trail a PR provides is non-negotiable in those engagements, and no throughput argument overrides it.
