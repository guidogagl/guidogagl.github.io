---
layout: page
permalink: /research/
title: research
description: The programme, and the record behind it.
nav: true
nav_order: 2
---

## Research programme

I build deep learning models for clinical neurophysiology that explain their own decisions — so
clinicians can audit them, and so their explanations can teach us something new about disease.

The core of this work is a clinical sleep profiling study at UZ Leuven, where we showed that deep
learning combined with concept-based explainability can do three things at once: stage sleep in
healthy subjects *and* in patients with Parkinson's disease and Alzheimer's dementia, through a
pipeline benchmarked against the AASM Manual for the Scoring of Sleep; reveal how sleep macro- and
micro-structure change under neurological disease; and turn that newly surfaced knowledge back into
a signal for detection and classification. The point is the third step. An explanation that only
reassures the clinician is a user-interface feature; an explanation that yields a measurable
disease marker is a scientific result.

The same pipeline is now being applied to narcoleptic mouse models with Prof. B. R. Kornum
(Department of Neuroscience, University of Copenhagen) and to patients with Alzheimer's disease and
REM Sleep Behaviour Disorder with J. Strøm (Center for Ear-EEG, Aarhus University).

So far this has been physiological signals, but nothing in the methodology is specific to them. My
next step is to extend it to other clinical modalities — medical imaging and the electronic health
record — and to embed it in agentic decision-support tools for high-stakes settings such as
neurocritical care.

---

<h2 id="trustworthiness">Trustworthiness</h2>

Measuring model performance beyond task accuracy: explaining the decision-making process,
quantifying uncertainty so that a model can abstain when the evidence is weak, and validating its
reasoning against established clinical guidelines — so that a clinician can understand, check and
trust the system before it enters a diagnostic workflow.

This is the line running from concept-wise granular computing
{% cite alfeo2023concept %} through instance-based explanations in a learned latent space
{% cite gagliardi2025building %} to prototype-based sleep micro-structure learning
{% cite gagliardi2026prototype %}, where reading the prototypes *is* reading the decision.
Alongside it sits the counterfactual line — a model-agnostic feature-importance measure matched
against expert knowledge {% cite alfeo2023matching %} and region-aware minimal counterfactual
rules {% cite gagliardi2025region %} — and the question of whether a visual explanation can be
validated at all rather than merely inspected {% cite gagliardi2025model %}.

<h2 id="knowledge-discovery">Knowledge discovery</h2>

Using AI not merely as an automation tool but as a *scientific instrument*: identifying complex,
previously unknown correlations in clinical data, whose explanation can yield new domain knowledge
about disease mechanisms.

In practice this means treating the learned representation as an object of study. Which
micro-structural patterns does a well-performing sleep model rely on, and do they change with
Parkinson's disease or Alzheimer's dementia? Injecting domain knowledge into the representation
rather than only reading it out is the complementary direction
{% cite gagliardi2023contrastive %}, as is exploiting the physical layout of the sensors
themselves {% cite gagliardi2023improving %}.

<h2 id="foundation-models">Foundation models and agentic AI</h2>

Engineering foundation models for neurophysiological signals with semantic embeddings, and
*agentic* systems that ground large-language-model reasoning in verifiable clinical knowledge
through retrieval — turning explainable representations into auditable, clinician-facing
decision-support tools.

Benchmarking is the prerequisite, and it is where this line currently sits
{% cite kontras2026neuroatlas %}; generalisation across cohorts is the other half of the problem
{% cite zvuloni2026multisource %}. The agentic side is deliberately exploratory: retrieval over
the AASM manual selecting the rule, a deterministic engine deciding the stage, and a language model
writing only the justification — see [agentic-aasm-staging](/software/).

---

## Supervision and mentoring

Between 2022 and 2026 I supervised **12 M.Sc. theses** at the University of Pisa — 10 as principal
advisor (*relatore*), one as co-advisor, one as tutor — together with Prof. M. G. C. A. Cimino and
Prof. A. L. Alfeo. Day-to-day supervision was mine: problem definition, method, experiments and
writing. Cimino and Alfeo were the formal supervisors.

**M. Manni** (2024) — *Enabling Concept-Embedding Models for Sleep Staging through Automatic
Prototype-Based Learning of Concepts.* The automatic prototype-discovery mechanism developed here
became a component of ProtoSleepNet.

**C. Daka** (2025) — *Extracting Region-Aware Counterfactual Rules for Model-Agnostic Explainable
Artificial Intelligence.* The same research line as our 2025 *Machine Learning* paper on
region-aware counterfactual rules. Now a PhD student at the University of Pisa, continuing on
explainable AI architectures.

**I. Grillo** (2026) — *Design and Development of a Transformer-Based Model for Subject-Invariant
R-Peak Localization in EEG Signals.* Now a PhD student at KU Leuven, working on explainable AI for
brain foundation models.

Two of these students went on to doctoral study, one of them in my own department.

<details markdown="1">
<summary>Full list of supervised theses (12)</summary>

Titles as deposited in the University of Pisa ETD archive.

| Defended | Role | Student | Deposited title |
|---|---|---|---|
| 23/09/2022 | advisor | F. Ritorti | Distance-based representation learning for recognizing emotions via EEG data |
| 18/11/2022 | advisor | N. Mota | Concept-wise architecture with topology learning for explainable emotion classification |
| 18/11/2022 | advisor | M. Martorana | A novel feature importance measure to explain the quality level prediction in Smart Manufacturing |
| 28/04/2023 | tutor | F. Marabotto | Explainable emotion recognition via a novel loss function based on informed contrastive learning |
| 16/06/2023 | advisor | G. Cancello Tortora | Analyzing brain data for robust emotion recognition via conceptual decomposition based on autoencoders |
| 16/06/2023 | advisor | L. Turchetti | Sleep stage recognition supported by instances-based explanation via contrastive learning |
| 22/09/2023 | advisor | T. Nocchi | Design and Experimental Evaluation of a Novel Model-Agnostic Feature Importance Measure for Quality Measures in Industrial Production Processes |
| 26/11/2024 | advisor | M. Manni | Enabling Concept-Embedding Models for Sleep Staging through Automatic Prototype-Based Learning of Concepts |
| 21/02/2025 | advisor | — | Analysis of a counterfactual-based feature importance measure: fidelity, computational cost and influencing factors |
| 21/02/2025 | co-advisor | E. Tinghi | A double quantization approach for autonomous concept learning in sleep staging |
| 02/10/2025 | advisor | C. Daka | Extracting Region-Aware Counterfactual Rules for Model-Agnostic Explainable Artificial Intelligence |
| 2026 | advisor | I. Grillo | Design and Development of a Transformer-Based Model for Subject-Invariant R-Peak Localization in EEG Signals |

</details>

---

## Funding

I have secured approximately **€200,000** in competitive personal funding, plus compute allocations
on three national and European supercomputers.

- **FWO Strategic Basic Research Fellowship** (mandate 1SH4Z24N), ~€131,000, 2023– — success rate
  below 20%.
- **FWO Travel Grant, Long Research Stay Abroad** (mandate V458425N), €9,900, 2025 — funded the
  research stay at Fraunhofer HHI.
- **Pegaso Scholarship**, Regione Toscana (Giovanisì), €61,300, 2021–2023.
- **Compute:** VSC (Flanders), LUMI (EuroHPC JU) and Leonardo/CINECA — all competitively allocated.

---

## Teaching and service

- **Guest Lecturer**, *Explainable & Trustworthy Artificial Intelligence*, Ghent University
  (UGain / VAIA professional course), 2026. Course coordinated by Prof. Dr. Femke De Backere.
- **Teaching Assistant**, *Biomedical Signal Processing*, KU Leuven, 2021–2026 — M.Sc. programmes in
  Biomedical Engineering and Electrical Engineering.
- **Submission Chair**, IEEE ICAI-TEMS 2026, Pisa.
- **Reviewer** for AAAI 2026 and *Journal of Ambient Intelligence and Humanized Computing*.
- Member of the **Sleep Revolution** network (Horizon 2020, grant agreement 965417).

---

## Collaborations

This work is done with Prof. W. Samek (Fraunhofer HHI Berlin) on attribution methods,
Prof. J. A. Behar (Technion) and Prof. A. L. P. Ribeiro (Universidade Federal de Minas Gerais) on
cross-cohort generalisation in physiological time series, Prof. B. R. Kornum (University of
Copenhagen) on narcolepsy models, Dr. J. Jiménez-García (University of Valladolid) on paediatric
sleep apnoea, and J. Strøm (Center for Ear-EEG, Aarhus University) on Alzheimer's disease and REM
Sleep Behaviour Disorder.

---

<div class="publications" markdown="1">
{% bibliography --cited %}
</div>
