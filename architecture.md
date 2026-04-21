# Architecture

Raw Data（食譜 / 網站）
→ ETL（清洗、去重複）
→ Chunking（語義切分）
→ Embedding（向量化）
→ Vector DB（FAISS）

【Boundary：非結構化 → 向量】

→ Retrieval（Hybrid Search）
→ Reranking（Cross Encoder）

【Reranking位置】

→ LLM
→ Output
