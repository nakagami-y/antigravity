---
name: fix-issue
description: Analyze and fix a GitHub issue end-to-end. Reads the issue, finds relevant code, implements a fix, tests it, and creates a PR.
version: "1.0.0"
---

# Fix Issue — GitHub Issue を解決する

GitHub Issue を読み、修正を実装し、PRを作成するまでを一気通貫で行う。

## トリガー

- `/fix-issue [issue番号 or URL]`
- "issue #123 を修正して"
- "このissueを直して"

## 入力

- **Issue**: 必須。Issue番号（`#123`）またはURL

## ワークフロー

### Step 1: Issue の把握

```bash
gh issue view [番号]
```

- Issue のタイトル・本文・ラベル・コメントを読む
- 再現手順があれば確認する
- **判断基準**: 「この Issue の "完了" とは何か？」を明確にする。曖昧なら質問する

### Step 2: 関連コードの特定

- Issue の内容からキーワードを抽出
- Grep / Glob で関連ファイルを検索
- エラーメッセージがあればそれで検索
- **判断基準**: 修正に必要な最小限のファイルセットを特定する

### Step 3: 修正の実装

- 最小限の変更で修正する（over-engineering しない）
- 既存のコードスタイル・パターンに従う
- **判断基準**: 「この変更で副作用はないか？」を確認

### Step 4: テスト

- 該当するテストを実行
- 新しいテストが必要な場合は追加
- lint / typecheck を実行
- **判断基準**: 「修正前に失敗し、修正後に成功する」テストがあるか

### Step 5: コミット & PR

- 変更内容を説明するコミットメッセージを作成
- ブランチを作成してプッシュ
- `gh pr create` でPRを作成
- PR本文に Issue 番号を参照（`Fixes #123`）

## セルフチェック

1. Issue の要件をすべて満たしているか？
2. テストが通っているか？
3. 不要な変更が混ざっていないか？
4. PR の説明で第三者が変更内容を理解できるか？
