# メモリの整理ルール（全会話に自動適用）

情報がゴチャゴチャにならないよう、何をどこに残すかを固定する。

## 保存先の判定フロー

```text
新情報
  ↓
1. 一時的な情報か？
   → Yes → 保存しない
  ↓ No
2. workspace 全体の運用ルールか？
   → Yes → GEMINI.md または .agents/rules/ を更新
  ↓ No
3. 共有知識か？
   → Yes → knowledge/ に整理
  ↓ No
4. Udemy 専用の知識や制作条件か？
   → Yes → projects/udemy/knowledge/ / contracts/ / samples/ / output/ の関連ファイルを更新
  ↓ No
5. 作業の計画 or 結果か？
   → Yes → AI 実行の plan / report は常に root memory_bank/ に保存
  ↓ No
6. 毎回使う手順か？
   → Yes → .agents/workflows/ または .agents/skills/ に整理
```

## 実行ゲート

- 人間がエージェントへ指示したら、作業開始前に root `memory_bank/plan/` を作る
- 作業が終わったら、root `memory_bank/report/` を作るまで完了扱いにしない
- これは `/plan` `/report` の手動トリガー待ちにせず、自動で実行する
- plan / report の保存先が不明なまま project 配下へ新しいログ置き場を増やさない

## 矛盾の検知

- ルール間の矛盾
- 共有知識と project 知識の責務混線
- 今回の指示と既存ファイルの不一致

矛盾に気づいたら、どこが食い違うかを具体的に示してから確認する。

## 衛生管理

- `GEMINI.md` が肥大化していないか
- `knowledge/` と `projects/udemy/knowledge/` の責務が混ざっていないか
- `memory_bank/plan/` に古い計画が放置されていないか
- `memory_bank/report/` に AI 実行診断ログが残っているか
- project 配下に plan / report の新規保存先を増やしていないか
- 新しい `projects/<project>/` が増えたのに root 側の plan / report 導線が落ちていないか
