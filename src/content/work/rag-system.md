---
title: Enterprise RAG System for Structured & Unstructured Intelligence
publishDate: 2026-03-01 00:00:00
img: /assets/work/rag-system.jpg
img_alt: Enterprise RAG pipeline architecture combining SQL and vector search
description: |
  A hybrid AI agent system merging natural language SQL queries over a 50K+ record
  inventory database with FAISS-powered semantic search across corporate policy
  documents — all through a single Streamlit dashboard.
tags:
  - RAG
  - LLM
  - LangChain
  - FAISS
  - Streamlit
---

## Overview

Built a production-grade hybrid intelligence system that lets non-technical users interact with both structured inventory data and unstructured corporate policy documents using plain natural language. The system intelligently routes each query to the right data source — SQL for analytical questions, RAG for policy lookups — and handles hybrid queries that need both.

**GitHub:** [saideepa05/Enterprise_inventory](https://github.com/saideepa05/Enterprise_inventory)

## What I Built

- **Hybrid query orchestration engine** — a smart routing layer built with LangChain LCEL that detects query intent and dispatches to either the SQL module, the RAG pipeline, or both simultaneously for hybrid queries
- **SQL intelligence module** — natural language interface over a 50,000+ record diamond inventory SQLite database, supporting complex analytical queries like *"What is the average price of Ideal cut diamonds?"*
- **Document intelligence (RAG pipeline)** — FAISS vector store with semantic search over corporate policy documents (grading policies, return procedures, approval workflows), enabling queries like *"What is the restocking fee for high-end returns?"*
- **ETL & data pipeline** — automated data ingestion from CSV, database initialization scripts, and document chunking/embedding pipeline from raw text to indexed vector store
- **Streamlit dashboard** — professional UI with glassmorphic design, unifying both data sources in a single responsive interface accessible to non-technical stakeholders

## Tech Stack

Python · LangChain (LCEL) · OpenAI API · FAISS · SQLite · Streamlit · Pandas · Embedding Models

## Impact

Unified two fundamentally different data sources — a relational inventory database and unstructured policy documents — behind a single natural language interface. Non-technical users can now run queries that previously required a developer or data analyst, including hybrid questions that cross both structured and unstructured data in a single response.
