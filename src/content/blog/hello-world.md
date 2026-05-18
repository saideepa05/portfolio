---
title: Hello World — Welcome to My Blog
publishDate: 2026-05-06 00:00:00
description: |
  A first post to kick off my blog — what I'll be writing about, why I'm starting now,
  and what's on my mind at the intersection of AI engineering and neuromorphic research.
tags:
  - Meta
  - AI
  - Neuromorphic
---

## Hello, World

If you're reading this, the blog is working. That's already a win.

I've been meaning to write publicly for a while. My work sits at an unusual intersection — I spend my days building production AI systems (RAG pipelines, multi-agent orchestrators, LLM monitoring stacks) while also running thesis research on spiking neural networks and neuromorphic computing. Those two worlds don't always talk to each other. This blog is my attempt to make them.

## What I'll Write About

A few themes I keep returning to:

**The gap between research and production.** Most ML research optimizes for benchmark performance. Most production systems optimize for reliability, debuggability, and the ability to hand off to someone who wasn't in the room when it was built. I find the tension between those two goals genuinely interesting.

**Energy-efficient AI.** My thesis asks whether we can replace the dense matrix multiplications inside deep RL agents with sparse, biologically inspired spiking operations — and get 80% energy savings without sacrificing much performance. The answer, it turns out, is: sometimes yes, and the "sometimes" is the whole research question. As models get larger, this matters more, not less.

**Things I had to figure out the hard way.** Retrieval failures that only show up at scale. Agent handoff bugs that look like LLM hallucinations but aren't. Chunking strategies that work in demos and fall apart on real documents. I'll write these up as I encounter them.

