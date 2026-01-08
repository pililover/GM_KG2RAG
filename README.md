# Graph Mining Knowledge Graph to Retrieval-Augmented Generation

## Overview

This repository contains my implementation and experimental analysis of the KG2RAG framework, based on the paper "Knowledge Graph-Guided Retrieval Augmented Generation" (Zhu et al., 2025).

While the core architecture follows the original paper, this implementation introduces specific modifications and optimizations adapted for available computational resources and enhanced text processing. The project demonstrates how Knowledge Graphs (KGs) can improve RAG performance by capturing structured relationships between text chunks, thereby reducing hallucinations in LLMs.

## Key Features & Modifications

Unlike the original implementation which utilized Llama-3 on high-end infrastructure, this repo adapts the framework for efficient execution while maintaining robust performance.

| Component	| Original Paper	| My Implementation |
|-----------|-----------------|-------------------|
| Document Chunking	| Standard Length-based	| Context-Aware Recursive Splitter (LangChain) |
| KG Construction	| Llama-3	| Gemini-2.0-Flash |
| Generation LLM	| Llama-3	| Gemma-7B-IT |
| Embedding Model	| mxbai-embed-large	| nomic-embed-text-v1.5 |
| Reranker |	bge-reranker-large	| bge-reranker-v2-m3 |


## References

Original Paper: Knowledge Graph-Guided Retrieval Augmented Generation (Zhu et al., 2025).
