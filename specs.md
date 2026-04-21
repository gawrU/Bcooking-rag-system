# Specs - Cooking RAG System

## 1. Chunking Strategy

採用語義切分（Semantic Chunking）

- 依照「食材 / 步驟」分段
- 保持料理流程完整性
- 避免語意斷裂

---

## 2. Performance Metrics

- Latency：< 2 秒
- Top-K Recall（Top-5）：≥ 85%

---

## 3. Evaluation

使用：
- RAGAS
- TruLens

### Evaluation Process

使用RAGAS評估系統輸出：

- Faithfulness：檢查答案是否來自檢索內容
- Relevance：檢查是否回答到問題
- Answer Completeness：檢查回答是否完整

TruLens用於追蹤模型輸出與檢索結果之間的關聯性，並分析檢索品質對生成結果的影響。
