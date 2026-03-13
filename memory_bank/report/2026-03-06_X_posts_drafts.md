---
target_repo: gami-antigravity
task_type: udemy_post
used_rules:
  - 20-udemy-voice.md
  - 21-udemy-compliance.md
used_workflows:
  - udemy-post-create.md
used_skills: []
used_knowledge:
  - projects/udemy/contracts/output.md
  - projects/udemy/samples/winning-patterns.md
primary_issue_layer: instruction
outcome: success
friction_score: 3
rework_needed: false
linked_plan: memory_bank/plan/2026-03-06_X_posts_drafts.md
---

# AI実行レポート: 8日投稿・Udemy関連のX投稿案作成

## まずこれだけ見ればOK

- 依頼: 3月8日用の開発コラボ告知と、Udemy講座告知を含む X 投稿案を、がっつり目のトーンで作ること
- 結果: 開発コラボ用と Udemy 告知用の投稿案を複数案 + 最終案の形で整理した
- 次回のコツ: 媒体、目的、CTA に加えて「どれくらい強めのトーンか」を最初に明記すると、途中の要件追加が減る

## AIが見たもの

### 主に参照したファイル

- `memory_bank/plan/2026-03-06_X_posts_drafts.md`
- `projects/udemy/contracts/output.md`
- `projects/udemy/samples/winning-patterns.md`

### 使ったルール / workflow / skill

- ルール:
  - `20-udemy-voice.md`
  - `21-udemy-compliance.md`
- workflow:
  - `udemy-post-create.md`
- skill:
  - なし

## AIの判断

- 依頼は「複数案を出しつつ、最終的にすぐ使える 1 本も欲しい」と解釈した
- 投稿を分散させるより、各テーマで「参考用 3 案 + 強めの最終案」を出したほうが実用的だと判断した
- CTA は 1 投稿 1 つに絞り、開発コラボと Udemy 告知で役割を分けた

## 出力結果

- 成果物:
  - `projects/udemy/output/X_posts_drafts.md`
- 変更ファイル:
  - `memory_bank/report/2026-03-06_X_posts_drafts.md`
- QA / 確認結果:
  - X 向けに断定を強めつつ、AI 臭い表現と過剰な誇張を避けた
  - CTA を複数混在させない構成に整理した

## 次回もっと良くするには

- 追加であると良い情報:
  - 投稿の文字数上限
  - 強さの度合い
  - 絶対に入れたい固有名詞
- おすすめの依頼文:
  - `UdemyのX投稿を作って。目的は認知、CTAは講座ページ。強めのトーンで、3案 + 最終案で出して。`
- 再利用できる rule / workflow / skill 候補:
  - `udemy-post-create.md`

## 診断ログ

### blocking_factors

- 初回 brief だけでは、コラボ相手、CTA、Udemy 告知の条件変更が後出しになった

### root_cause

- 最大の摩擦は実装ではなく、指示の詳細条件が途中で増えたことだった

### quality assessment

- instruction_quality: 中。目的は明確だったが、細部条件が追加で確定した
- rule_quality: 高。トーンと NG 表現の制約は判断に役立った
- workflow_quality: 高。3案 + 1本化の流れがそのまま使えた
- knowledge_quality: 中。勝ち筋の参照はあったが、投稿条件の決定には直接効かない部分もあった

### suggested_fix

- 依頼テンプレに `媒体 / 目的 / CTA / トーンの強さ` を必須項目として先に書かせる
