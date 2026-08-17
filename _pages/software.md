---
layout: page
permalink: /software/
title: software
description: I release the methods in my papers as maintained software.
nav: true
nav_order: 4
---

Two of these libraries are used outside my own group.

---

## PhysioEx — *physiological signal explainer*

{% include figure.liquid loading="eager" path="assets/img/projects/physioex.jpg" class="img-fluid rounded z-depth-1" %}

A PyTorch library that puts **12 clinical cohorts behind one declarative interface**, so that
training a state-of-the-art model on physiological signals is a command and the research effort
goes into explaining it. It fixes subject-wise splits and seeds, ships staging architectures and
pretrained encoders, and carries an explainability subsystem. Roughly 46,500 lines across 207
modules, with continuous integration on two Python versions and automated releases to PyPI.
Described in *Physiological Measurement* (2025).

Models distributed through PhysioEx were used as **external-validation baselines** by Thapa et al.,
*Nature Medicine* (2026).

[Docs](https://guidogagl.github.io/physioex/) ·
[PyPI](https://pypi.org/project/physioex/) ·
[GitHub](https://github.com/guidogagl/physioex) ·
[Paper](https://doi.org/10.1088/1361-6579/adaf73)

---

## ProtoSleepNet — *prototype-based interpretable sleep staging*

{% include figure.liquid loading="lazy" path="assets/img/projects/protosleepnet_demo.jpg" class="img-fluid rounded z-depth-1" %}

Reading the prototypes *is* reading the decision: the model classifies a sleep epoch by matching it
against learned micro-structural patterns, and those patterns are the explanation. Trained and
evaluated across **11 polysomnography datasets and 12,317 subjects**. MIT licensed and built on
PhysioEx; the pretrained weights are released on Hugging Face together with the paper.

The demo below is the fastest way to see what the model is doing — pick an epoch, see its nearest
prototype, and see the time–frequency evidence behind the match.

[**Live demo**](https://protosleepnet-demo.pages.dev) ·
[Docs](https://guidogagl.github.io/protosleepnet) ·
[GitHub](https://github.com/guidogagl/protosleepnet) ·
[Preprint (v2)](/assets/pdf/papers/gagliardi2026prototype-v2.pdf) ·
[Research Square (v1)](https://doi.org/10.21203/rs.3.rs-9169987/v1)

---

## Spectral Gradients — *disentangled time–frequency attributions* <small>(manuscript in preparation)</small>

{% include figure.liquid loading="lazy" path="assets/img/projects/spectralgradients.jpg" class="img-fluid rounded z-depth-1" %}

An attribution method that separates a network's evidence **in time** from its evidence **in
frequency**, so that an explanation over a physiological signal can be read as "this rhythm, at this
moment" rather than as an undifferentiated heatmap. It combines progressive band ablation in the
frequency domain with path-integrated gradients, and is benchmarked against nine STFT-explainer
configurations across synthetic, audio, arrhythmia and sleep data. Manuscript in preparation with
Prof. W. Samek (Fraunhofer HHI).

*Code to be released with the paper.*

---

## Also in development

Not yet public — these are released as the corresponding papers appear.

**EEGBenchmarks** — an extension-oriented benchmark harness for EEG: datasets, wrappers for
foundation and supervised models, downstream evaluation tasks, and preprocessing and reporting
workflows.

**agentic-aasm-staging** — neuro-symbolic explainable sleep staging: retrieval over the AASM manual
selects the rule, a deterministic engine decides the stage, and a local language model writes the
justification. A demonstrator for auditable clinical reasoning, not a state-of-the-art classifier.

**eeg-signal2text-survey** — a survey and empirical probe of signal-to-text models applied to single
EEG epochs, across four adaptation strategies. The finding is negative and worth stating: no
open-weight model is credibly zero-shot on EEG.
