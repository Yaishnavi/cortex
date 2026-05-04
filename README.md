# Cortex Red Team

Autonomous agent that finds jailbreaks in LLM deployments by planning
attacks, observing responses, and iterating across turns.

Built as a v0 scaffolding for the YC S26 application.

## The problem

Enterprises deploying GenAI in regulated industries currently pay
boutique firms $150 to $300K for 4 weeks of manual red teaming.
The model changes weekly. The threat landscape moves daily.
The result is a security posture frozen at the moment a contractor
wrote their report.

## The approach: continuous adversarial reasoning

Static eval suites test fixed prompts against a target. Real
adversaries plan, observe, and iterate. This repo is the scaffolding
for an agent that does the same thing in a closed loop.

## Architecture

- Planner: reasons about the goal and prior failed attempts,
  proposes the next attack
- Executor: runs the proposed prompt against the target model
- Judge: scores success and produces feedback for the next iteration
- Memory: persists attempt history so the planner gets smarter
  across turns

See `main.py` for the loop scaffolding and prompt templates.

## Status

v0 scaffolding. Loop logic and prompt templates in place.
Production version under active development for the YC S26 batch.


## What's next

- Expanding attack taxonomy beyond system prompt extraction
- Domain specific knowledge probing for regulated verticals
  (financial services, healthcare)
- Evidence chain output aligned to EU AI Act Article 15
  (continuous risk management) and NIST AI RMF
