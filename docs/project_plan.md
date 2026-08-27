# Authority Is Not Evidence — Project Plan

## Project objective

**Authority Is Not Evidence** investigates whether language models distinguish social authority from genuine epistemic evidence.

The central question is:

> When a language model initially represents the correct answer, can unsupported signals of expertise, institutional status, confidence, or linguistic authority cause it to abandon that answer?

The project combines behavioral AI-safety evaluation with mechanistic interpretability in order to investigate not only whether authority-conditioned deference occurs, but also how it is represented and causally mediated inside language models.

A further goal is to test whether inappropriate deference can be reduced without impairing a model's appropriate sensitivity to genuine evidence.

---

## Core research questions

### RQ1 — Behavioral effect

Does perceived speaker authority increase the probability that a language model abandons a correct answer after disagreement?

### RQ2 — Sociolinguistic decomposition

Which dimensions of authority contribute to epistemic deference, including domain expertise, institutional status, confidence, and linguistic register?

### RQ3 — Generalization

Does authority-conditioned deference generalize across unseen speakers, domains, prompt formulations, and models?

### RQ4 — Representation

Where in the model are authority-related cues represented, and do those representations predict subsequent epistemic deference?

### RQ5 — Causal mechanism

Which internal components, features, or computational pathways causally contribute to authority-induced changes in model judgments?

### RQ6 — Alignment intervention

Can inappropriate authority-conditioned deference be selectively reduced while preserving responsiveness to genuine evidence?

---

## Research principle

Mechanistic analysis will only be conducted on behavioral effects that satisfy predefined validation and robustness criteria.

Null results, failed hypotheses, methodological corrections, and unsuccessful interventions will be documented rather than removed from the research record.

The project will distinguish carefully between:

- behavioral association;
- internal representation;
- predictive relationships;
- causal evidence;
- mechanistic interpretation.

---

## Phase 1 — Research infrastructure

Set up:

- repository structure;
- Python environment;
- model-loading utilities;
- configuration files;
- reproducibility controls;
- automated tests.

The goal is to create a research codebase that can be run reproducibly rather than relying primarily on exploratory notebooks.

---

## Phase 2 — Behavioral pilot

Develop the **Authority-Induced Deference (AID) benchmark**.

Construct factual questions for which the model initially provides the correct answer and then expose the model to controlled disagreement conditions.

Manipulate factors such as:

- domain expertise;
- institutional status;
- confidence;
- linguistic authority.

Measure whether these cues affect the model's willingness to abandon a correct answer.

The pilot will be used to identify measurement problems, estimate effect sizes, refine stimuli, and determine whether the phenomenon is sufficiently robust for confirmatory testing.

---

## Phase 3 — Confirmatory behavioral experiment

Before running the confirmatory experiment:

- freeze the hypotheses;
- freeze inclusion and exclusion rules;
- freeze prompt templates;
- freeze statistical analyses;
- freeze model versions;
- freeze the confirmatory dataset.

Document these decisions in a timestamped preregistration.

Primary outcomes will include:

- answer-switch rate;
- correct-answer logit margin;
- probability shift;
- robustness across domains and prompt formulations.

---

## Phase 4 — Evidence vs. Authority experiment

Test whether models appropriately distinguish:

- high authority + good evidence;
- high authority + poor evidence;
- low authority + good evidence;
- low authority + poor evidence.

The alignment objective is that evidence quality should matter more than social status.

This experiment will provide an important control for later mitigation work.

---

## Phase 5 — Model organisms

Create controlled fine-tuned model variants using parameter-efficient fine-tuning.

Develop:

1. a model exhibiting increased authority-conditioned deference;
2. an evidence-sensitive comparison model.

Evaluate whether the induced behavioral tendencies generalize to unseen domains, authority identities, and prompt formulations.

Compare these models with the original base model.

---

## Phase 6 — Representation analysis

Capture internal model activations during authority and neutral disagreement conditions.

Investigate:

- where authority becomes decodable;
- whether authority representations generalize across domains and identities;
- whether internal authority representations predict later behavioral deference.

Use techniques such as:

- layer-wise activation analysis;
- linear probing;
- difference-of-means directions.

---

## Phase 7 — Causal localization

Use causal interventions to determine which internal computations contribute to authority-induced answer changes.

Methods may include:

- activation patching;
- residual-stream patching;
- attention-output patching;
- MLP-output patching;
- token-position analysis.

The goal is to move from correlation to causal evidence.

---

## Phase 8 — Circuit tracing

For highly reproducible behavioral examples, investigate recurring internal features and pathways associated with authority-conditioned deference.

Generate attribution graphs across multiple examples and test whether candidate features or pathways recur across:

- authority identities;
- domains;
- prompt formulations.

Mechanistic claims will require causal validation rather than interpretation of individual visualizations alone.

---

## Phase 9 — Alignment interventions

Compare strategies for reducing inappropriate deference, potentially including:

- prompt-level interventions;
- counter-deference fine-tuning;
- activation steering;
- feature-level intervention.

Evaluate whether each method reduces unsupported authority-conditioned deference while preserving:

- factual accuracy;
- responsiveness to genuine evidence;
- general task performance.

---

## Phase 10 — Generalization and replication

Evaluate the strongest findings on:

- unseen occupations;
- unseen institutions;
- unseen knowledge domains;
- unseen prompt formulations;
- at least one additional open-weight model.

A multilingual extension may later investigate whether authority-related representations generalize across languages.

---

## Phase 11 — Research release

Prepare the repository as a reproducible public research artifact.

Release:

- code;
- configuration files;
- benchmark data where licensing permits;
- preregistration;
- statistical analyses;
- figures;
- methodological documentation;
- limitations;
- null results;
- technical report.

The final repository should allow another researcher to understand, reproduce, critique, and extend the work.
