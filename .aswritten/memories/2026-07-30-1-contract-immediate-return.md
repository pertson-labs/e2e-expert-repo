---
reviewers:
  - xena+staging@aswritten.ai
---

# Contract check: the immediate-return remember

**Date:** 2026-04-06
**Participants:** Wynn Castellano (Staff Engineer)

Wynn: "We ratified the async job contract: remember returns a receipt in
seconds and the extraction is watched by polling a cursor. No blocking
call, and no lost work if the client drops the receipt."

Key decision: remember dispatches, then the agent either polls the run or
gets the reaction piggybacked on a later call.