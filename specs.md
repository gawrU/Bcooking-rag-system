# Specs

## Chunking
語義切分（依食材與步驟）

## Performance
- Latency < 2s
- Top-5 ≥ 85%

## Evaluation
- RAGAS
- TruLens

Metrics：
- Faithfulness
- Relevance
- Completeness

Evaluation Process:

使用RAGAS評估系統輸出：
- Faithfulness：檢查答案是否來自檢索內容
- Relevance：檢查是否回答到問題
- Answer Completeness：檢查回答是否完整

TruLens用於追蹤模型輸出與檢索結果的關聯性。
