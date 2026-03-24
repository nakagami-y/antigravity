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

# AI実行Plan: 予約者向けLINE告知文（期待値上げ）作成

## まずこれだけ見ればOK

- 依頼: 参加予約者に対し、セミナー参加の意欲を高めるために「セミナー内容」と「参加したらできるようになること」を分けて記載したLINE投稿文を作成する。
- ゴール: 参加予約者の当日の参加率や学習意欲を最大化するLINE文面の完成。
- 完了条件: 
  - メッセージが「セミナー内容」と「参加したらできるようになること」に分かれていること
  - 予約者向けの期待値を上げるトーンであること
  - planとreportが指定ディレクトリに保存されていること

## AIが今回見る予定のもの

- ルール: GEMINI.md, AGENTS.md
- workflow: 該当なし
- skill: plan, report
- knowledge: 過去の告知文にあったセミナー内容（Claude Codeの自動化、画像100枚一括生成、MCP連携など）

## 実行方針

1. これまで訴求していた「Claude CodeとClaudeの違い」「画像一括生成などの実践例」をもとに、セミナー内容を箇条書きで分かりやすく整理する。
2. その内容を学んだ結果「具体的に何ができるようになるのか（作業の放置、数時間の作業の数分化など）」をベネフィットとして提示する。
3. 文面、plan、reportの3つのファイルを出力する。

## やること

1. `memory_bank/plan/2026-03-18_line-post-for-reserved.md` の作成
2. `projects/unikoschool-launch/marketing/line-posts/wado-line/260318-19_reserved-participants-reminder.md` の作成
3. `memory_bank/report/2026-03-18_line-post-for-reserved.md` の作成

## 保存先

- 成果物: `projects/unikoschool-launch/marketing/line-posts/wado-line/260318-19_reserved-participants-reminder.md`
- plan: `memory_bank/plan/2026-03-18_line-post-for-reserved.md`
- report: `memory_bank/report/2026-03-18_line-post-for-reserved.md`

## リスク・前提

- 予約者向けのため、申し込みURLは不要（または控えめでOK）と判断する。
- 過去のテキストコンテキストを元に、セミナー内容を一部AI側で補間して魅力的に書き起こす。
