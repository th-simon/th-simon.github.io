---
title: Multi-Armed Bandit Optimization
date: 2025-10-17
authors:
  - admin

summary: Want to run more efficient experiments? See how to implement adaptive randomization in sequential experimental setups.

tags: []
featured: false

image:
  caption: ''
  focal_point: Center
  preview_only: false
---

## What is a multi-armed bandit experiment?
Multi-armed bandit (MAB) optimization is a reinforcement learning approach that combines exploration and exploitation within a sequential experiment. In traditional experimental designs, researchers *explore* by testing all alternatives equally and evaluate outcomes only after the experiment has ended. In contrast, MAB optimization continuously learns from the data that arrives during the experiment and immediately *exploits* this information to improve allocation decisions. This means that MAB experiments not only generate knowledge but also earn on that knowledge *while still learning*.

> [!NOTE]
> The term multi-armed bandit comes from the metaphor of a gambler facing several slot machines (“one-armed bandits”) with unknown payout probabilities. The gambler must decide whether to keep playing the most rewarding machine (exploitation) or try others to learn about their potential (exploration). In experimental research, this trade-off mirrors the idea of allocating more observations to better-performing treatments while still learning about the rest.
