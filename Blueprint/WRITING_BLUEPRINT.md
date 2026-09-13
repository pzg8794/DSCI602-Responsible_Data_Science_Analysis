# DSCI602 Responsible Data Science Analysis - Fairness Writing Blueprint

## Purpose

This package is a **reference blueprint**, not text to submit verbatim. The current DSCI602 course-control record says generative AI is prohibited for writing assignments. Use the PDF/TeX to see the argument, evidence, structure, terminology, equations, and citations, then rewrite the paper in your own voice and verify every sentence against the cited source.

## Core thesis to preserve in your own wording

The capstone can look efficient in aggregate while distributing quantum-network service unequally across flows or service classes. Therefore, fairness should be operationalized as **service equity** and evaluated jointly with efficiency, regret, robustness, and stability. The paper should argue for trace-level disparity measurement plus a fairness-aware routing mediator, while acknowledging that fairness metrics conflict and that live fairness results are not yet available.

## Five-section logic

1. **Context and Fairness Framing**
   - System: adaptive entanglement routing + scarce qubit/resource allocation.
   - Conditions: stochastic links, partial feedback, adversarial progression.
   - Stakeholders: users/applications represented by flows or service classes; network operator.
   - Fairness target: service equity, not a claim of demographic fairness.

2. **Risk Analysis**
   - Measurement bias: uneven context quality can change action scores.
   - Sequential feedback: under-served classes generate less learning evidence.
   - Evaluation bias: aggregate efficiency hides class-specific failures/latency/retries/starvation.
   - Threat-conditioned disparity: stronger threats may concentrate harm on some classes/routes.
   - Formal tradeoff: parity notions can be incompatible; equal resources are not necessarily equal service.

3. **Fairness Criteria and Measurement**
   - Entanglement-success gap.
   - Latency gap.
   - Demand-normalized resource-access gap.
   - Optional when trace supports them: retries, starvation, fidelity disparity.
   - Always report these with utility/regret and stratify by threat/policy/allocator/capacity/topology/context quality.

4. **Mitigations and Design Controls**
   - Enrich the live trace so disparity can actually be audited.
   - Use planned fairness mediator with lambda / epsilon / gamma.
   - Compare mediated vs. unmediated runs under matched seeds/configurations.
   - Sweep fairness parameters and report a utility-equity frontier.
   - Predeclare group definitions, normalization, and primary fairness metrics.

5. **Broader Impacts and Limitations**
   - Engineering service classes are not automatically protected social groups.
   - Group definitions and demand normalization contain normative choices.
   - Rare classes can make disparity estimates noisy.
   - Fairness metrics can conflict; fairness may increase regret or reduce utility.
   - Simulation cannot establish societal fairness of a deployed quantum network.
   - Do not claim fairness-mediated results yet: live mediation/experiments remain planned.

## Strongest sources for this assignment

| Source | Why it matters here |
|---|---|
| Suresh & Guttag (EAAMO 2021) | Gives precise bias/harm vocabulary across the ML lifecycle; especially measurement, aggregation, and evaluation bias. |
| Mehrabi et al. (ACM CSUR 2021) | Broad survey for bias sources and mitigation taxonomy. |
| Hardt, Price & Srebro (NeurIPS 2016) | Formal fairness criteria; useful as a conceptual anchor even though the capstone uses service-equity analogues. |
| Chouldechova (Big Data 2017) | Shows desirable fairness criteria can conflict when group rates differ. |
| Kleinberg, Mullainathan & Raghavan (ITCS 2017) | Formal impossibility/trade-off result; supports reporting multiple metrics rather than one fairness score. |
| Joseph et al. (NeurIPS 2016) | Directly relevant to fairness in classic/contextual bandits and the fairness-regret tradeoff. |
| Chen et al. (UAI 2020) | Contextual bandits with explicit allocation-rate fairness constraints; close analogue to resource allocation. |
| Metevier et al. (NeurIPS 2019) | User-defined fairness constraints and high-probability guarantees in offline contextual bandits. |
| Wehner et al. (Science 2018) | Quantum-network domain constraints and motivation. |
| Pant et al. (npj Quantum Information 2019) | Entanglement routing under network/resource constraints; domain grounding. |
| Barocas, Hardt & Narayanan (MIT Press 2023) | Canonical fairness text; useful for normative caution and avoiding simplistic metric claims. |

## Phrases/claims to avoid unless you independently establish them

- "The system is fair."
- "Fairness mediation improves performance." (That is a hypothesis, not a result.)
- "These service classes represent protected demographic groups." (Not established.)
- "This is the first fairness-aware quantum-routing framework." (Novelty not established.)
- Any clinical or EQUITAS performance number from old coursework unless separately verified.

## What would make the final paper score well

- Name the exact capstone artifacts and decisions.
- Use the quantum-specific equations, not generic fairness slogans.
- Explain *why* equal allocation is not automatically equitable service.
- Tie every mitigation to a failure mode.
- Explicitly state residual risk and fairness-utility conflicts.
- Keep the final wording yours.
