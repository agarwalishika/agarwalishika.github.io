---
title: "A Rising Tide Lifts All Boats: MTQE Rewards for Idioms Improve General Translation Quality"
collection: publications
permalink: /publications/risingtide
excerpt: ''
date: 2026-10-23
venue: 'EMNLP'
venue_short: 'EMNLP'
selected: false
authors: 'Ishika Agarwal*, Zhenlin He*, Dhruva Patil, Dilek Hakkani-Tür'
paperurl: 'https://arxiv.org/abs/2601.06307'
links:
  - name: Paper
    url: https://arxiv.org/abs/2601.06307
  - name: Code
    url: https://github.com/agarwalishika/RisingTide
  - name: Thread
    url: https://x.com/wonderingishika/status/2011177433358389495?s=20
---

Non-compositional expressions (e.g., idioms, proverbs, and metaphors) pose significant challenges for neural machine translation systems because their meanings cannot be derived from individual words alone. These expressions encode rich, cultural meaning, and have both figurative and literal meanings, making accurate translation difficult. Because models are fairly good at translating compositional text, we investigate GRPO-style fine-tuning using Machine Translation Quality Estimation (MTQE) models as reward functions to train models to better translate idioms. Using Chinese and Hindi idiom datasets, we find that idiom translation abilities improve by ~14 points, general, non-idiomatic translation implicitly improves by ~8 points, and cross-lingual translation abilities (trained on one language, evaluated on another) improves by ~6 points. Overall, our work quantifies the non-compositional translation gap and offers insights for developing LLMs with stronger cross-cultural and figurative language understanding.

<small>* Equal contribution.</small>
