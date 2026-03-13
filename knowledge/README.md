# knowledge — 3ブランド マスター知識ベース

## このフォルダの目的

株式会社UnionAIが展開するブランドの上流知識をまとめる。
ブランドの「何者か」「誰に何を届けるか」「どう語るか」をここで定義し、下流の workflow と skill が参照する。

## 上流と下流の関係

| 層 | パス | 役割 | 更新頻度 |
|----|------|------|---------|
| 上流（定義） | `knowledge/` | ブランドの本質・戦略・声・商品体系の定義 | 四半期〜半期 |
| 下流（運用） | `projects/udemy/knowledge/` | 日常の制作で使う知識、講座素材、台本 | 週次〜月次 |

## フォルダ構造

```text
knowledge/
├── README.md
├── operating-system/
│   └── decision-os.md
├── wado/
├── hikari/
└── unionai/
```

## AntiGravity 参照ガイド

| やりたいこと | 読むファイル |
|-------------|-------------|
| わどの口調で書きたい | `wado/voice-guide.md` |
| わどのターゲットや経歴を確認したい | `wado/profile.md` |
| 商品体系や CTA を確認したい | `wado/offer-system.md` |
| ひかりのコンセプトを確認したい | `hikari/profile.md` |
| ひかりの訴求軸を見たい | `hikari/brand-guide.md` |
| UnionAI の法人情報を確認したい | `unionai/company-info.md` |
| 事業戦略を確認したい | `unionai/strategy.md` |
| 判断の軸を確認したい | `operating-system/decision-os.md` |

## 運用ルール

- 共有知識は `knowledge/` に集約する
- Udemy 専用の実務知識は `projects/udemy/knowledge/` に置く
- 新ファイル追加時はこの README も更新する
