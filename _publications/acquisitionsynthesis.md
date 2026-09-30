---
title: "AcquisitionSynthesis: Targeted Data Generation using Acquisition Functions"
collection: publications
permalink: /publications/acquisitionsynthesis
excerpt: ''
date: 2026-05-15
venue: 'arXiv'
venue_short: 'arXiv'
selected: true
authors: 'Ishika Agarwal, Sofia Stoica, Emre Can Acikgoz, Pradeep Natarajan, Mahdi Namazifar, Jiaqi Ma, Dilek Hakkani-Tür'
paperurl: 'https://arxiv.org/abs/2605.13149'
links:
  - name: Paper
    url: https://arxiv.org/abs/2605.13149
  - name: Thread
    url: https://x.com/wonderingishika/status/2055031124292960434?s=20
---

Data quality remains a critical bottleneck in developing capable, competitive models. Researchers have explored many ways to generate top quality samples. Some works rely on rejection sampling: generating lots of synthetic samples and filtering out low-quality samples. Other works rely on larger or closed-source models to extract model weaknesses, necessary skills, or a curriculum off of which to base data generation. These works have one common limitation: there is no quantitative approach to measure the impact of the generated samples on the downstream learner. Active learning literature provides exactly this, in the form of acquisition functions. Acquisition functions measure the informativeness and/or influence of data, providing interpretable, model-centric signals. Inspired by this, we propose AcquisitionSynthesis: using acquisition functions as reward models to train language models to generate higher-quality synthetic data. We conduct experiments on classic verifiable tasks of math, medical question-answering, and coding. Our experimental results indicate that (1) student models trained with AcquisitionSynthesis data achieve good performance on in-distribution tasks (2-7% gain) and is more robust to catastrophic forgetting, and (2) AcquisitionSynthesis models can generate data for other models and for low-to-high resource training paradigms. By leveraging acquisition rewards, we seek to demonstrate a principled path toward model-aware self-improvement that surpasses static datasets.
