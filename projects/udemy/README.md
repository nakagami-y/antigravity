# Udemy Workspace

Udemy講座の投稿を作るための実務ディレクトリ。

## 目的

- 5C の考え方で投稿生成を再現可能にする
- ルール、出力契約、サンプル、講座台本を分離する
- 投稿品質を benchmark で比較できるようにする

## このディレクトリの前提

- ここは「Udemy講座そのものの教材置き場」ではなく、「Udemy講座を題材にした投稿制作の実務層」
- `knowledge/` は参照用の素材層
- 実際に投稿を作るときの正本は、このディレクトリ配下の `contracts/`, `samples/`, `output/`, `benchmarks/` と、workflow が読む補助 rules
- AI 実行の plan / report はこのディレクトリではなく、root `memory_bank/` に統一する
- 人間から Udemy の実作業を指示したら、必ず開始前に plan、完了後に report を root `memory_bank/` に残す

## 参照順

1. `contracts/output.md`
2. `../../.agents/workflows/udemy-post-create.md`
3. `../../.agents/rules/20-udemy-voice.md`
4. `../../.agents/rules/21-udemy-compliance.md`
5. `samples/winning-patterns.md`
6. 必要な `knowledge/*.md`

`../../.agents/rules/20-udemy-voice.md` と `../../.agents/rules/21-udemy-compliance.md` は、Udemy 投稿 workflow が読む補助 rules。

## このディレクトリで編集するもの

- `contracts/`
- `samples/`
- `output/`
- `benchmarks/`

## 基本編集しないもの

- `knowledge/`

`knowledge/` は参照素材であり、通常は改稿対象にしない。本文刷新が必要な場合だけ別タスクで扱う。

## 保存先

- テキスト成果物:
  - `output/`
- AI 実行の plan / report:
  - `../../memory_bank/plan/`
  - `../../memory_bank/report/`
- 比較素材:
  - `benchmarks/`
