---
target_repo: "gami-antigravity"
task_type: "standardization"
planned_rules:
  - "GEMINI.md"
  - "AGENTS.md"
  - ".agents/rules/04-memory-routing.md"
  - ".agents/rules/05-quality-check.md"
planned_workflows: []
planned_skills: []
planned_knowledge:
  - "AI_organization templates"
status: active
report_required: true
---

# AI実行Plan: gami-antigravity AI実行 fact log 標準反映

## まずこれだけ見ればOK

- 依頼: gami-antigravity の AI実行ログ導線を新標準へ揃える
- ゴール: template、rule、README 導線を事実ログ中心へ更新する
- 完了条件: root rule と `memory_bank` template が新標準になっている

## AIが今回見る予定のもの

- ルール: `GEMINI.md`、`AGENTS.md`、`.agents/rules/`
- workflow: 既存 workflow は参照のみ
- skill: なし
- knowledge: `AI_organization` 側の正本テンプレ

## 実行方針

- `memory_bank` template を更新し、README と rule にある旧診断前提の説明を差し替える

## やること

1. `GEMINI.md`、`AGENTS.md`、README を更新する
2. `04-memory-routing.md` と `05-quality-check.md` を更新する
3. `_TEMPLATE.md` を更新し、report を残す

## 保存先

- 成果物: root rule / README / `memory_bank`
- plan: `memory_bank/plan/2026-03-20_ai-execution-fact-log-standardization.md`
- report: `memory_bank/report/2026-03-20_ai-execution-fact-log-standardization.md`

## リスク・前提

- Udemy の出力契約や workflow 本体は変更しない
