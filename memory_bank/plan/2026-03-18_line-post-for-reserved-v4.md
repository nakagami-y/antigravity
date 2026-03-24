---
target_repo: gami-antigravity
task_type: "マーケティングテキスト作成"
planned_rules: []
planned_workflows: []
planned_skills: ["plan", "report"]
planned_knowledge: []
status: draft
report_required: true
---

# AI実行Plan: 予約者向けLINE告知文（AIに対する表現の修正）

## まずこれだけ見ればOK

- 依頼: 当日12時用の配信文に記載されていた「部下」「やらせる」といった、AIを下に見るような表現を修正してメッセージを作成し直す。
- ゴール: AIに対するリスペクトを持ち、AIを「優秀なパートナー・協働者」として迎え入れるような、前向きで現代的なトーンのLINE告知文を完成させる。
- 完了条件: 
  - AIを下に見る表現（部下、やらせる、指示して放置など）が排除されている
  - AIを「パートナー」として共に働くポジティブな文脈になっている
  - planとreportが指定ディレクトリに保存されている

## AIが今回見る予定のもの

- ルール: GEMINI.md, AGENTS.md
- workflow: 該当なし
- skill: plan, report
- knowledge: なし

## 実行方針

1. `260319-20_reserved-participants-reminder.md` の当日12時用のテキストを修正する。
2. 具体的には以下の箇所をリライトする：
   - 「指示して放置」→「信頼して任せる」
   - 「一つのコマンドに任せられる」→「AIに引き継げる」
   - 「頼れる専属の部下」→「共に働く頼もしいパートナー」
   - 「AIにやらせるフェーズ」→「AIと共に作業を完遂するフェーズ」
3. 修正テキストで既存のファイルを上書きし、本PlanとReport（v4版）を出力する。

## やること

1. `memory_bank/plan/2026-03-18_line-post-for-reserved-v4.md` の作成
2. `projects/unikoschool-launch/marketing/line-posts/wado-line/260319-20_reserved-participants-reminder.md` の上書き保存（全体リライト）
3. `memory_bank/report/2026-03-18_line-post-for-reserved-v4.md` の作成

## 保存先

- 成果物: `projects/unikoschool-launch/marketing/line-posts/wado-line/260319-20_reserved-participants-reminder.md` (Overwritten)
- plan: `memory_bank/plan/2026-03-18_line-post-for-reserved-v4.md`
- report: `memory_bank/report/2026-03-18_line-post-for-reserved-v4.md`

## リスク・前提

- 「作業が減る・楽になる」という本質的なベネフィットの魅力は落とさないように、表現だけをポジティブに調整する。
