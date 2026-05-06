---
title: LLM Pipeline Monitoring and Evaluation System
publishDate: 2026-02-01 00:00:00
img: /assets/work/llm-monitoring.jpg
img_alt: LLM monitoring dashboard showing latency and quality metrics
description: |
  A production-grade RAG support agent for Amazon Subscribe guidelines — wrapped
  with a full observability stack: real-time latency tracking, automated groundedness
  evaluation, human feedback logging, and an offline compliance benchmark.
tags:
  - MLOps
  - LLM
  - RAG
  - LangChain
  - Streamlit
---

## Overview

Built a complete LLM monitoring and evaluation system around an Amazon Subscribe support agent. The agent answers questions about product listing, returns, payments, tax, and customer service guidelines using a RAG pipeline — but the real engineering is the observability layer wrapped around it: every inference is logged, measured, scored, and surfaced in a live dashboard.

The system separates the LLM into measurable stages (retrieval vs. generation), scores each response for groundedness against its retrieved context, and provides a repeatable offline benchmark to validate compliance against known good answers.

## What I Built

- **RAG support pipeline** (`pipeline.py`) — LangChain LCEL chain over a FAISS vector store indexing 5 Amazon guideline documents (product listing, returns, payments, taxes, customer service), chunked with source traceability. Top-3 retrieval feeding a GPT model with strict grounding instructions
- **Real-time monitoring dashboard** (`app.py`) — Streamlit interface with three views:
  - **Dashboard** — live KPIs (support latency, success rate, guideline accuracy score, total queries), latency distribution histogram, query status pie chart, and an expandable audit trail with per-request trace logs
  - **Live Support Agent** — interactive query interface with example questions and custom input
  - **Guideline Benchmark** — one-click offline evaluation against the full validation set
- **Automated evaluator** (`evaluator.py`) — OpenAI embedding-based cosine similarity scoring for two dimensions: *response similarity* to expected answers (pass threshold: ≥ 0.85) and *groundedness* (response vs. retrieved context), catching hallucinations not grounded in the source documents
- **Structured audit logger** (`logger.py`) — JSON-based persistent log capturing every request: `request_id`, `timestamp`, `query`, `retrieved context`, `response`, `model`, `retrieval_latency`, `generation_latency`, `total_latency`, `status`, and human `feedback`
- **Metrics manager** (`metrics.py`) — computes performance metrics (avg / P95 / max latency, retrieval vs. generation breakdown), reliability metrics (success rate, failure count), and quality metrics (aggregated human feedback scores)
- **Offline benchmark runner** (`run_eval.py`) — batch evaluation pipeline against a CSV validation set, logging similarity and groundedness scores for every guideline question

## Tech Stack

Python · LangChain (LCEL) · OpenAI API (GPT + Embeddings) · FAISS · Streamlit · Plotly · scikit-learn · Pandas · JSON Logging

## Why This Matters

Most LLM failures aren't the model hallucinating out of nowhere — they're silent: retrieved context that doesn't match the question, responses that sound confident but aren't grounded in the source, or latency regressions that only show up under load. This system makes all of that visible. Splitting latency into retrieval and generation stages pinpoints where slowdowns happen. Groundedness scoring catches responses that drift from their source documents. The offline benchmark gives a repeatable compliance test you can run any time the knowledge base or model changes — so you know before users do.
