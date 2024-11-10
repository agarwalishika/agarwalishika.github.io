---
title: "DELIFT: Data Efficienct Language Model Fine-Tuning"
collection: publications
permalink: /publications/delift
excerpt: ''
date: 2024-08-09
venue: arxiv
paperurl: 'https://arxiv.org/abs/2411.04425'
authors: 'Ishika Agarwal, Krishna Killamsetty, Lucian Popa, Marina Danilevsky'
---

[Paper](https://arxiv.org/abs/2411.04425)
[Code](https://github.com/agarwalishika/DELIFT)
[Thread](https://x.com/wonderingishika/status/1854770402590851119)

Fine-tuning large language models (LLMs) is essential for enhancing their performance on specific tasks but is often resource-intensive due to redundant or uninformative data. To address this inefficiency, we introduce DELIFT (Data Efficient Language model Instruction Fine-Tuning), a novel algorithm that systematically optimizes data selection across the three key stages of fine-tuning: (1) instruction tuning, (2) task-specific fine-tuning (e.g., reasoning, question-answering), and (3) continual fine-tuning (e.g., incorporating new data versions). Unlike existing methods that focus on single-stage optimization or rely on computationally intensive gradient calculations, DELIFT operates efficiently across all stages. Central to our approach is a pairwise utility metric that quantifies how beneficial a data sample is for improving the model's responses to other samples, effectively measuring the informational value relative to the model's current capabilities. By leveraging different submodular functions applied to this metric, DELIFT selects diverse and optimal subsets that are useful across all stages of fine-tuning. Experiments across various tasks and model scales demonstrate that DELIFT can reduce the fine-tuning data size by up to 70% without compromising performance, offering significant computational savings and outperforming existing methods in both efficiency and efficacy.