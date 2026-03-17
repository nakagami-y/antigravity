# Security Review Workflow

## 目的

- コードや設定の危険な点を、修正提案つきで洗い出す

## 観点

- 入力検証
- 認証 / 認可
- 秘密情報管理
- インジェクション
- 不要な公開

## 保存

- 人間から指示されたレビューは、開始前に root `memory_bank/plan/`、完了後に root `memory_bank/report/` を残す

## 出力

- Issue
- Risk
- Suggested Fix
