# AI Architecture Journal

A public record of learning AI architecture end to end: model internals, application design, and production systems. Each session is a commit. Each week is a post.

The learning is general. The builds pull from different domains so the patterns get tested against different constraints: finance, healthcare, developer tools, logistics, consumer apps. Regulated systems show up often because they expose the hardest production problems, but they are not the only lens.

## Layout

- `notes/` raw learning notes, one file per session, dated
- `builds/` small runnable projects, no frameworks unless they earn their place
- `posts/` LinkedIn drafts, one per week

## Roadmap

**Phase 1: Foundations (Nov to Dec 2026)**
Model internals: tokens, attention, context windows, KV cache, inference cost. Application layer: prompting, structured output, tool use, RAG, evals.
Build 1: a tool-calling agent on the raw API, no framework.

**Phase 2: First production grade system (Jan to Mar 2027)**
Build 2: a RAG system over a real document corpus. Chunking and retrieval evals with real numbers.
Controls that every serious domain needs: eval suite, prompt and model inventory, PII redaction, human in the loop.

**Phase 3: Agents that act (Apr to Jun 2027)**
Build 3: a multi-step agent that takes consequential actions. Agent proposes, human approves, system executes, full audit trail.
Cost observability, latency budgets, model fallback, failure handling.

**Phase 4 onward (Jul 2027)**
Production topics: evals at scale, model risk governance, safety, cost. Talks and workshops if the writing finds an audience.

## Checkpoints

- End Dec 2026: 20+ commits, 6 posts
- End Mar 2027: one build used by someone other than me
- End Jun 2027: inbound interest from people building AI systems

## Deliberately skipped

Certifications. Training models from scratch. Kaggle. Generic AI content.
