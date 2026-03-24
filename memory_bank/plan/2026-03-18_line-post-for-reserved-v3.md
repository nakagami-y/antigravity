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

# AI実行Plan: 予約者向けLINE告知文（内容と未来の分離・前日/当日配信）

## まずこれだけ見ればOK

- 依頼: これまで1通にまとめていた予約者向けLINE告知文を、「セミナー内容」と「参加したらできるようになること」に分割し、それぞれ前日20時と当日12時に配信するよう構成変更する。
- ゴール: 接触頻度を増やし、かつ情報過多を避けることで、当日直前の期待値の最大化を図るLINE文面の完成。
- 完了条件: 
  - 前日20時配信用のメッセージ（セミナー内容）が作成されている
  - 当日12時配信用のメッセージ（参加したらできるようになること）が作成されている
  - planとreportが指定ディレクトリに保存されている

## AIが今回見る予定のもの

- ルール: GEMINI.md, AGENTS.md
- workflow: 該当なし
- skill: plan, report
- knowledge: なし

## 実行方針

1. 以前作成した `260318-19_reserved-participants-reminder.md` の内容をベースに2日間に分割し、前日用と当日用に適切な挨拶と文脈のつなぎを付与する。
2. 今回の日程に合わせて、配信日を（20日から始まるものとして）3/19 20:00, 3/20 12:00に設定する。
3. 3ファイルの出力とユーザー通知を行う。

## やること

1. `memory_bank/plan/2026-03-18_line-post-for-reserved-v3.md` の作成
2. `projects/unikoschool-launch/marketing/line-posts/wado-line/260319-20_reserved-participants-reminder.md` の作成（新ファイルとして分割版を保存）
3. `memory_bank/report/2026-03-18_line-post-for-reserved-v3.md` の作成

## 保存先

- 成果物: `projects/unikoschool-launch/marketing/line-posts/wado-line/260319-20_reserved-participants-reminder.md`
- plan: `memory_bank/plan/2026-03-18_line-post-for-reserved-v3.md`
- report: `memory_bank/report/2026-03-18_line-post-for-reserved-v3.md`

## リスク・前提

- 前日に提供した情報（300枚のスライド等）を前提として、当日側の原稿を構成する必要がある。
