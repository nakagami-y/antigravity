---
target_repo: gami-antigravity
task_type: "マーケティングテキスト作成"
used_rules: []
used_workflows: []
used_skills: ["plan", "report"]
used_knowledge: []
primary_issue_layer: instruction
outcome: success
friction_score: 1
rework_needed: false
linked_plan: "memory_bank/plan/2026-03-18_line-post-for-reserved-v3.md"
---

# AI実行レポート: 予約者向けLINE告知文（分割版）の作成

## まずこれだけ見ればOK

- 依頼: これまで1通にまとめていた予約者向けLINE告知文を、「セミナー内容を前日の20時」と「参加したらできるようになることを当日の12時」に分割して再構成する。
- 結果: 指定された構成に沿って「前日20時用（セミナー内容）」と「当日12時用（未来のベネフィット）」の2通に完全に分け、それぞれの文脈が自然に繋がるように調整・保存しました。
- 次回のコツ: 分岐や段階的な配信シナリオを組む場合は、今回のように「どのタイミングでどの情報を出すか」をご指定いただけると、非常に精度の高いメッセージが生成できます。

## AIが見たもの

### 主に参照したファイル

- 1つ前の依頼で作成した、スライド300枚などの要素が含まれる告知文のテキスト

### 使ったルール / workflow / skill

- ルール: GEMINI.md, AGENTS.md
- workflow: 該当なし
- skill: plan, report

## AIの判断

- **前日20時のメッセージ**: 翌日に控えたセミナーの「内容とボリューム」を先行公開し、参加の心理的なハードル（何をするのかわからない不安など）を取り除く構成にしました。
- **当日12時のメッセージ**: 前日の内容を引き継ぎ、「じゃあ結局何が変わるのか」という当事者意識を持たせるために「参加後の未来」に焦点を絞って記載しました。また、当日「今夜20時お会いできるのを〜」という期待感とホスピタリティ要素を踏襲しています。

## 出力結果

- 成果物: `projects/unikoschool-launch/marketing/line-posts/wado-line/260319-20_reserved-participants-reminder.md`
- 変更ファイル:
  - `memory_bank/plan/2026-03-18_line-post-for-reserved-v3.md` (新規)
  - `memory_bank/report/2026-03-18_line-post-for-reserved-v3.md` (新規)
  - `projects/unikoschool-launch/marketing/line-posts/wado-line/260319-20_reserved-participants-reminder.md` (新規として保存)
- QA / 確認結果: 2部構成となっており、指定された時間（前日20時、当日12時）での情報出し分けができていることを確認しました。

## 次回もっと良くするには

- 追加であると良い情報: 当日用のリンク（直前の案内URLやZoomリンクなど）があれば、それも差し込む枠を設けることができます。
- おすすめの依頼文: 「2日間に分けて、1日目は〇〇、2日目は〇〇というストーリーで文面を作成して」
- 再利用できる rule / workflow / skill 候補: `plan`, `report`

## 診断ログ

### blocking_factors

- 特になし

### root_cause

- 該当なし

### quality assessment

- instruction_quality: 明確（分割のタイミングと情報の内容が完全に指定されていた）
- rule_quality: PlanとReportのルール遵守
- workflow_quality: -
- knowledge_quality: 連続したタスクで過去の要望（スライド300枚など）を落とさず引き継げた

### suggested_fix

- なし
