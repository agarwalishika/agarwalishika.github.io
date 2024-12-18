---
title: "Neural Active Learning Beyond Bandits"
collection: publications
permalink: /publications/neural_bandits
excerpt: ''
date: 2024-05-11
venue: ICLR
paperurl: 'https://arxiv.org/abs/2404.12522'
authors: 'Yikun Ban, Ishika Agarwal, Ziwei Wu, Yada Zhu, Kommy Weldemariam, Hanghang Tong, Jingrui He'
---

[Paper](https://arxiv.org/abs/2404.12522)
[Code](https://github.com/agarwalishika/NeurONAL)

We study both stream-based and pool-based active learning with neural network approximations. A recent line of works proposed bandit-based approaches that transformed active learning into a bandit problem, achieving both theoretical and empirical success. However, the performance and computational costs of these methods may be susceptible to the number of classes, denoted as K, due to this transformation. Therefore, this paper seeks to answer the question: "How can we mitigate the adverse impacts of K while retaining the advantages of principled exploration and provable performance guarantees in active learning?" To tackle this challenge, we propose two algorithms based on the newly designed exploitation and exploration neural networks for stream-based and pool-based active learning. Subsequently, we provide theoretical performance guarantees for both algorithms in a non-parametric setting, demonstrating a slower error-growth rate concerning K for the proposed approaches. We use extensive experiments to evaluate the proposed algorithms, which consistently outperform state-of-the-art baselines.