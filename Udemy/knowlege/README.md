# 成果物・配布物マップ

受講者が講座内で使う/受け取る成果物・配布テンプレートの一覧。
各セクションで「何を配るか」「どのファイルが該当するか」を紐付ける。

---

## セクション別 成果物・配布物マップ

### Sec 01: はじめに（この講座でできること）

| 配布物 | ファイル | 説明 |
|--------|---------|------|
| 5Cメソッド早見表 | `5c-method-cheatsheet.md` | 5つの成果物の型（Calendar, Copy, Chart, Communication, Campaign）の早見シート |

### Sec 02: 準備（Claude Code / VS Code / Git）

| 配布物 | ファイル | 説明 |
|--------|---------|------|
| Gitコマンド早見表 | `git-cheatsheet.md` | 講座内で使うGitコマンドのチートシート |

### Sec 03: 作り方の土台（CLAUDE.md）

| 配布物 | ファイル | 説明 |
|--------|---------|------|
| CLAUDE.md最小テンプレート | `claude-md-template.md` | CLAUDE.mdの最小構成テンプレート |
| 曖昧表現辞書 | `ambiguous-expression-dictionary.md` | 「いい感じに」等の曖昧表現→具体化変換リスト |

**撮影用デモファイル** (`filming/staged/`):
- `claude-md-v0.md` ~ `claude-md-v3.md` — デモで段階的に進化させるCLAUDE.mdの4バージョン

### Sec 04: 成果物1 — SNS投稿カレンダー

| 配布物 | ファイル | 説明 |
|--------|---------|------|
| CSVテンプレート | `sns-calendar-template.csv` | SNSカレンダーの入力用テンプレート |
| CSV出力サンプル | `sns-calendar-sample-output.csv` | 完成例（30日分の投稿カレンダー） |
| チェックリスト | `sns-calendar-checklist.md` | SNSカレンダー作成時の品質チェック項目 |

**撮影用Skillファイル** (`filming/staged/sns-calendar-skill/`):
- `SKILL.md` — デモで使う `/sns-calendar` スキル定義

### Sec 05: 安全に使う（止める・戻す・守る）

配布テンプレートなし（スライド内で設定おすすめ表を解説）

### Sec 06: Skillsでコマンド1つにまとめる

| 配布物 | ファイル | 説明 |
|--------|---------|------|
| SNSカレンダーSkill | `sns-calendar-skill.md` | `/sns-calendar` のSKILL.md完成版（Sec04のスキル化） |

### Sec 07: 成果物2 — ブログ下書き

| 配布物 | ファイル | 説明 |
|--------|---------|------|
| ブログ下書きSkill | `blog-draft-skill.md` | `/blog-draft` のSKILL.md |
| 出力サンプル | `blog-draft-sample.md` | ブログ下書きの完成例 |
| チェックリスト | `blog-draft-checklist.md` | 下書き品質チェック項目 |
| プロンプト例集 | `blog-draft-prompt-examples.md` | よく使うプロンプトパターン集 |

**撮影用Skillファイル** (`filming/staged/blog-draft-skill/`):
- `SKILL.md` — デモで使う `/blog-draft` スキル定義

### Sec 08: 成果物3 — 週次/月次レポート

| 配布物 | ファイル | 説明 |
|--------|---------|------|
| レポートSkill | `report-skill.md` | `/weekly-report` のSKILL.md |
| 入力CSVサンプル | `report-input-sample.csv` | レポート生成用のサンプルデータ |
| 出力サンプル | `report-output-sample.md` | レポートの完成例 |
| 数字チェックリスト | `report-number-checklist.md` | 数字・計算の正確性チェック項目 |
| Excel連携ガイド | `report-excel-guide.md` | Excelファイルとの連携方法 |

**撮影用Skillファイル** (`filming/staged/weekly-report-skill/`):
- `SKILL.md` — デモで使う `/weekly-report` スキル定義

### Sec 09: 成果物4 — 議事録→タスク化

| 配布物 | ファイル | 説明 |
|--------|---------|------|
| 議事録Skill | `minutes-skill.md` | `/minutes-to-tasks` のSKILL.md |
| 入力サンプル（文字起こし） | `minutes-sample-input.md` | 議事録の元になるサンプル文字起こし |
| 出力サンプル（議事録） | `minutes-output-sample.md` | 整形済み議事録の完成例 |
| タスクCSVサンプル | `minutes-tasks-sample.csv` | 議事録から抽出されたタスク一覧の完成例 |

**撮影用Skillファイル** (`filming/staged/minutes-skill/`):
- `SKILL.md` — デモで使う `/minutes-to-tasks` スキル定義

### Sec 10: 成果物5 — 告知LP

| 配布物 | ファイル | 説明 |
|--------|---------|------|
| LP Skill | `event-lp-skill.md` | `/event-lp` のSKILL.md |
| HTMLテンプレート | `event-lp-template.html` | LP生成の元テンプレート |
| HTML出力サンプル | `event-lp-sample.html` | 完成LPのサンプル |
| チェックリスト | `event-lp-checklist.md` | LP公開前チェック項目 |

**撮影用Skillファイル** (`filming/staged/event-lp-skill/`):
- `SKILL.md` — デモで使う `/event-lp` スキル定義

### Sec 11: まとめ（続けるコツ）

配布テンプレートなし（Sec01-10の全テンプレートを一式として案内）

---

## ファイル数サマリー

| カテゴリ | ファイル数 |
|---------|----------|
| 配布テンプレート・サンプル（`deliverables/`） | 25 |
| 撮影用デモファイル（`filming/staged/`） | 9（CLAUDE.md 4版 + Skill 5つ） |
| **合計** | 34 |

---

## その他の制作物（受講者には非配布）

| ディレクトリ | 内容 | ファイル数 |
|------------|------|----------|
| `slides/` | スライド原稿（Marp形式） | 11 |
| `scripts/` | 講師台本 | 11 |
| `slide-templates/final/` | スライド画像（PNG） | sec01: 17枚, sec02: 16枚, sec03: 11枚 |
| `design/` | 講座設計・戦略ドキュメント | 6 |
| `marketing/` | Udemy掲載文・競合リスト・ローンチ記事 | 4 |
| `launch/` | ローンチ戦略・アカウント設定 | 2 |
| `review/` | ファクトチェック・修正記録 | 2 |
| `filming/` | 撮影準備（ランシート・チェックリスト・デモ環境） | 4 + staged/ |
| `asset/` | 共通アセット（わどキャラクター画像） | 1 |
| `minutes/` | 会議記録 | 10 |

---

**最終更新**: 2026-03-03
