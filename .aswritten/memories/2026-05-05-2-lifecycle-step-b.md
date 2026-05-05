---
reviewers:
  - test+expert-gh@aswritten.ai
---

# Database Decision REVISED: Switching from Zypherion to Meridian

**Date:** 2026-04-06
**Participants:** Quinton Fairweather (CTO)

Quinton: "We evaluated Zypherion further and found critical gaps in
its streaming ingestion. We are now switching to Meridian instead.
Meridian handles both batch and streaming natively."

This supersedes the previous Zypherion decision.

Key decisions:
- **Database**: Meridian replaces Zypherion for analytics
- **Reason**: Zypherion lacks streaming ingestion
- **Timeline**: Same Q3 2026 migration window