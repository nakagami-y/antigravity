# GEMINI.md

Google AntiGravity 用の workspace 契約。

## このファイルの役割

- この `GEMINI.md` は workspace 全体の共通ルール
- あわせて、構造と参照先のリンク集として使う
- 個別業務の詳細ルールはここに肥大化させず、下位ディレクトリへ分ける

## Workspace Purpose

- この repo は `Content & Automation Lab` の共通 workspace
- root は共通ルールと導線だけを持ち、業務固有の実務は `projects/<project>/` 側で受ける
- `knowledge/` は参照用 knowledge 層であり、中身そのものを runtime 正本として編集運用する場ではない
- `projects/udemy/` は現時点の主要な実務ディレクトリのひとつ

## First Read Order

1. この `GEMINI.md`
2. `.agents/rules/01-*.md` から `.agents/rules/10-*.md`
3. `.agents/rules/04-memory-routing.md` と `.agents/rules/05-quality-check.md`
4. `knowledge/README.md`
5. 必要な `projects/<project>/README.md`
6. 必要時のみ `.agents/workflows/*.md` と `.agents/skills/*/SKILL.md`

## Workspace Contracts

- root 正本は `GEMINI.md`
- 共通ルールは `.agents/rules/01-*.md` から `.agents/rules/10-*.md`
- workflow は業務別の判断手順と実行導線を定義する
- skill は再利用する定型手順を定義する
- `knowledge/` は複数業務から参照する共通知識を置く
- `projects/<project>/` は業務別の契約、samples、output、benchmarks を受ける
- 旧来の Claude 系構成は使わない

## Working Rules

- 不明点は推測で埋めず、結論を変える前提だけ確認する
- 編集前に必ず対象ファイルを読む
- 数字・引用・実績・仕様は捏造しない
- 時間で変わる情報は取得日を添える
- 破壊的操作、外部公開、機密情報操作は事前確認する
- 人間がエージェントへ指示した作業は、開始前に root `memory_bank/plan/`、完了後に root `memory_bank/report/` を必ず残す
- ユーザーが `/plan` や `/report` を明示しなくても自動で実行する
- plan / report がないまま作業を進めたり終えたりしない

## Project Routing

- Udemy 投稿生成:
  - `.agents/workflows/udemy-post-create.md`
- それ以外の `projects/<project>/` 作業:
  - まず対象 `README.md` を読み、root `memory_bank/plan/` を切ってから進める
- 共通知識:
  - `knowledge/README.md`
- 実務出力:
  - `projects/<project>/`

## Output Routing

- AI 実行の plan / report:
  - `memory_bank/plan/YYYY-MM-DD_内容.md`
  - `memory_bank/report/YYYY-MM-DD_内容.md`
- テキスト成果物:
  - `projects/udemy/output/`
- バイナリ成果物:
  - `assets/images/`
  - `assets/exports/`
  - `assets/screenshots/`

## Never Do

- 旧来の Claude 系構成を再作成しない
- 共有知識を `projects/udemy/` に複製しない
- テキスト成果物を root `assets/` に混ぜない
- root 共通層へ業務固有ルールを肥大化させない
- AI 実行ログを project 配下へ分散させない
- 根拠なしの誇張、成果保証、一般論で埋めない
