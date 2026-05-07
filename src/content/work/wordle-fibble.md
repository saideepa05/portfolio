---
title: RL- and LLM-Based AI Solvers for Wordle & Fibble
publishDate: 2024-05-01 00:00:00
img: /assets/work/wordle-fibble.jpg
img_alt: Reinforcement learning agents playing Wordle and Fibble word-guessing games
description: |
  Trained deep RL agents to master Wordle and its adversarial variant Fibble — where
  the game deliberately lies — then benchmarked them against GPT-based solvers.
  Published as co-authored research at IEEE Conference on Games 2025.
tags:
  - Reinforcement Learning
  - LLM
  - OpenAI Gym
  - Python
---

## Overview

Trained deep reinforcement learning agents to master word-guessing games with increasing deception complexity. Built custom environments for standard Wordle and the adversarial "Fibble" variant, where the game injects 1–5 intentional lies per round of feedback, directly testing whether an agent can infer truth from corrupted signals. Achieved 99.8% win rate on clean Wordle, with performance degrading sharply as lie count increased — findings that became the empirical core of a co-authored paper published at the IEEE Conference on Games 2025.

**GitHub:** [saideepa05/wordle-and-fibble-using-RL](https://github.com/saideepa05/wordle-and-fibble-using-RL)

## What I Built

- **Custom game environments** — parametric Wordle and Fibble environments with configurable lie injection (1–5 deceptions per round), built to mirror the OpenAI Gym interface
- **Q-learning agent** — implemented with experience replay (standard and prioritized buffers), trained across 9 million episodes with epsilon-decay exploration
- **Multi-action representation strategies** — experimented with letter-level selections, full-word actions, and hybrid approaches to find optimal state-action encodings
- **PPO baseline** — implemented Proximal Policy Optimization within an OpenAI Gym environment as an additional RL benchmark
- **LLM comparative analysis** — benchmarked GPT variants against RL agents, identifying performance gaps in logical reasoning under noisy/contradictory feedback
- **Experiment tracking** — integrated Weights & Biases dashboards for real-time monitoring of win rates, loss curves, and degradation across Fibble difficulty levels

## Tech Stack

Python · Q-learning · PPO · OpenAI Gym · Weights & Biases · NumPy · scikit-learn · GPT API

## Results

Misinformation complexity exponentially eroded agent performance: standard Wordle reached **99.8% win rate**, Fibble-1 achieved **56.82%**, and Fibble-2 through Fibble-5 collapsed to under 1% — with Fibble-5 reaching only **0.29%**. These results quantify how RL agents struggle to reconcile contradictory feedback and provided the empirical foundation for the published IEEE paper.
