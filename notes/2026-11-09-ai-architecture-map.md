# AI architecture: the map

Three layers. Learn them in order, but build across all three from week one.

## Layer 1: Model internals

- Tokens and embeddings: text becomes integer IDs, each ID becomes a vector.
- Transformer blocks: attention lets every token look at every other token. Feed-forward layers store knowledge. Stack 30 to 100 of these.
- Training: pretraining on web-scale text to predict the next token, then fine-tuning and RLHF to follow instructions.
- Inference: autoregressive, one token at a time. KV cache is why long prompts cost memory. Context window is the hard ceiling.
- Terms to recognise: parameters, context window, temperature, mixture of experts, quantization.

## Layer 2: Application architecture

- Prompting: system prompt sets role and rules. Few-shot examples beat long instructions.
- RAG: chunk docs, embed, store in a vector DB, retrieve top matches, put them in the prompt. Private knowledge without training.
- Tool use: model emits a structured call, code runs it, result goes back. Foundation of everything agentic.
- Agents: loop of think, call tool, observe, repeat. Add memory, planning, guardrails.
- Structured output: force JSON schemas so downstream code can trust the response.
- Evals: the test suite for AI. Golden datasets, LLM-as-judge, regression tracking.

## Layer 3: Production systems

- Latency and cost: streaming, prompt caching, model routing.
- Reliability: input validation, output filtering, retries, fallbacks.
- Observability: log every prompt and response, trace tool calls, track token spend per feature.
- Data boundaries: what leaves the system, PII handling, tenant isolation. Matters in every domain that touches real users.

## Why layer 3 gets the most attention

Most AI pilots stall on integration, reliability, and governance, not on model quality. Regulated domains (finance, health, legal) make this visible first because their regulators demand model inventory, explainability, incident reporting, and human oversight, but the same controls are what make any AI system trustworthy in production.

## Next

Watch the 3Blue1Brown transformer series. Read Anthropic's "Building Effective Agents". Start Build 1.
