---
name: setup-wizard
description: "AntiGravity workspace の初期セットアップを対話で整える。"
version: 2.0.0
---

# Setup Wizard

AntiGravity workspace を最小構成で整えるための skill。

## ゴール

- `GEMINI.md` のプロジェクト概要を埋める
- `.agents/rules/02-style.md` を好みの口調に整える
- 最初の skill を `.agents/skills/` に追加する
- `memory_bank/` の使い方を確認する

## レベル

1. プロジェクトの自己紹介
   - `GEMINI.md` を更新
2. AI の口調決め
   - `.agents/rules/02-style.md` を更新
3. 最初の skill 作成
   - `.agents/skills/{skill_name}/SKILL.md` を作る
4. ログ導線の確認
   - `memory_bank/plan/` と `memory_bank/report/` の役割を説明
5. 仕上げ確認
   - `knowledge/` と `projects/` の読み分けを確認

## 進め方

- 1 レベルごとに止まり、次へ進むか確認する
- 必要な質問だけを 1 問ずつ聞く
- 生成したファイルと保存先を毎回明示する

## 完了条件

- `GEMINI.md` に目的と対象が入っている
- `.agents/rules/02-style.md` が workspace の話し方を表している
- `.agents/skills/` に少なくとも 1 つ skill がある
- `memory_bank/` の使い分けを説明できる
