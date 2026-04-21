# Architecture - Cooking RAG System

## System Overview
本系統為料理輔助RAG系統，整合食譜、料理技巧與營養資料，提供具依據的料理建議。

---

## Pipeline

Raw Data（食譜 / 料理網站 / 營養資料）
→ ETL（清洗、去重複、格式統一）
→ Chunking（語義切分）
→ Embedding（BGE-M3）
→ Vector Database（FAISS）

【🔴 Boundary：非結構化 → 向量化】

Vector Database 採用 FAISS 單節點架構，向量儲存在本地記憶體中，以支援高速相似度搜尋。

→ Retrieval（Hybrid Search：Keyword + Vector）
→ Reranking（Cross Encoder）

【🔵 Reranking介入點：Retrieval之後、LLM之前】

→ LLM（生成答案）
→ Output（料理建議）

---

## Explainability

本系統透過提供檢索來源，使生成答案具備可追溯性（Explainability），提升使用者信任度。
