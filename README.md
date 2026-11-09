# AI Architecture Journal

A public record of learning AI architecture from the point of view of a payments and compliance engineer. Each session is a commit. Each week is a post.

Angle: AI systems for regulated finance. Payments, KYC, fraud, compliance. Every build is something only a fintech engineer would make.

## Layout

- `notes/` raw learning notes, one file per session, dated
- `builds/` small runnable projects, no frameworks unless they earn their place
- `posts/` LinkedIn drafts, one per week

## Roadmap

**Phase 1: Foundations (Nov to Dec 2026)**
Model internals: tokens, attention, context windows, KV cache, inference cost. Application layer: prompting, structured output, tool use, RAG, evals.
Build 1: a tool-calling agent on the raw API, no framework.

**Phase 2: First production grade system (Jan to Mar 2027)**
Build 2: RAG over regulatory documents (RBI circulars, FREE-AI report, DPDP rules). Chunking and retrieval evals with real numbers.
Controls: eval suite, prompt and model inventory, PII redaction, human in the loop.

**Phase 3: Agentic payments (Apr to Jun 2027)**
Build 3: an agentic payment flow under RBI's two factor mandate. Agent proposes, human approves, system executes, full audit trail.
Cost observability, latency budgets, model fallback, failure handling.

**Phase 4 onward (Jul 2027)**
Production topics: evals at scale, model risk governance, safety, cost. Talks and workshops if the writing finds an audience.

## Checkpoints

- End Dec 2026: 20+ commits, 6 posts
- End Mar 2027: one build used by someone other than me
- End Jun 2027: inbound interest from the fintech AI space

## Deliberately skipped

Certifications. Training models from scratch. Kaggle. Generic AI content.
