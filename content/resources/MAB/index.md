---
title: Multi-Armed Bandits
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
A multi-armed bandit (MAB) experiment is a reinforcement learning approach that combines exploration and exploitation within a sequential setup. In traditional experimental designs, researchers *explore* by testing all alternatives equally and evaluate outcomes only after the experiment has ended. In contrast, MAB experiments continuously learn from the data that arrives during the trial and immediately *exploit* this information to improve allocation decisions. This means that such experiments not only generate knowledge but also earn on that knowledge *while still running*.

> [!NOTE]
> The term *multi-armed bandit* originates from the metaphor of a gambler facing several slot machines (“one-armed bandits”) with unknown payout probabilities. The gambler must decide whether to keep playing the supposedly most rewarding machine (exploitation) or try others to learn about their reward potential (exploration). In experimental research, this trade-off mirrors the idea of allocating more observations to better-performing treatments while still learning about the rest.

## Why are MAB experiments useful?
MAB experiments are particularly useful in settings with strong output orientation. This is clearly the case in medical research, where they allow patients to benefit from emerging evidence on effective treatments while the study is still ongoing. Similar logic applies to field experiments with firms. Businesses often evaluate experiments by the additional output they generate rather than by their statistical power, which is what we as researchers typically care about. By balancing these two objectives, MAB experiments could help encourage more firms to engage in field experiments in the future.

## Putting the MAB approach into practice
Together with Johannes Gaul, Davud Rostam-Afschar, and Florian Keusch, I applied a multi-armed bandit approach in a large-scale business survey experiment. We aimed to identify how to phrase an invitation message targeted at business decision-makers so that their likelihood of starting the survey would be maximized, which is particularly relevant given the typically low response rates in business surveys. Over a 15-week period, 176,000 firms received one of 32 invitation message versions. Instead of implementing a fixed and balanced randomization scheme, we continuously updated the probability of sending each message version based on its observed starting rate, using a Bayesian decision rule known as randomized probability matching. This adaptive approach made it possible to learn which messages worked best while the experiment was still running and increased the number of survey starts by 6.66 percent compared to a traditional fixed design.

## Learn more

For details, see our paper:  
👉 [**Invitation Messages for Business Surveys: A Multi-Armed Bandit Experiment**](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5053083)

The [**replication package**](https://search.gesis.org/research_data/SDN-10.7802-2836) includes the code to implement *randomized probability matching* and reproduce all results.

For the original introduction of *randomized probability matching*, see:  
Scott, S. L. (2010). *A modern Bayesian look at the multi-armed bandit.*  
*Applied Stochastic Models in Business and Industry, 26*(6), 639–658.
