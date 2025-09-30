---
title: Raptor RAG theory
date: 2025-09-05
tags:
  - AI_DL
draft: "True"
---
**Source** : 
1. [Building long context RAG with RAPTOR from scratch](https://youtu.be/jbGchdTL7d0)  YouTube video  
2. [Raptor RAG paper](https://arxiv.org/pdf/2401.18059)


**Long Context LLMs :**  
Where you can send a lots of tokens at once. Good thing, nothing to do, send your documents to LLM, ask questions and get answers automatically.

But, there are some problems:
1. P50, P99 latencies
2. Cost
3. What if document is bigger than than the context window.

Solution idea : Embed each document and build a document tree (RAPTOR)

**RAPTOR :** Recursive Abstractive Processing for Tree Organized Retrieval

**Intuition :**
1. Documents of any size
2. Chunks (token counts)
3. embed them
4. cluster them, grouped together like documents
5. summarize those clusters
6. more higher level of clustering, more abstract
7. do clustering recursively till either we have only one cluster remain or we set a limit on the recurring clusters.

> In tree structure, documents are leaf. It can be chunks or full documents.  
> then come middle level summaries, then high level summaries  
> then at root, highest level summary (mostly only one summary)  

All documents, summaries of all levels and root summary got embedded and stored in Vector database. Indexed and ready to retrieve.  

GMM : Gaussian Mixture Model  
To model the distribution of data points across different clusters. You don't need to give number of clusters. they find optimally number of clusters by evaluating the model's Bayesian Information Criterion (BIC).

UMAP : Uniform Manifold Approximation and Projection  
Kind of dimensionality reduction approach to improve the clustering process.  

Local and Global clustering :
it tries to analysing the data at two different scales : local and global.  
looking at patterns in smaller group and then full dataset. and try to improve. How to group these documents together.  
fine grain and broader patterns.  