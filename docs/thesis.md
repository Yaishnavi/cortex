# Cortex: Why Causal Reasoning is AI's Missing Layer

## Core Thesis

The current wave of AI — large language models, agentic systems, chain-of-thought reasoning — is built entirely on correlation. LLMs learn statistical associations from text. They can predict, summarize, and generate. But they cannot answer the most fundamental question in decision-making: *why?*

This is not a minor gap. It is the reason AI systems hallucinate confidently, fail at novel situations, and cannot be trusted for high-stakes decisions. Pattern matching breaks when the world changes. Causal reasoning doesn't.

## The Problem in Practice

I spent 3+ years building agentic AI diagnostics at Meta — automating root cause analysis across Instagram, Facebook, and WhatsApp's global telecom infrastructure serving hundreds of millions of users. The system worked well for known failure patterns. But every truly hard problem — the ones that cost millions in infrastructure decisions — required reasoning about causality:

- **Correlation traps:** Network latency and video quality degraded together. Were they causally linked, or both caused by a third factor? The LLM couldn't tell. A human investigator could.
- **Intervention reasoning:** If we reroute traffic through a different ISP, what happens to video quality? The system could show historical correlations but couldn't reason about the effect of an action it had never observed.
- **Counterfactual questions:** A major outage occurred. Would it have happened if we had upgraded the CDN last quarter? No amount of pattern matching answers this.

These aren't edge cases. They are the *central* questions in diagnostics, healthcare, policy, finance, and any domain where decisions have consequences.

## Why Now

Three converging trends make this the right moment:

1. **Agentic AI is exploding** — but agents acting on correlations in high-stakes environments is dangerous. The reliability gap is becoming a market blocker.
2. **Causal inference is mature** — Judea Pearl's structural causal models, do-calculus, and counterfactual frameworks have been mathematically rigorous for decades. The theory exists. The integration with modern AI does not.
3. **LLMs are surprisingly good at causal graph construction** — recent research shows that LLMs encode implicit causal knowledge from training text. The opportunity is to extract and formalize that knowledge, not start from scratch.

## The Cortex Approach

Cortex is not trying to make LLMs "understand" causality in a philosophical sense. It is an engineering approach: augmenting agentic LLM workflows with a structured causal reasoning layer.

Three components:

**Causal Discovery Engine** — Combines LLM-extracted causal knowledge with data-driven causal discovery algorithms (PC algorithm, GES, NOTEARS) to build and refine causal graphs for a given domain. The LLM proposes candidate causal structures; statistical tests validate or reject them.

**Intervention Simulator** — Given a causal graph, enables agents to reason about do-operations: "If I intervene on variable X, what is the expected effect on Y?" This uses Pearl's do-calculus to compute interventional distributions without requiring actual experiments.

**Counterfactual Reasoner** — Supports "what would have happened if..." queries by combining the causal graph with observed evidence. This is the hardest component and the most valuable — it enables agents to learn from past decisions in a way that pure correlation cannot.

## What Success Looks Like

A system where an AI agent, confronted with a complex diagnostic problem, can:

1. Build a causal model of the domain from data and prior knowledge
2. Identify root causes — not just correlated signals
3. Predict the effect of proposed interventions before executing them
4. Explain its reasoning in causal terms a human can verify

This is the difference between an AI that says "these variables are correlated" and one that says "changing X will fix Y, because X causes Z which causes Y, and here's the evidence."

## Open Questions

- How do you validate a causal graph when ground truth is unavailable?
- What is the right interface between LLM reasoning and formal causal models?
- Can causal reasoning improve agent reliability enough to unlock high-stakes autonomy?
- How do you handle domains with latent confounders that the LLM doesn't know about?

These are research questions I'm actively exploring.

---

*Vaishnavi Yeruva — [vaish.ai](https://vaish.ai)*
*April 2026*
