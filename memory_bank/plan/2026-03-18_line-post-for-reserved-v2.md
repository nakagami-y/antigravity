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

# AI実行Plan: 予約者向けLINE告知文（スライド300枚）追加修正

## まずこれだけ見ればOK

- 依頼: 予約者向けLINE告知文に「セミナー内容には300枚以上のスライドを用意していること」「参加を楽しみにしてというメッセージ」の2点を追加する。
- ゴール: ボリューム感とホスピタリティを伝え、参加意欲をさらに高める文面の完成。
- 完了条件: 
  - 300枚以上のスライドがあることが明記されている
  - 参加を楽しみにしてねというメッセージが含まれている
  - planとreportが指定ディレクトリに保存されている

## AIが今回見る予定のもの

- ルール: GEMINI.md, AGENTS.md
- workflow: 該当なし
- skill: plan, report
- knowledge: なし

## 実行方針

1. 既存のLINE告知文 (`260318-19_reserved-participants-reminder.md`) の内容を上書きベースで改修する。
2. 「セミナー内容」のパートにスライド300枚超のボリューム感を足す。
3. 文末に向かって「楽しみにお待ちください」「当日お会いできるのを楽しみにしています」というホスピタリティ要素を付け加える。

## やること

1. `memory_bank/plan/2026-03-18_line-post-for-reserved-v2.md` の作成
2. `projects/unikoschool-launch/marketing/line-posts/wado-line/260318-19_reserved-participants-reminder.md` の上書き保存
3. `memory_bank/report/2026-03-18_line-post-for-reserved-v2.md` の作成

## 保存先

- 成果物: `projects/unikoschool-launch/marketing/line-posts/wado-line/260318-19_reserved-participants-reminder.md` (Overwritten)
- plan: `memory_bank/plan/2026-03-18_line-post-for-reserved-v2.md`
- report: `memory_bank/report/2026-03-18_line-post-for-reserved-v2.md`

## リスク・前提

- 既存の「セミナー内容と参加したらできるようになることの分離」という構造は崩さずにテキストを追加する。
