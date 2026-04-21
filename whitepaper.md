# Whitepaper

## Challenges
- 食材名稱不同（番茄/西紅柿）
- 模糊描述（少許）
- 步驟順序重要

## Hallucination
- 僅根據檢索回答
- 使用Reranking

## Cold Start
- 定期更新資料

## Ontology
- 建立食材詞庫

料理知識具有高度語意依賴與上下文關聯，將其轉換為向量表示時需保留步驟順序與食材關係，這對embedding模型是一大挑戰。
