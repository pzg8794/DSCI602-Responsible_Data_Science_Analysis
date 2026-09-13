# Source and Requirements Map

## Assignment coverage

| Requirement | Draft location | Evidence state |
|---|---|---|
| Capstone-specific artifact and decisions | Context and Fairness Objective | Names route selection, qubit allocation, entanglement success, latency, retries, and starvation |
| Affected stakeholders and groups | Context and Fairness Objective | Users/applications, operators, and prespecified service/flow cohorts |
| Established fairness terminology | Context and Fairness Objective; Risk Analysis | Demographic parity, equalized odds, calibration, allocative harm, pipeline bias, sequential feedback |
| Concrete failure modes | Risk Analysis | Measurement, representation, aggregation, evaluation, feedback, and threat-concentration risks |
| Literature-supported mitigation | Mitigations and Validation | Auditable traces, bounded mediation, service floor, matched stress tests, uncertainty reporting, rollback |
| Residual risk and trade-offs | Limitations and Broader Impacts | Throughput, latency, fidelity, group-definition legitimacy, simulator validity |
| Two body pages maximum | Compiled PDF pages 1-2 | References begin on page 3 |
| Six or more citations; four or more peer-reviewed/archival | Bibliography | Nine sources; eight peer-reviewed venue/journal sources plus one archival technical report |
| BibTeX and consistent style | `fairness_references.bib` | IEEE bibliography style |
| Conference template and venue framing | `fairness_analysis.tex` | Latest Overleaf-style `IEEEtran` conference format; explicit Limitations and Broader Impacts section |

## Reuse decisions

### Reused as foundation

- The DSCI 601 fairness report's view of fairness as a design requirement.
- The DSCI 601 fairness-aware bandits manuscript's sequential allocation model,
  missing-context risk, outcome-gap notation, and EQUITAS mediation concept.
- The DSCI 601/602 integration plan's quantum-first scope, candidate service
  measures, fairness score, and utility-equity framing.
- The current Overleaf quantum manuscript's IEEE conference format.

### Deliberately not reused as evidence

- Numerical fairness findings from prior clinical, bioinformatics, or writing-
  sample drafts.
- Claims that live quantum fairness mediation or DSCI 602 fairness experiments
  are complete.
- Demographic subgroup claims unsupported by the present simulator.
- Unsupported causal or deployment-impact claims from older EQUITAS drafts.

## Most useful scholarly foundations

1. Suresh and Guttag: identifies where harms enter across the ML life cycle.
2. Mehrabi et al.: provides a taxonomy of bias and fairness definitions.
3. Hardt et al. and Chouldechova: establish classification criteria and their
   limitations; used here to explain why they cannot be copied mechanically.
4. Joseph et al. and Chen et al.: ground fairness in sequential and contextual
   bandit allocation.
5. Li et al. and Cicconetti et al.: establish simultaneous quantum requests,
   scarce-capacity scheduling, service differentiation, and fair sharing.
6. Jain et al.: supplies a bounded resource-allocation fairness index.

## Author review questions

- Are latency-sensitive versus delay-tolerant flows the intended primary service
  groups, or should the paper use demand tiers or context-quality cohorts?
- Is demand-normalized access the primary fairness criterion the capstone will
  actually implement?
- What minimum fidelity or service constraint must never be relaxed for parity?
- Who should be accountable for changing fairness weights in a future deployment?
