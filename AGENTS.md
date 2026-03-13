# AGENTS.md

この repo は Google AntiGravity 専用の workspace です。

## 役割マップ

- `GEMINI.md`
  - workspace 全体の基本契約。最初に読む
- `.agents/rules/`
  - `01-*.md` から `10-*.md` が共通ルール
  - `20-udemy-*` は Udemy workflow 専用の補助ルール
- `.agents/workflows/`
  - 判断や作業の進め方を定義した workflow
- `.agents/skills/`
  - 再利用する skill 群
- `knowledge/`
  - ブランド・法人・意思決定 OS の参照 knowledge
- `projects/udemy/`
  - Udemy講座の投稿を作るための実務ディレクトリ
- `memory_bank/`
  - AI 実行の plan / report をまとめる root ログ
- `assets/`
  - 画像・PPTX・スクリーンショットなどのバイナリ成果物

## 重要ルール

- 旧来の Claude 系構成はこの repo では使わない
- root は共通層、業務固有の実務は `projects/<project>/` 側で受ける
- Udemy 投稿は `projects/udemy/README.md` と `.agents/workflows/udemy-post-create.md` から入る
- AI 作業で保存対象がある場合は root `memory_bank/plan/` と `memory_bank/report/` に記録する
- AI 作業後は root report の `まずこれだけ見ればOK` と `AIが見たもの` を確認する

## 最初の確認順

1. `GEMINI.md`
2. `.agents/rules/01-*.md` から `.agents/rules/10-*.md`
3. `knowledge/README.md`
4. `projects/udemy/README.md`
