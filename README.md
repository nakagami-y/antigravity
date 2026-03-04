# Claude Code Starter Kit

Claude Code を最大限活用するための「最小構成テンプレート」。

## 使い方（3ステップ）

### Step 1: このフォルダをコピー

自分のプロジェクトフォルダに、このフォルダの中身をまるごとコピーする。

```bash
# 例: 自分のプロジェクトフォルダにコピー
cp -r ~/Desktop/claude-code-starter-kit/* ~/my-project/
cp -r ~/Desktop/claude-code-starter-kit/.* ~/my-project/  # 隠しファイルも
```

### Step 2: Claude Code を起動

プロジェクトフォルダで Claude Code を起動する。

```bash
cd ~/my-project
claude
```

### Step 3: セットアップウィザードを実行

Claude Code の中で以下を入力する:

```
/setup-wizard
```

あとは AI との対話に答えていくだけ。
5つのレベルをクリアすると、自分専用の設定が完成する。

## レベル一覧

| Lv | やること | 生成されるファイル |
|----|---------|-----------------|
| 1 | プロジェクトの自己紹介 | `CLAUDE.md` を更新 |
| 2 | AIのキャラを決める | `.claude/rules/02-style.md` |
| 3 | 最初のスキルを作る | `.claude/skills/{名前}/SKILL.md` |
| 4 | 作業ログの仕組みを知る | `memory_bank/` の使い方 |
| 5 | 仕上げチェック | 全体の整合性を確認 |

## フォルダ構成の説明

```
your-project/
├── CLAUDE.md                     # プロジェクトの指示書（最重要）
├── CLAUDE.local.md               # 個人用の指示（gitに入れない）
├── .claude/
│   ├── rules/                    # 自動適用されるルール
│   │   ├── 01-safety.md          # 安全ルール（捏造禁止・PII保護等）
│   │   ├── 03-tool-tips.md       # ツールの使い方と制限
│   │   ├── 04-memory-routing.md  # メモリの整理ルール
│   │   ├── 05-quality-check.md   # セルフチェックの習慣
│   │   └── 10-skill-design-guide.md # スキル設計ガイド
│   ├── agents/                   # 専門エージェント（7個同梱）
│   │   ├── brain.md              # 意思決定OS（指揮官エージェント）
│   │   ├── brain-knowledge.md    # Brain用の判断ナレッジベース
│   │   ├── brain-manual.md       # Brainの使い方マニュアル
│   │   ├── security-reviewer.md  # セキュリティレビュー
│   │   ├── code-reviewer.md      # コードレビュー
│   │   ├── researcher.md         # リサーチ・調査
│   │   ├── writer.md             # コンテンツ執筆
│   │   ├── strategist.md         # 意思決定パートナー（軽量版）
│   │   └── weekly-coach.md       # 週次振り返りコーチ
│   ├── skills/                   # スラッシュコマンドで呼べるスキル（19個同梱）
│   │   ├── setup-wizard/         # セットアップウィザード
│   │   ├── plan/                 # 計画書を作る
│   │   ├── report/               # 実装レポートを作る
│   │   ├── review/               # コード/文章をレビュー
│   │   ├── daily-log/            # 日次の作業ログ（勤務報告）
│   │   ├── todo/                 # タスク管理
│   │   ├── brainstorm/           # アイデア出し（8つのフレームワーク）
│   │   ├── hook/                 # フック案を10個生成（H1〜H8型）
│   │   ├── seo-optimize/         # SEO最適化（キーワード分析〜改善）
│   │   ├── content-extraction/   # 長文→マルチ媒体コンテンツ抽出
│   │   ├── presentation-builder/ # スライド構成を設計
│   │   ├── create-pptx/          # PowerPoint自動生成
│   │   ├── competitive-watch/    # 競合ウォッチ（定期スキャン）
│   │   ├── customer-interview/   # 顧客インタビュー（ペルソナ対話）
│   │   ├── reply-draft/          # 返信案を3パターン生成
│   │   ├── coach/                # 週次1on1振り返りコーチ
│   │   ├── fix-issue/            # GitHubイシュー修正ガイド
│   │   ├── skill-audit/          # スキルの健全性を監査
│   │   └── playwright-cli/       # ブラウザ操作の自動化（テスト・スクショ・データ抽出）
│   └── settings.local.json       # Claude Codeの権限設定
├── memory_bank/                  # 作業ログ（AIの記憶の代わり）
│   ├── plan/                     # 計画書の保存先（テンプレ付き）
│   └── report/                   # 実装レポートの保存先（テンプレ付き）
├── 00_knowledge/                  # ブランド・事業のナレッジベース
│   ├── README.md                 # ナビゲーション（全体構成・参照ガイド）
│   ├── wado/                     # 個人ブランドの定義
│   ├── hikari/                   # サブブランド（例）
│   └── unionai/                  # 法人ブランド（例）
├── assets/                       # 生成ファイルの保存先
│   ├── images/                   # 生成画像・図解・サムネイル
│   ├── exports/                  # PPTX・PDF・HTML等の書き出し
│   └── screenshots/              # ブラウザスクリーンショット
└── .gitignore
```

## 各ファイルの役割

| ファイル | 役割 | 編集タイミング |
|---------|------|-------------|
| `CLAUDE.md` | プロジェクト全体の指示書。Claude が毎回読む | プロジェクト方針が変わったとき |
| `.claude/rules/*.md` | 番号順に自動適用されるルール | 「毎回こうしてほしい」が増えたとき |
| `.claude/agents/*.md` | 専門エージェント。Task toolで呼び出す | 専門的な分析・レビューが必要なとき |
| `.claude/skills/*/SKILL.md` | `/スキル名` で呼べるコマンド | よくやる作業をスキル化したいとき |
| `memory_bank/` | AIの記憶の代わりになる作業ログ | 大きめの作業の前後 |
| `memory_bank/*/_TEMPLATE.md` | plan / report の書き方テンプレート | 参考にする（手動で書くとき） |
| `00_knowledge/` | ブランド・事業・顧客のナレッジベース（上位定義層） | ブランド方針や事業構造が変わったとき |
| `assets/` | スキルが生成した画像・PPTX・スクショの保存先 | 自動保存される。大きいファイルは .gitignore 検討 |
| `settings.local.json` | 権限の自動許可設定 | ツール許可のポップアップが面倒なとき |

## ルールファイルの詳細

| # | ファイル | 内容 |
|---|---------|------|
| 01 | safety.md | 捏造禁止・個人情報保護・破壊的操作の事前確認 |
| 03 | tool-tips.md | Claude Code のツール一覧・既知の制限・失敗時の対処法 |
| 04 | memory-routing.md | 情報をどこに保存するかの判定フロー・矛盾検知 |
| 05 | quality-check.md | 生成→確認→改善のセルフチェックループ |
| 10 | skill-design-guide.md | スキルの2層構造（手順+判断軸）の設計原則 |

> **02番が空いている理由**: `/setup-wizard` の Lv.2 で口調・キャラ設定ルールが自動生成されてここに入る。

## 同梱エージェント一覧（7個）

エージェントは `.claude/agents/{名前}.md` に定義する。Claude Code の Task tool から呼び出せる専門家。

### Brain（指揮官エージェント）

| ファイル | 役割 |
|---------|------|
| `brain.md` | 意思決定OS本体。5段階の思考階層・4ドメインの判断フレーム・7問フィルター・アンチパターン検出 |
| `brain-knowledge.md` | 判断ナレッジベース。コンテンツ/ビジネス/チーム/戦略の蒸留済み判断材料 |
| `brain-manual.md` | 使い方マニュアル。2つのモード・質問テンプレート・出力の読み方 |

**2つのモード**:
- **Advisor Mode**: 「これどうすべき？」→ 構造化された推奨を返す（前提確認・判断・根拠・トレードオフ・次の一手）
- **Sparring Mode**: 「この方向性で合ってる？」→ 前提を疑い、盲点を突き、別のフレームを提示する

> Brain は他のエージェント（Writer, Researcher 等）と組み合わせて使う。Brain が判断し、専門エージェントが実行する。

### 専門エージェント

| エージェント | ファイル | やること |
|------------|---------|---------|
| Security Reviewer | `security-reviewer.md` | コードのセキュリティ脆弱性をレビュー。インジェクション・認証・秘密情報の漏洩を検出 |
| Code Reviewer | `code-reviewer.md` | コードの品質・パフォーマンス・保守性をレビュー。具体的な修正提案付き |
| Researcher | `researcher.md` | Web・コードベースのリサーチ。競合分析、情報収集、事実検証 |
| Writer | `writer.md` | 記事・ドキュメント・メール・マーケコピーの執筆。媒体別ガイドライン内蔵 |
| Strategist | `strategist.md` | 意思決定パートナー（軽量版）。前提を疑い、盲点を突き、構造化された推奨を返す |
| Weekly Coach | `weekly-coach.md` | 週次1on1の振り返りコーチ。対話で気づきを引き出し `memory_bank/` に記録 |

> **Brain vs Strategist の違い**: Brain は5段階の思考階層+4ドメインフレーム+ナレッジベース付きのフル装備。Strategist はシンプルな壁打ち用の軽量版。大きな意思決定は Brain、日常の相談は Strategist。

> **スキルとの違い**: スキルは `/コマンド名` で直接実行する「手順書」。エージェントは Task tool 経由で呼び出す「専門家」。
> スキルは決まったワークフローを実行し、エージェントは状況に応じて判断する。

---

## 同梱スキル一覧（19個）

### 基本ツール

| スキル | コマンド | やること |
|--------|---------|---------|
| Setup Wizard | `/setup-wizard` | 対話形式で初期設定。5レベルをクリアして環境構築 |
| Plan | `/plan` | 作業前の計画書を作成 → `memory_bank/plan/` に保存 |
| Report | `/report` | 作業後の実装レポートを作成 → `memory_bank/report/` に保存 |
| Review | `/review` | コードや文章をレビュー。良い点・問題点・改善案をバランスよく |
| Daily Log | `/daily-log` | 1日の作業ログ。開始時に予定、終了時に実績と学びを記録 |
| Todo | `/todo` | タスクの追加・一覧・完了。`memory_bank/todo.md` で一元管理 |
| Fix Issue | `/fix-issue` | GitHubイシューの調査→原因特定→修正→テストまでガイド |

> `/plan` → 承認 → 作業 → `/report` のサイクルを回すと、セッションをまたいだ作業が安定する。

### コンテンツ制作

| スキル | コマンド | やること |
|--------|---------|---------|
| Brainstorm | `/brainstorm` | 8つのフレームワーク（SCAMPER, JTBD等）でアイデアを5〜7個生成 |
| Hook | `/hook` | H1〜H8の型でフック案を10個生成。心理メカニズムで評価 |
| Content Extraction | `/content-extraction` | 長文コンテンツからSNS・動画・メルマガ用ネタを抽出 |
| Reply Draft | `/reply-draft` | メッセージに対する返信を3パターン（丁寧/カジュアル/専門）で生成 |

### リサーチ・分析

| スキル | コマンド | やること |
|--------|---------|---------|
| Competitive Watch | `/competitive-watch` | 競合の動向を4軸でスキャンし、差別化機会をレポート |
| Customer Interview | `/customer-interview` | ペルソナになりきって質問。Pain/Desire/Objection/Triggerを深掘り |
| SEO Optimize | `/seo-optimize` | キーワード分析〜見出し構造〜メタ情報まで一括SEO最適化 |

### プレゼン・スライド

| スキル | コマンド | やること |
|--------|---------|---------|
| Presentation Builder | `/presentation-builder` | アイデアからスライド構成を設計（5つのテンプレート） |
| Create PPTX | `/create-pptx` | python-pptxでPowerPointファイルを自動生成 |

### ブラウザ自動化

| スキル | コマンド | やること |
|--------|---------|---------|
| Playwright CLI | `/playwright-cli` | ブラウザ操作を自動化。Webテスト・フォーム入力・スクショ・データ抽出 |

### 運用・改善

| スキル | コマンド | やること |
|--------|---------|---------|
| Coach | `/coach` | 週次の振り返り1on1。対話で気づきを引き出し記録 |
| Skill Audit | `/skill-audit` | スキルの健全性を8項目×12.5点で採点し改善提案 |

## よくある質問

**Q: CLAUDE.md と rules/ の違いは？**
A: CLAUDE.md はプロジェクト全体の指示。rules/ はテーマ別に分割したルール。
   どちらも Claude に自動で読まれるが、rules/ のほうが整理しやすい。

**Q: skills/ にファイルを置いたのに認識されない**
A: スキルは `.claude/skills/{スキル名}/SKILL.md` の構造が必須。
   フォルダ名がスキル名になる。SKILL.md（大文字）であること。

**Q: settings.local.json って何？**
A: Claude Code がツールを使うときの許可設定。
   毎回「許可しますか？」と聞かれるのが面倒なら、ここで自動許可を設定できる。

**Q: このフォルダを git に入れていい？**
A: `.claude/` フォルダは git に入れてOK（チームで共有できる）。
   ただし `settings.local.json` と `CLAUDE.local.md` は個人設定なので `.gitignore` に入れる。

**Q: memory_bank/ って何？**
A: AIの「記憶の代わり」。plan/ に計画書、report/ に実装レポートを残す。
   AIはセッションをまたぐと過去の作業を忘れるので、ログを残すことで引き継ぎができる。
   `/plan` と `/report` コマンドで自動生成できる。手動で書く場合は `_TEMPLATE.md` を参考に。

**Q: /plan や /report はいつ使う？**
A: 「1セッションで終わらないかも」くらいの作業のとき。
   小さいタスク（typo修正、1ファイル変更等）にはいらない。
   目安: 3ファイル以上変更する or 30分以上かかりそう → plan を書く。

**Q: /review はコード以外にも使える？**
A: 使える。文章、設定ファイル、SKILL.md、なんでもレビューできる。
   レビュー対象の種類を自動判定して、適切な観点でフィードバックする。

**Q: スキルが19個もあるけど、どれから使えばいい？**
A: まずは基本の3つ: `/plan` → `/report` → `/review` のサイクルから。
   次に自分の仕事に合うものを1つ選ぶ:
   - 文章を書く人 → `/brainstorm` `/hook`
   - 開発する人 → `/fix-issue` `/seo-optimize`
   - マーケティングする人 → `/competitive-watch` `/customer-interview`
   全部使う必要はない。必要なときに必要なものを使えばOK。

**Q: agents/ と skills/ の違いは？**
A: skills/ は `/コマンド名` で実行する「手順書」。決まったステップを上から順にやる。
   agents/ は Task tool から呼び出す「専門家」。状況に応じて自分で判断して動く。
   使い分け: 毎回同じ手順でやりたい作業 → スキル。状況判断が必要な分析・レビュー → エージェント。

**Q: エージェントはどうやって呼び出す？**
A: Claude Code の会話中に「セキュリティレビューして」「このコードをレビューして」等と頼めば、
   Claude が自動的に適切なエージェントを Task tool で呼び出す。
   自分でエージェントの `.md` ファイルを編集すれば、専門性や判断基準をカスタマイズできる。

**Q: Brain エージェントはどう使い分ける？**
A: 大きな意思決定（戦略判断、商品設計、方向性の決定等）は Brain。日常の軽い相談は Strategist。
   Brain には `brain-knowledge.md` に自分の事業の判断材料を蓄積していくと、精度がどんどん上がる。
   詳しくは `brain-manual.md` を参照。

**Q: 00_knowledge/ って何？**
A: ブランド・事業・顧客の「定義情報」を置く場所。
   プロフィール、ブランドシステム、声のガイド、商品体系、顧客像などを構造化して保存する。
   スキルやルールが参照する「上流の知識」。ここを整えると、AIの出力精度が格段に上がる。
   ブランドごとにフォルダを分ける（個人ブランド / 法人 / サブブランド等）。

**Q: スキルを自分でカスタマイズしていい？**
A: どんどんやるべき。SKILL.md はただのMarkdownファイル。
   自分のワークフローに合わせて、ステップを追加したり出力形式を変えたりできる。
   `rules/10-skill-design-guide.md` を参考にすると質の高いスキルが作れる。

---

## 実践Tips

### セッションを使い分ける

AIとの会話は用途によってセッション（チャット）を分けると精度が上がる。

| 用途 | セッションの使い方 |
|------|------------------|
| **壁打ち・相談** | 考えるためのセッション。アイデア出し、方向性の検討に使う |
| **実作業** | 正確に進めるためのセッション。確定した前提だけを持ち込む |

なぜ分けるか:
- 壁打ちは思考が揺れやすく、仮説や没案が多い
- それが混ざるとAIが「どれが確定事項か」を判断しにくくなる
- 作業用セッションはコンテキストを軽くすることで出力が安定する

### 大きめのタスクの進め方

```
1. plan を書く（何をやるか・どう進めるか）
   → memory_bank/plan/ に保存

2. ユーザー（自分）が承認

3. 実行

4. report を書く（何をやったか・何が変わったか）
   → memory_bank/report/ に保存
```

この「plan → 承認 → 実行 → report」のサイクルを回すと、AIとの協業が格段に安定する。
