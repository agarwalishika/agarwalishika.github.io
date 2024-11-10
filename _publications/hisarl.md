---
title: "HiSaRL: A Hierarchical Framework for Safe Reinforcement Learning"
collection: publications
permalink: /publications/hisarl
excerpt: ''
date: 2021-11-01
venue: 'SafeAI @ AAAI'
paperurl: 'https://ceur-ws.org/Vol-3087/paper_17.pdf'
authors: 'Zikang Xiong, Ishika Agarwal, Suresh Jagannathan'
---

[Paper](https://ceur-ws.org/Vol-3087/paper_17.pdf)
[Code](https://github.com/agarwalishika/two-d-nav-gym)

We propose a two-level hierarchical framework for safe reinforcement learning in a complex environment. The high-level part is an adaptive planner, which aims at learning and generating safe and efficient paths for tasks with imperfect map information. The lower-level part contains a learning-based controller and its corresponding neural Lyapunov function, which characterizes the controller’s stability property. This learned neural Lyapunov function serves two purposes. First, it will be part of the high-level heuristic for our planning algorithm. Second, it acts as a part of a runtime shield to guard the safety of the whole system. We use a robot navigation example to demonstrate that our framework can operate efficiently and safely in complex environments, even under adversarial attacks.