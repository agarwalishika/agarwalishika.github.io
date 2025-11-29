---
title: "Neural Networks for Learnable and Scalable Influence Estimation of Instruction Fine-Tuning Data"
collection: publications
permalink: /publications/nncift
excerpt: ''
date: 2025-12-03
venue: NeurIPS
paperurl: 'https://arxiv.org/abs/2502.09969'
authors: 'Ishika Agarwal, Dilek Hakkani-Tür'
---

[Paper](https://arxiv.org/abs/2502.09969)
[Code](https://github.com/agarwalishika/NN-CIFT)
[Thread](https://x.com/wonderingishika/status/1891335751360520241)

Influence functions provide crucial insights into model training, but existing methods suffer from large computational costs and limited generalization. Particularly, recent works have proposed various metrics and algorithms to calculate the influence of data using language models, which do not scale well with large models and datasets. This is because of the expensive forward and backward passes required for computation, substantial memory requirements to store large models, and poor generalization of influence estimates to new data. In this paper, we explore the use of small neural networks -- which we refer to as the InfluenceNetwork -- to estimate influence values, achieving up to 99% cost reduction. Our evaluation demonstrates that influence values can be estimated with models just 0.0027% the size of full language models (we use 7B and 8B versions). We apply our algorithm of estimating influence values (called NN-CIFT: Neural Networks for effiCient Instruction Fine-Tuning) to the downstream task of subset selection for general instruction fine-tuning. In our study, we include four state-of-the-art influence functions and show no compromise in performance, despite large speedups, between NN-CIFT and the original influence functions. We provide an in-depth hyperparameter analyses of NN-CIFT.