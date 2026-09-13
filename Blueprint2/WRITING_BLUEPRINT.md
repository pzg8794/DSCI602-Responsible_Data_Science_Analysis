# DSCI602 Responsible Data Science Analysis — Writing Blueprint (Fairness, Option C)

**Due:** Sep 14, 2026, 11:59 PM ET (myCourses PDF upload — must click Submit and see "FILE SUBMISSION SUCCESSFUL")
**Companion files:** `main.tex` (skeleton) + `refs.bib` (12 verified entries) — upload both to Overleaf.
**Course rule:** individual assignment, personal writing; generative AI may not write it. This blueprint is structure and evidence only.

## The one-sentence thesis to build around

Aggregate-optimized quantum routing can hide per-class service disparities that only become visible under threat and capacity stress; because fairness definitions are mutually incompatible, the responsible design measures a utility–disparity frontier and mediates decisions explicitly rather than claiming a single fair metric.

## Section map and key points

### 1. Context (~250–300 words)
- The artifact: a quantum-network controller choosing entanglement routes and allocating qubits under five threat regimes (baseline → online-adaptive); inherited threat-aware bandit evaluation spine; your planned fairness mediation layer.
- The groups: flows / service classes with different demand, priority, and context quality.
- The decision at stake: who gets successful, timely service under scarcity.
- Anchor fact you may cite internally: the validated replay slice (efficiency 89.2 → 84.9 → 90.8 across capacity scales for one configuration) proves regime-dependent behavior hides inside aggregates — describe it as inherited baseline evidence, not a fairness result.

### 2. Risk Analysis (~500–600 words) — deepest section, rubric row 2 (25 pts)
- Pipeline bias mapping: name YOUR stages (measurement, evaluation, deployment) using Suresh & Guttag's lifecycle and Mehrabi's taxonomy.
- Definitions: per-class service parity vs error-rate parity; then the impossibility trio (Kleinberg; Chouldechova; Hardt) to justify frontier measurement over single-metric claims.
- Failure modes (write all three, concrete about who is harmed): (a) threat-regime concentration of retries/starvation on low-demand or poor-context flows; (b) fairness-through-unawareness — today's records lack demand/qubit/starvation fields, so disparity is currently invisible; (c) cross-regime transfer failure, with Gender Shades and Obermeyer as the documented precedent that aggregate metrics conceal group harm.

### 3. Mitigations (~350–450 words)
- Measurement first: D1 schema + per-class gap metrics (constructed-case unit tests; denominators and zero-demand rules).
- Intervention: the λ/γ/ε mediation score at a decided seam, evaluated off-vs-on (D2), framed as a trade-off dial.
- Process: datasheets/model-card documentation and the contribution ledger (D5).
- Residual risk stated plainly: impossibility means some disparity survives; mediation can cost utility — hence measure the frontier.

### 4. Limitations (~150–200 words, ACL-limitations voice)
- Prospective analysis; simulator lacks hardware-anchored timing/contention; service-class design can encode wrong groups; security/privacy intersections only by pointer.

## Source key points (what each citation contributes)

- **suresh2021** — harm enters at identifiable lifecycle stages; gives you the pipeline vocabulary.
- **mehrabi2021** — bias taxonomy and measurement/mitigation survey; your general grounding.
- **hardt2016** — equalized odds/opportunity; error-rate-based fairness.
- **chouldechova2017** — disparate impact in risk scores; calibration vs parity conflict.
- **kleinberg2017** — impossibility: fairness criteria cannot all hold together.
- **barocas2023** — canonical text; use for definitions and the unawareness caution.
- **buolamwini2018** — documented harm: aggregate accuracy hid intersectional error gaps.
- **obermeyer2019** — documented harm: a widely deployed algorithm's proxy choice produced racial bias.
- **mitchell2019** — model cards: documentation as accountability.
- **gebru2021** — datasheets: dataset/artifact documentation discipline.
- **gibney2020 / neuripschecklist / aclarr** — venue norms; why this analysis exists at all.

### Added after comparing against the ready-reference draft (gap-closing sources)

- **joseph2016** — fairness constraints change the regret cost of learning under uncertainty; the sequential-bandit-specific counterpart to the general lifecycle/taxonomy papers above. Use in Risk Analysis §1.
- **chen2020** — fair contextual multi-armed bandits with minimum service rates; supports both the feedback-loop risk (Risk Analysis §1) and the separable/auditable mediator design (Mitigations).
- **li2021** — quantum-network routing already schedules scarce capacity across simultaneous requests; a fair-sharing precedent native to the domain. Use in Context for specificity.
- **cicconetti2023** — service differentiation and fair sharing framed explicitly as a quantum-resource problem. Pairs with li2021 in Context.
- **jain1984** — a citable, formal disparity/fairness index (or demand-normalized access) to anchor the frontier claim in Risk Analysis §2 with a concrete metric instead of prose alone.

## Pre-submission checklist

- [ ] Body ≤ 2 pages excluding references (compile and count)
- [ ] Header shows name, capstone title, "Focus Area: Fairness", and your subtitle
- [ ] ≥6 citations, ≥4 peer-reviewed/archival (16 available in refs.bib after the gap-closing additions), bibtex, one consistent style
- [ ] Section headings present; conference-template bonus framing (limitations/broader-impacts voice)
- [ ] No completed-fairness-results claims; clinical work framed as prior infrastructure only
- [ ] PDF export → myCourses upload → click Submit → capture the success screen as your receipt

## Suggested schedule

- Tonight (Sep 13): draft Context + Risk Analysis (~2.5–3 h)
- Tomorrow afternoon: Mitigations + Limitations + references QA (~2 h)
- Tomorrow evening (buffer before 11:59 PM): compile, page-limit check, submit, save receipt
