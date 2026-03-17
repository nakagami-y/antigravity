# Code Review Workflow

## 目的

- 変更内容を correctness / security / maintainability の観点でレビューする

## 手順

1. レビュー指示に対する plan を root `memory_bank/plan/` に作る
2. changed files を読む
3. 意図と周辺文脈を確認する
4. 正しさ、例外系、境界条件を見る
5. セキュリティと秘密情報を確認する
6. 保守性と無駄な複雑さを確認する
7. root `memory_bank/report/` に report を作る

## 出力

- Summary
- Good
- Issues
- Suggestions
