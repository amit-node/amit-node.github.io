---
title: Raptor RAG theory
date: 2025-09-05
tags:
  - AI_DL
---
Source : [Building long context RAG with RAPTOR from scratch](https://youtu.be/jbGchdTL7d0)
YouTube video  
[Raptor RAG paper](https://arxiv.org/pdf/2401.18059)


**Long Context LLMs :** Where you can send a lots of tokens at once. Good thing, nothing to do, send your documents to LLM, ask questions and get answers automatically.

But, there are some problems:
1. P50, P99 latencies
2. Cost
3. What if document is bigger than than the context window.

Solution idea : Embed each document and build a document tree (RAPTOR)

**RAPTOR :** Recursive Abstractive Processing for Tree Organized Retrieval

