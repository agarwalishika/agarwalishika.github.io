---
title: "Generative Transformers for Diverse text Generation"
collection: projects
permalink: /projects/diverse_text_gen
excerpt: ''
date: 2023-05-07
paperurl: 'http://agarwalishika.github.io/files/diverse_text_gen.pdf'
authors: 'Ishika Agarwal, Priyanka Kargupta, Bowen Jin, Akul Joshi'
---

[Paper](http://agarwalishika.github.io/files/diverse_text_gen.pdf)
[Code](https://github.com/agarwalishika/SeqDiffuSeq)

Diverse text generation is an important and challenging task. Existing methods mainly adopt a discriminative model, with the underlying assumption that the input text-to-output text projection is a one-one mapping. However, this is not true in the real world, since given one single input text, there can be multiple ground truth output text candidates. For example, in the commonsense generation, given a list of knowledge entities, there should be more than one way to use them to come up with a sentence. This motivates us to capture the underlying text semantics distribution with generative models (e.g., VAE and diffusion models). On the other hand, Transformer architecture has been demonstrated to be effective in text semantics capturing. Then the problem comes to how to effectively combine the Transformer architecture with the generative models. Our project aims to combine the best of both worlds by introducing VAE & Diffusion model into transformers. Specifically, we want to apply them to two downstream tasks: common sense generation and question generation. We include results, and some future work to further this project.