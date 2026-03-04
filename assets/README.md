# assets/

スキルやAIが生成したファイルの保存先。

## フォルダ構成

```
assets/
├── images/       ← 生成画像・図解・サムネイル・OG画像
├── exports/      ← PPTX・PDF・HTML等の書き出しファイル
└── screenshots/  ← playwright-cli のスクリーンショット・スナップショット
```

## 使い方

- スキルが画像やファイルを生成したとき、ここに自動保存される
- `/create-pptx` → `exports/` に .pptx を保存
- `/playwright-cli screenshot` → `screenshots/` に .png を保存
- 画像生成 → `images/` に保存

## 注意

- 大きなファイル（動画・大量の画像）は `.gitignore` に追加を検討する
- 本番環境にデプロイするファイルは別の場所（`public/` 等）で管理する
