---
reviewers:
  - scarlet@aswritten.ai
  - +15555550100
---

# Multi-pass write model ratified: frozen referent sets, the ambiguity short-circuit, and the first authored reconciliation

## Context

July 5, 2026 — day one of the two-day Fable window allocated to the multi-pass extraction spike (task-146). Scarlet chose an architecture session before committing to an implementation slice: work the pipeline design against product-doc-v2, the Expression Graph proposal, and the live read path. The session ratified the write model, and the same afternoon the first authored reconciliation in the system's history round-tripped on a local stack — written through the real commit seam, rendered back as "⊕ RECONCILED (Scarlet, 2026-07-05)" in a live perspective response.

## The referent taxonomy — in-message commentary is free

Scarlet drew the distinction that reshaped the resolve pass's scope:

> "Any particular message can have both a set of primary source material about which there is commentary. That commentary is about primary source that is in this message, therefore it's an expression about an expression in this message. You can also have commentary that references other messages, and that's the reference that you're talking about — not only other messages, really ultimately other nodes in the graph, right?"

Commentary about source in the same message binds structurally — the envelope's decomposition already knows which commentary attaches to which source, so those bindings cost nothing and can never be ambiguous. Resolution is only ever needed for commentary reaching back into the graph. As she put it: "it's cool that you get resolved for free."

## Targets are not a query — the freeze rule

Scarlet pushed on "targets a named graph" as an oversimplification:

> "Each transaction is a named graph, so you could target multiple transactions by named graphs, but there are other cross-cutting things that someone could be referring to. It's basically a query. Yeah, so that resolution process is super important."

What a person concludes about is often cross-cutting — "everything we've said about enterprise pricing since March" — a reference no existing graph holds. The ratified resolution: resolution collapses the intensional reference into an extensional, frozen set at write time. Scarlet's formulation, verbatim:

> "You're definitely not saving a query. You're saving a concrete set of IRIs or named graphs."

Two reasons carry the decision — Claude-proposed in the session, Scarlet-ratified. Append-only semantics: a conclusion concluded over exactly what it saw — later-arriving nodes aren't retroactively covered; a later conclusion covers them, and the trajectory of conclusions does its job. And the guardrail: a stored query the read path re-evaluates is machinery deciding what a conclusion covers as the graph moves — the retired demotion engine returning through the referent side. The query-shaped phrasing survives as witnessed text inside the conclusion; what the conclusion binds is concrete.

A companion decision separates two roles that would otherwise blur: a conclusion's target is the graph-grain address whose digest should narrate it (a hub, a session's transaction, several of either); its referent bindings are the precise nodes it concerns, carried as typed relationships (extends / supersedes / contradicts). Folding referents into the target would make every correction surface on nodes it never concerned — the read-time bleed the June 24 session warned about, now located precisely and designed out.

## The ambiguity short-circuit — and why source always lands

Scarlet proposed the escape valve for unresolvable references:

> "There might need to be a short circuit where, if there's greater than a certain amount of ambiguity, you return to the user and say, 'Did you mean this set of references or these, or could it be these other ones? Can you please specify?' Maybe that's a tool that happens before, so you could pass the set of references explicitly into remember."

Ratified as: explicit referents can be passed into the write and skip resolution entirely; missing referents get a resolution pass; confident resolutions bind frozen; ambiguous ones bounce back with candidate sets — the one legitimate prompt in a disambiguate-never-ask-permission system. Crucially, source always lands regardless: it is an append-only record of what was said, and there is nothing ambiguous about that. Only the held commentary waits.

The follow-up needed no new machinery, which Scarlet spotted immediately:

> "We need to do a follow-up, which now is basically just a new memory... with everything that was already committed dropped from it, right?"

The bounce payload itself is the state — the held commentary returns as an ordinary commentary-only envelope with referents now explicit, through the same pipeline, no special mode, nothing held server-side. The unified write path paying for itself. One refinement pinned in the same exchange: the held commentary's witness chain anchors to the source committed in round one — it was said then; only the confirmation is new.

## Authorship provenance — a live gap the footing design answers

Reviewing this memory's draft, Scarlet flagged that the freeze rule's rationale must be attributed as Claude-proposed, Scarlet-ratified — and named the general problem:

> "We need to be able to handle these more nuanced author provenance relationships cleanly in v2. There are all sorts of memories that attribute Claude's words to me in the past."

This is a lived witness for the footing primitive (animator / author / principal): model speech carries no principal until a human endorses it, and endorsement is itself a recordable act distinct from authorship. The historical graph contains the failure mode footing is designed against — Claude-authored formulations recorded as Scarlet's words. This memory is deliberately its own first test case: the freeze rationale enters as Claude-authored, Scarlet-endorsed.

## The dogfood moment

The session closed its own loop: the first reconciliation ever authored concludes about the multi-pass pipeline's own design — the ratified write model, signed by Scarlet as principal, bound by typed edges to the June 24 design nodes it extends. Verified the same hour at the real seam — on an ephemeral local stack (worktree task-146-multipass), not the org perspective; the spike artifact lives and dies with that stack. Committed through the production commit path, returned in a live perspective response as the leading "⊕ RECONCILED" line, with a second test conclusion stacking above it as "earlier rebalancing" below — the trajectory-of-conclusions rendering that the conviction trajectory, and ultimately the fundraise demo's trajectory-grounded reactions, stand on.

## Deferred, deliberately

The resolve tool as a user-facing surface (the pass is the machinery; the tool is a registration away). A numeric ambiguity threshold — the pass judges confident/ambiguous/new qualitatively until the gold set provides calibration data; in the interim: confident when navigation converges on a single dominant referent set at a determinate grain, ambiguous when more than one candidate set fits comparably (or the same name matches multiple nodes at one grain), new when no prior plausibly matches at any grain. Segmentation grain defaulted to one speech act per expression, logged as tunable. Directional dimensions this window: the Conviction spine only — ship spines, gate facets.