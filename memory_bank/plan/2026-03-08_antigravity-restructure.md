# Plan: antigravity 完全再整形

- **日付**: 2026-03-08
- **ステータス**: done

---

## ゴール

この repo を AntiGravity 専用構成へ再整形し、Udemy 投稿生成の知識・workflow・成果物導線を分離する。

## 背景

旧来の Claude 系構成と Udemy 固有の運用ルールが混在しており、予約席、知識の責務、成果物の保存先が曖昧だった。

## やること

1. `GEMINI.md` と `.agents/` を正本へ移す
2. `projects/udemy/` を業務ワークスペースとして再編する
3. benchmark と log 導線を追加する

## やらないこと（スコープ外）

- 講座台本の install / auth 記述を全面的に最新仕様へ書き直すこと
- 実際の AntiGravity 実行結果を benchmark に流し込むこと

## 完了条件

- [x] root に `GEMINI.md` と `.agents/{rules,workflows,skills}` がある
- [x] `projects/udemy/` が知識・rules・contracts・output・benchmarks を持つ
- [x] 旧パス参照が repo 内から除去されている

## リスク・懸念

- 講座素材の一部には legacy な install / auth 記述が残るため、配布前の事実確認が必要
