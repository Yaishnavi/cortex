# References & Foundational Work

## Causal Inference — Core Theory

1. **Pearl, J.** (2009). *Causality: Models, Reasoning, and Inference* (2nd ed.). Cambridge University Press.
   — The foundational text. Structural causal models, do-calculus, counterfactuals. Everything Cortex builds on starts here.

2. **Pearl, J., Glymour, M., & Jewell, N.P.** (2016). *Causal Inference in Statistics: A Primer*. Wiley.
   — Accessible introduction to the mathematical framework. Good for translating theory into implementation.

3. **Peters, J., Janzing, D., & Schölkopf, B.** (2017). *Elements of Causal Inference: Foundations and Learning Algorithms*. MIT Press.
   — Bridges causal inference and machine learning. Covers causal discovery algorithms relevant to the Causal Discovery Engine.

4. **Spirtes, P., Glymour, C., & Scheines, R.** (2000). *Causation, Prediction, and Search* (2nd ed.). MIT Press.
   — Introduces the PC algorithm and constraint-based causal discovery. Core to automated causal graph construction.

## Causal Reasoning + LLMs

5. **Kıcıman, E., Ness, R., Sharma, A., & Tan, C.** (2023). "Causal Reasoning and Large Language Models: Opening a New Frontier for Causality." *arXiv:2305.00050*.
   — Key paper showing LLMs have implicit causal knowledge that can be extracted and formalized. Directly informs Cortex's approach.

6. **Jin, Z., Liu, J., Lyu, Z., et al.** (2024). "Can Large Language Models Infer Causation from Correlation?" *ICLR 2024*.
   — Benchmarks LLM causal reasoning capabilities. Identifies specific failure modes that Cortex aims to address.

7. **Ban, T., Chen, L., Wang, X., & Chen, H.** (2023). "From Query Tools to Causal Architects: Harnessing Large Language Models for Advanced Causal Discovery from Data." *arXiv:2306.16902*.
   — Explores using LLMs as active participants in causal discovery, not just query tools.

## Causal Discovery Algorithms

8. **Zheng, X., Aragam, B., Ravikumar, P., & Xing, E.P.** (2018). "DAGs with NO TEARS: Continuous Optimization for Structure Learning." *NeurIPS 2018*.
   — NOTEARS algorithm. Reformulates causal graph discovery as a continuous optimization problem. Relevant to scalable implementation.

9. **Chickering, D.M.** (2002). "Optimal Structure Identification with Greedy Search." *JMLR, 3*, 507–554.
   — Greedy Equivalence Search (GES). Score-based causal discovery approach.

## Agentic AI + Reasoning

10. **Yao, S., Zhao, J., Yu, D., et al.** (2023). "ReAct: Synergizing Reasoning and Acting in Language Models." *ICLR 2023*.
    — ReAct framework for agentic reasoning. Cortex extends this with causal reasoning capabilities.

11. **Wei, J., Wang, X., Schuurmans, D., et al.** (2022). "Chain-of-Thought Prompting Elicits Reasoning in Large Language Models." *NeurIPS 2022*.
    — Chain-of-thought as a reasoning paradigm. Cortex asks: what if the chain of thought was causally structured?

## Counterfactual Reasoning

12. **Mothilal, R.K., Sharma, A., & Tan, C.** (2020). "Explaining Machine Learning Classifiers through Diverse Counterfactual Explanations." *FAT* 2020*.
    — Counterfactual explanations for ML. Connects to Cortex's goal of causal explainability in agent decisions.

---

*This list is actively maintained as Cortex development progresses.*
