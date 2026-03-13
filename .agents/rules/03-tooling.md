# ツール運用ルール（全会話に自動適用）

AntiGravity 上での作業を安定させるための最低限ルール。

## 予約席の優先順位

- workspace 契約は `GEMINI.md`
- 常時ルールは `.agents/rules/`
- 手順は `.agents/workflows/`
- 再利用 skill は `.agents/skills/`

## 作業の基本

- 読む前に書かない
- 大きい一括置換の後は必ず `rg` で残件確認する
- 破壊的変更前は `git status` で差分を確認する
- 時間で変わる情報は取得日を添える

## 失敗しやすいポイント

- 認証付き Web 情報は取得できないことがある
  - 必要ならユーザーに本文共有を依頼する
- 大量置換は意図しない文言まで変わる
  - 置換後に `git diff` と `rg` を回す
- skill / workflow の正本パスを混ぜると認識がぶれる
  - `.agents/skills/` と `.agents/workflows/` を混同しない

## 出力の置き場

- テキスト:
  - `projects/udemy/output/`
- バイナリ:
  - `assets/images/`
  - `assets/exports/`
  - `assets/screenshots/`
