# Udemy Post Create Workflow

## 目的

- `projects/udemy/` の知識を使って、SNS 投稿を再現性高く生成する
- 対象は「Udemy講座についての投稿」であり、講座教材そのものの改稿は主目的にしない

## 最初に読むファイル

- `projects/udemy/README.md`
- `projects/udemy/contracts/output.md`
- `.agents/rules/20-udemy-voice.md`
- `.agents/rules/21-udemy-compliance.md`
- `projects/udemy/samples/winning-patterns.md`
- 必要な `projects/udemy/knowledge/*.md`

`projects/udemy/knowledge/` は参照素材であり、通常は書き換え対象にしない。
`.agents/rules/20-udemy-voice.md` と `.agents/rules/21-udemy-compliance.md` は Udemy 投稿時だけ読む補助 rules であり、root の共通ルールではない。

## 入力契約

結論を変える前提だけ最大 3 つ確認する。

1. 媒体
2. 目的
3. CTA

不足があっても止まりすぎず、合理的な仮定を明記して暫定案を出す。

## 実行手順

1. brief を 1 文で要約する
2. 媒体 / 目的 / CTA を確定する
3. 使う知識ファイルを列挙する
4. 切り口を 3 つ作る
5. 投稿案を 3 本作る
6. 1 本に統合して磨く
7. QA を通す

## QA

- 文字数
- NG 表現
- 誇張表現
- AI臭
- CTA の明確性

## 出力

- 投稿案 3 本
- 最終案 1 本
- QA 結果

標準形は「3案 + 1本化 + QA結果」とする。

## 保存

- テキスト成果物を保存する場合は `projects/udemy/output/` を使う
- AI 実行 plan / report は root `memory_bank/plan/` と `memory_bank/report/` に残す
- report では「AIが見たもの」「AIの判断」「次回もっと良くするには」を必ず書く
