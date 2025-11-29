---
title: "Language Specific Knowledge: Do Models Know Better in X than in English?"
collection: publications
permalink: /publications/lskextractor
excerpt: ''
date: 2025-07-27
venue: arXiV
paperurl: 'https://arxiv.org/abs/2505.14990'
authors: 'Ishika Agarwal*, Nimet Beyza Bozdag*, Dilek Hakkani-Tür'
---

[Paper](https://arxiv.org/abs/2505.14990)
[Code](https://github.com/agarwalishika/LSKExtractor)
[Thread](https://x.com/wonderingishika/status/1926468812691431731)

Often, multilingual language models are trained with the objective to map semantically similar content (in different languages) in the same latent space. In this paper, we show a nuance in this training objective, and find that by changing the language of the input query, we can improve the question answering ability of language models. Our contributions are two-fold. First, we introduce the term Language Specific Knowledge (LSK) to denote queries that are best answered in an "expert language" for a given LLM, thereby enhancing its question-answering ability. We introduce the problem of language selection -- for some queries, language models can perform better when queried in languages other than English, sometimes even better in low-resource languages -- and the goal is to select the optimal language for the query. Second, we introduce simple to strong baselines to test this problem. Additionally, as a first-pass solution to this novel problem, we design LSKExtractor to benchmark the language-specific knowledge present in a language model and then exploit it during inference. To test our framework, we employ three datasets that contain knowledge about both cultural and social behavioral norms. Overall, LSKExtractor achieves up to 10% relative improvement across datasets, and is competitive against strong baselines, while being feasible in real-world settings. Broadly, our research contributes to the open-source development (this https URL) of language models that are inclusive and more aligned with the cultural and linguistic contexts in which they are deployed.