# AI Architecture Journal

A public record of learning AI architecture end to end: model internals, application design, and production systems. Each session is a commit. Each week is a post.

The learning is general. The builds pull from different domains so the patterns get tested against different constraints: finance, healthcare, developer tools, logistics, consumer apps. Regulated systems show up often because they expose the hardest production problems, but they are not the only lens.

## Layout

- `notes/` raw learning notes, one file per session, dated
- `builds/` small runnable projects, no frameworks unless they earn their place
- `posts/` LinkedIn drafts, one per week

## Roadmap

Started 9 November 2026.

**Goal**
Become an applied AI architect who ships AI systems into production, with a payments and compliance background as one strength among several. Lock in the role during 2026 to 2027, while the AI skills premium in India is still high.

**Method**
Learn, build, write. Every session is a commit here. Every week is one post. Builds are the proof. Posts are the reach.

**Phase 1: Foundations (Nov to Dec 2026)**
- Model internals: tokens, attention, context windows, KV cache, inference cost
- Application layer: prompting, structured output, tool use, RAG, evals
- Build 1: a tool-calling agent on the raw API, no framework
- Target: 20+ commits and 6 posts by 31 December

**Phase 2: First production grade system (Jan to Mar 2027)**
- Build 2: RAG over a real document corpus, with chunking and retrieval evals and real numbers
- Controls every serious domain needs: eval suite, prompt and model inventory, PII handling, human in the loop
- Target: one build used by someone other than me

**Phase 3: Agents that act (Apr to Jun 2027)**
- Build 3: a multi-step agent that takes real actions. Agent proposes, human approves, system executes, full audit trail
- Cost observability, latency budgets, model fallback, failure handling
- Comment daily on others' work, pitch one meetup talk
- Target: first inbound conversation from someone building AI systems

**Phase 4: Convert (Jul to Sep 2027)**
- Three shipped builds and around 30 posts become the evidence for applied AI architect and Head of AI roles at product companies, banks, GCCs, AI labs, and cloud vendors

**Phase 5: Optional (Oct 2027 onward)**
- Paid workshops for companies if the writing built an audience. A course only after that. Founding only if a build turns into something people ask to pay for

## Checkpoints

- End Dec 2026: 20+ commits, 6 posts
- End Mar 2027: one build used by someone other than me
- End Jun 2027: inbound interest from people building AI systems
- If a checkpoint fails: do not add more learning. Ship more and write more specifically.

## Deliberately skipped

Certifications. Training models from scratch. Kaggle. Generic AI content. Courses, newsletters, or video in year one.
