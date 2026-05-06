---
title: Deep Spiking Q-Networks for Turn-Based Game Environments — Tic-Tac-Toe & Connect 4
publishDate: 2026-03-15 00:00:00
img: /assets/work/dsqn.jpg
img_alt: Deep Spiking Q-Network architecture for turn-based game environments
description: |
  MS thesis research systematically evaluating 6 spike-encoding strategies inside
  Deep Q-Network agents — achieving up to 82.7% energy savings while maintaining
  competitive win rates in Tic-Tac-Toe and Connect 4.
tags:
  - Neuromorphic
  - Spiking Neural Networks
  - Reinforcement Learning
  - PyTorch
  - Research
---

## Overview

My MS thesis at Ohio University, presented as a poster at the **NICE Neuromorphic Computing Conference 2026** (Atlanta, GA) and submitted for publication to *IOP Neuromorphic Computing and Engineering*.

The core research question: can we replace the standard deep neural networks inside Q-learning agents with biologically inspired spiking neural networks — and if so, which spike-encoding strategy delivers the best balance of game performance and energy efficiency?

**GitHub:** [saideepa05/snn_encoding_methods_dsqn](https://github.com/saideepa05/snn_encoding_methods_dsqn)

## What I Built

- **Full DSQN framework** implementing six spike-encoding strategies — Population Coding, Count Rate, Time-to-First-Spike (TTFS), Rate of Change (ROC), Sparse Distributed Representation (SDR), and Burst Coding — each as a drop-in replacement for the standard DQN value network
- **Two game environments** — Tic-Tac-Toe and Connect 4 — with agents trained and evaluated against Random and Minimax baselines across 5 random seeds for statistical robustness
- **Energy measurement harness** tracking total synaptic operations (MAC vs. AC) and spike sparsity per encoding method
- **SpiNNaker neuromorphic implementation** using RSTDP for hardware-level validation alongside the software benchmarks
- **Benchmarking pipeline** comparing DSQN variants vs. conventional DQN across performance and energy dimensions

## Key Results

### Tic-Tac-Toe
| Encoding | Win+Draw Rate | Energy Savings | Sparsity |
|---|---|---|---|
| **SDR** | **100%** | — | — |
| **TTFS** | 99.4% | **82.7%** | **88.41%** |
| Population | competitive | — | — |

### Connect 4
| Encoding | Win+Draw Rate | Energy Savings | Sparsity |
|---|---|---|---|
| **Population** | **92.80%** | — | — |
| **TTFS** | competitive | **80.5%** | **70.44%** |
| ROC | 91.8% | — | — |

**Key finding:** TTFS encoding consistently delivered the optimal trade-off between game performance and energy consumption across both environments — making it the most suitable encoding for resource-constrained neuromorphic deployments. All six encoding methods maintained competitive win rates against baselines, validating that SNNs can match DQN performance while delivering substantial energy benefits.

## Tech Stack

Python · PyTorch · snnTorch · Reinforcement Learning (DQN/DSQN) · Surrogate Gradient Learning · SpiNNaker · Jupyter Notebooks · Neuromorphic Computing

## Publication

*Deep Spiking Q-Networks for Turn-Based Game Environments: Encoding Choices and Energy Trade-offs* — IOP Neuromorphic Computing and Engineering (Under Review, 2026)
