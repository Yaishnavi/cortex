# Cortex

Causal reasoning for LLMs. 

Current AI systems find correlations but fail at cause and effect — making them unreliable for high-stakes decisions. Cortex embeds structured causal inference into agentic workflows so AI systems can reason about *why*, not just *what*.

## The Problem

LLMs are powerful pattern matchers, but they cannot:
- Distinguish correlation from causation
- Reason about interventions ("what happens if I change X?")
- Answer counterfactuals ("what would have happened if...?")

This makes them fundamentally unreliable for diagnostics, root cause analysis, planning, and any domain where understanding cause and effect matters.

## Approach

Cortex integrates causal inference methods — structural causal models, do-calculus, and counterfactual reasoning — into agentic LLM workflows. The goal is not to replace LLMs but to augment them with a causal reasoning layer.

Key areas of exploration:
- **Causal discovery** — extracting causal graphs from data and LLM knowledge
- **Intervention reasoning** — enabling agents to reason about the effects of actions
- **Counterfactual generation** — supporting "what if" reasoning in agent chains

## Status

🚧 Active research & development. Early-stage.

## Background

This work is informed by 3+ years building agentic AI diagnostics at Meta-scale (Instagram, Facebook, WhatsApp) where every hard problem came down to causality.

## Author

**Vaishnavi Yeruva** — [vaish.ai](https://vaish.ai) · [Google Scholar](https://scholar.google.com/citations?user=fhe95D0AAAAJ&hl=en) · [LinkedIn](https://www.linkedin.com/in/yaish/)

MS in AI, Northwestern · Research at IISc · 5 published papers (INTERSPEECH, ICANN, Speaker Odyssey)
