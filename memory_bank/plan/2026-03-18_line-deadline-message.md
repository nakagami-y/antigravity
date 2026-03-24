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

# AI実行Plan: LINE告知文（3/18 締切メッセージ）作成

## まずこれだけ見ればOK

- 依頼: 参加予約していない人向けに、本日23:59〆切のメッセージを8時と20時に送る用を作成する
- ゴール: 3/18 23:59 締切に向けたLINE配信文（8時・20時）の完成
- 完了条件: 
  - 8時配信用と20時配信用の2パターンのメッセージが作成されていること
  - 予約URLが記載されていること
  - planとreportが指定ディレクトリに保存されていること

## AIが今回見る予定のもの

- ルール: GEMINI.md, AGENTS.md
- workflow: 該当なし
- skill: plan, report
- knowledge: プロジェクト内の過去の配信文 (260317-18_live-talk-and-tokuten.md)

## 実行方針

1. 過去の配信文からトーン＆マナーと遷移先URL（セミナー予約URL）を把握する
2. 8時用（朝のプレッシャー）・20時用（最後の念押し）の文面を作成する
3. planとreportを出力する

## やること

1. `memory_bank/plan/2026-03-18_line-deadline-message.md` の作成
2. `projects/unikoschool-launch/marketing/line-posts/wado-line/260318_deadline-message.md` の作成
3. `memory_bank/report/2026-03-18_line-deadline-message.md` の作成

## 保存先

- 成果物: `projects/unikoschool-launch/marketing/line-posts/wado-line/260318_deadline-message.md`
- plan: `memory_bank/plan/2026-03-18_line-deadline-message.md`
- report: `memory_bank/report/2026-03-18_line-deadline-message.md`

## リスク・前提

- 遷移先URLは過去のコンテキストから抽出した `https://utage-system.com/p/2475iiyrC23E` を使用する
