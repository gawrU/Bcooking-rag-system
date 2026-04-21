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

Vector Database 採用 FAISS 單節點架構，所有向量儲存在本地記憶體中，以支援快速相似度搜尋。
本系統透過提供檢索來源，使生成答案具備可追溯性（Explainability）。
