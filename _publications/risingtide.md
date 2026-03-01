---
title: "A Rising Tide Lifts All Boats: MTQE Rewards for idioms Improve General Translation Quality"
collection: publications
permalink: /publications/risingtide
excerpt: ''
date: 20256-01-05
venue: arXiV
paperurl: 'https://arxiv.org/abs/2601.06307'
authors: 'Ishika Agarwal*, Zhenlin Hi*, Dhruva Patil, Dilek Hakkani-Tür'
---

[Paper](https://arxiv.org/abs/2601.06307)
[Code](https://github.com/agarwalishika/RisingTide)
[Thread](https://x.com/wonderingishika/status/2011177433358389495?s=20)
[HuggingFace Collection](https://huggingface.co/collections/ishikaa/rising-tide)

Non-compositional expressions (e.g., idioms, proverbs, and metaphors) pose significant challenges for neural machine translation systems because their meanings cannot be derived from individual words alone. These expressions encode rich, cultural meaning, and have both figurative and literal meanings, making accurate translation difficult. Because models are fairly good at translating compositional text, we investigate GRPO-style fine-tuning using Machine Translation Quality Estimation (MTQE) models as reward functions to train models to better translate idioms. Using Chinese and Hindi idiom datasets, we find that idiom translation abilities improve by ~14 points, general, non-idiomatic translation implicitly improves by ~8 points, and cross-lingual translation abilities (trained on one language, evaluated on another) improves by ~6 points. Overall, our work quantifies the non-compositional translation gap and offers insights for developing LLMs with stronger cross-cultural and figurative language understanding.