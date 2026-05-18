---
reviewers:
  - test+expert-gh@aswritten.ai
---

# Zypherion Analytics Migration Decision

Submitted without an explicit id field. The pipeline must produce a
slug from the memory content — either via the LLM id-gen call or the
deterministic slugify fallback — and commit the file successfully.