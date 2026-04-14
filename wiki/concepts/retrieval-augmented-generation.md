---
title: "Retrieval-Augmented Generation"
type: concept
tags: [llm, rag, information-retrieval, methodology]
created: 2026-04-14
updated: 2026-04-14
sources: [karpathy-llm-wiki-pattern]
---

# Retrieval-Augmented Generation

A technique in which an LLM retrieves relevant chunks from a document collection at query time and uses them to generate an answer. The documents themselves remain unmodified; the LLM re-derives knowledge on every question.

## Overview

RAG is the dominant pattern for "chat with your documents" applications (NotebookLM, ChatGPT file uploads, most enterprise search tools). It works by embedding documents into a vector store, retrieving the top-k most relevant chunks for each query, and including those chunks in the LLM's context window when generating an answer.

The [[LLM-Maintained Wiki]] pattern contrasts with RAG: instead of retrieving and re-deriving, the LLM *compiles* knowledge into a persistent structure that accumulates over time.

## Key Properties / Characteristics

- **Stateless:** No knowledge is built between queries. Each query starts fresh.
- **Scales to large document collections** via vector indexing
- **Limited synthesis:** Subtle questions requiring synthesis of many documents are re-computed from scratch each time
- **No contradiction management:** The LLM doesn't know if Document A and Document B disagree unless both happen to be retrieved together

## How It Works

1. Documents are chunked and embedded into a vector store
2. User query is embedded and used to retrieve top-k similar chunks
3. Retrieved chunks are injected into the LLM's context
4. LLM generates an answer citing those chunks

## Variants / Subtypes

- **Naive RAG** — simple vector similarity retrieval
- **Hybrid RAG** — BM25 + vector search (e.g. [[qmd]])
- **Agentic RAG** — LLM decides which queries to run, iterative retrieval
- **Graph RAG** — uses knowledge graphs for structured retrieval

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/karpathy-llm-wiki-pattern]] | RAG involves no accumulation; knowledge is re-derived on every question | high |

## Contradictions & Open Questions

- At what scale does [[LLM-Maintained Wiki]] break down and RAG become preferable? Very large corpora (thousands of documents) may require RAG's indexing infrastructure. [low confidence]

## See Also

- [[LLM-Maintained Wiki]] — the contrasting, compounding alternative
- [[Knowledge Compounding]] — the property RAG lacks
- [[qmd]] — a hybrid search tool that can enhance RAG
