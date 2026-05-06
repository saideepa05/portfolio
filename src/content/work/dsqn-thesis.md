---
title: Deep Spiking Q-Networks for Strategic Game Environments
publishDate: 2026-03-15 00:00:00
img: /assets/stock-4.jpg
img_alt: Spiking neural network diagram with LIF neurons
description: |
  MS thesis research implementing biologically inspired spiking neural
  networks as drop-in replacements for traditional DQNs — achieving up to
  80% energy savings while matching strategic game performance.
tags:
  - Neuromorphic
  - Spiking Neural Networks
  - Reinforcement Learning
  - PyTorch
  - Research
---

## Overview

My MS thesis at Ohio University, presented as a poster at the **NICE Neuromorphic Computing Conference 2026** (Atlanta, GA) and submitted for publication to *IOP Neuromorphic Computing and Engineering*.

The core question: can we replace the standard deep neural networks inside Q-learning agents with biologically inspired spiking neural networks — and if so, what do we gain and what do we lose?

## Key Results

- **Up to 80% energy savings** over traditional DQNs by replacing dense MAC operations with sparse Accumulate (AC) operations
- **Matched strategic performance** against Random and Minimax baselines on Tic-Tac-Toe and Connect 4
- **Evaluated 6 spike-encoding methods** to find the best balance of performance and energy efficiency
- **Solved non-differentiability** using Surrogate Gradient Learning (Fast Sigmoid approximation) for end-to-end PyTorch training

## What I Built

- Full DSQN implementation using Leaky Integrate-and-Fire (LIF) neurons in snnTorch + PyTorch
- Benchmarking harness comparing DSQN vs. conventional DQN and rule-based agents across Tic-Tac-Toe and Connect 4
- Systematic analysis of spike-encoding density vs. energy efficiency

## Tech Stack

Python · PyTorch · snnTorch · Gymnasium · Reinforcement Learning · Surrogate Gradient Learning · Neuromorphic Computing

## Publication

*Deep Spiking Q-Networks for Turn-Based Game Environments: Encoding Choices and Energy Trade-offs* — IOP Neuromorphic Computing and Engineering (Under Review, 2026)
