# AntiGravity Workspace for Content & Automation

この workspace は、Google AntiGravity に「共通ルール」と「業務ごとの実務ディレクトリ」を分けて読ませるための作業場所です。

いまのメイン用途は、`projects/udemy/` を使って Udemy講座に関する投稿を再現性高く作ることです。

## このディレクトリで何をするか

- 共通ルールを root に置く
- 共有の知識を `knowledge/` に置く
- 業務ごとの実務ファイルを `projects/` 配下に分ける
- 投稿案や制作ログを、後から見返せる形で保存する

## まず覚える 3 つ

1. `GEMINI.md`
   - この workspace 全体の共通ルールです
   - 最初にここを見れば「何を読むべきか」が分かります
2. `knowledge/`
   - 共有で使う知識置き場です
   - 基本は参照用で、日常的な編集場所ではありません
3. `projects/udemy/`
   - 今回メインで使う Udemy 投稿制作の実務ディレクトリです
   - 実際に投稿案を作るときは、ここを中心に使います
4. `memory_bank/report/`
   - AI が何を見て、どう判断したかを確認する場所です

## 全体の見取り図

```text
gami-antigravity/
├── GEMINI.md                  # workspace 全体の共通ルール
├── AGENTS.md                  # 人間向けの短い地図
├── .agents/
│   ├── rules/                 # 共通 rules と補助 rules
│   ├── workflows/             # 業務別の進め方
│   └── skills/                # 再利用する定型スキル
├── knowledge/                 # 共有 knowledge
├── projects/
│   └── udemy/                 # Udemy 投稿制作の実務層
├── memory_bank/               # repo 改修の plan / report
└── assets/                    # 画像や書き出し
```

## どこを見ればいいか

### workspace 全体を知りたいとき

1. `GEMINI.md`
2. `.agents/rules/01-*.md` から `.agents/rules/10-*.md`
3. `knowledge/README.md`

### Udemy 投稿を作りたいとき

1. `projects/udemy/README.md`
2. `.agents/workflows/udemy-post-create.md`
3. `projects/udemy/contracts/output.md`
4. `.agents/rules/20-udemy-voice.md`
5. `.agents/rules/21-udemy-compliance.md`
6. `projects/udemy/samples/winning-patterns.md`
7. 必要な `projects/udemy/knowledge/*.md`

ポイントは、`20-udemy-*` の rules は常時ルールではなく、**Udemy 投稿のときだけ読む補助ルール**だということです。

## Udemy 投稿の作り方

### 1. まず伝えること

Udemy 投稿を依頼するときは、最低でも次の 3 つがあると進めやすいです。

- 媒体
  - 例: X、LINE
- 目的
  - 例: 講座の認知、申込み、リマインド
- CTA
  - 例: 講座ページを見る、詳細を確認する

### 2. 依頼のしかた

こんな言い方で十分です。

- `UdemyのX投稿を作って。目的は認知、CTAは講座ページを見る。`
- `Udemy講座のLINE告知文を作って。申込み促進が目的。`
- `Udemy投稿として3案出してから、最後に1本へまとめて。`

`Udemy投稿` や `UdemyのX投稿` のように書くと、Udemy workflow に寄せやすくなります。

### 3. どういう流れで作られるか

Udemy workflow では、基本的に次の流れで進みます。

1. brief を 1 文で整理する
2. 媒体 / 目的 / CTA を固める
3. 使う知識を選ぶ
4. 切り口を 3 つ出す
5. 投稿案を 3 本作る
6. 1 本にまとめる
7. QA で確認する

標準の出力は **3案 + 1本化 + QA結果** です。

## ファイルごとの役割

### root で使うもの

- `GEMINI.md`
  - workspace 全体の共通ルール
- `.agents/rules/01-10`
  - 共通の出力方針
- `.agents/workflows/`
  - 業務ごとの進め方
- `knowledge/`
  - 複数業務で共通利用する知識

### Udemy で使うもの

- `projects/udemy/contracts/`
  - 出力の型
- `projects/udemy/samples/`
  - 参考にする勝ち筋
- `projects/udemy/output/`
  - 完成した投稿案の保存先
- `projects/udemy/benchmarks/`
  - 比較・検証素材
- `projects/udemy/knowledge/`
  - 参照素材

## どこを編集するか

### よく編集する場所

- `projects/udemy/contracts/`
- `projects/udemy/samples/`
- `projects/udemy/output/`
- `projects/udemy/benchmarks/`

### 基本は参照だけにする場所

- `knowledge/`
- `projects/udemy/knowledge/`

特に `projects/udemy/knowledge/` は講座台本や制作素材の保管層なので、普段の投稿生成では直接書き換えない前提です。

## 出力はどこに保存されるか

- repo 改修の plan / report:
  - `memory_bank/plan/`
  - `memory_bank/report/`
- Udemy 投稿の成果物:
  - `projects/udemy/output/`
- 画像や書き出し:
  - `assets/`

## AIレポートでまず見る場所

非エンジニアのメンバーは、root `memory_bank/report/` の report を開いたら、まず次の 3 つを見れば大丈夫です。

- `まずこれだけ見ればOK`
- `AIが見たもの`
- `次回もっと良くするには`

ここを見ると、AI がどの rule / workflow / skill / knowledge を見て、なぜその出力にしたかを追いやすくなります。

## 迷ったときの考え方

- workspace 全体の話なら `GEMINI.md` を見る
- 共通知識が必要なら `knowledge/README.md` を見る
- Udemy 投稿なら `projects/udemy/README.md` と `udemy-post-create.md` を見る
- 「このファイルを触っていいか分からない」ときは、まず `projects/udemy/README.md` の編集対象ルールを確認する
- AI がどう判断したか知りたいときは、root `memory_bank/report/` を見る
