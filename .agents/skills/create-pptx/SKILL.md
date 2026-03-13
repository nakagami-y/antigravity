---
name: create-pptx
description: >
  Generate PowerPoint (.pptx) presentations from outlines or bullet points.
  Creates professionally styled slides with charts, tables, and image support.
  PIL-based programmatic image generation for title backgrounds and hero images.
  Ideal for marketing proposals, seminar materials, and business presentations.
  Use when: user says "create pptx", "make powerpoint", "build a deck",
  "パワポ作って", "PPTX作って", "プレゼン資料を作成して",
  "提案書作って", "スライドをPPTXで",
  or when generating PowerPoint files.
version: "2.0.0"
last_reviewed: "2026-02-17"
---

# PowerPoint生成スキル (create-pptx)

python-pptx を使って .pptx ファイルを生成する。

---

## 前提条件

- `pip install python-pptx` 済み
- `pip install Pillow` — 任意。タイトル背景画像の自動生成に使用
- Python 3.11+

---

## トリガー

- `/create-pptx [テーマ]`
- 「パワポ作って」
- 「PPTX作って」
- 「プレゼン資料をPowerPointで」
- 「提案書作って」

## 入力

- **スライド骨子**: 必須。各スライドのタイトル・内容（なければヒアリング）
- **用途**: 任意。セミナー / 提案資料 / 社内説明 / 報告書
- **カラーテーマ**: 任意。デフォルトは Navy + Mint（またはNavy + Accent Blue）
- **枚数目安**: 任意
- **参考スライド**: 任意。既存PPTXを参照してデザインを合わせる場合

---

## ワークフロー

### Step 1: ヒアリング

以下を確認:
- テーマ / タイトル
- 枚数目安（指定なければ内容に応じて決定）
- 用途（セミナー / 提案 / 報告）
- カラー（デフォルト: Navy #1E3A5F + Mint #00D4AA）
- 画像の有無（PIL生成 / マスコット / 写真）
- 参考デザイン（既存PPTXがあれば分析して合わせる）

### Step 2: スライド構成設計

13種のスライドタイプから構成を組み立てる:

| タイプ | 用途 | 詳細 |
|------|------|------|
| `title` | タイトル | タイトル + サブタイトル + 日付 + 背景画像（PIL生成可） |
| `divider` | 扉・中表紙 | Navy背景 + 中央揃えテキスト + アクセントライン |
| `fullbleed` | キーメッセージ | Navy背景 + ど真ん中の大きなテキスト（扉と併用可） |
| `agenda` | アジェンダ | 番号付きリスト |
| `content` | コンテンツ | 見出し + 箇条書き |
| `two_column` | 2カラム | 左テキスト + 右テキスト/画像 |
| `three_cards` | 3カード | 3列カードレイアウト（アクセントバー付き） |
| `comparison` | 比較（2択） | ✕ vs ○ の対比カード |
| `demo` | デモ手順 | ステップ番号付きの手順リスト |
| `table` | 表データ | 表形式のデータ |
| `triple_comparison` | 3列比較 | 3つの項目を並べて比較 |
| `data` | グラフ | 棒/円/折れ線グラフ |
| `closing` | クロージング | CTA + 連絡先 + 感謝 |

### Step 3: Pythonスクリプト生成

`scripts/template.py` をベースに、ユーザーの内容で SLIDES リストを埋めたスクリプトを生成する。

**重要ポイント**:
- 日本語テキストはUnicodeエスケープ(`\uXXXX`)で記述
- 画像パスはフォワードスラッシュ(`/`)で指定
- OUTPUT_PATHを内容に応じて設定
- 大規模スライド（20枚以上）ではビルダーのディスパッチテーブルを使う

### Step 4: 実行・確認

1. スクリプトを実行: `python {script_path}`
2. 出力ファイルを `ls` で確認（存在 + サイズ）
3. スライド数・ファイルサイズを報告

---

## デザインガイド

### デフォルトカラーテーマ（Navy + Mint）

| 用途 | 色 | Hex |
|------|-----|-----|
| 背景 | ホワイト | `#FFFFFF` |
| メインテキスト | ダーク | `#333333` |
| タイトル・見出し | Navy | `#1E3A5F` |
| アクセント | Mint | `#00D4AA` |
| サブテキスト | グレー | `#666666` |
| 背景アクセント | Light Gray | `#F0F4F8` |
| 扉サブテキスト | Light Navy | `#BBC3CF` |

### 代替テーマ（Navy + Accent Blue — セミナー向け）

参考デッキに合わせる場合に使用。

| 用途 | 色 | Hex |
|------|-----|-----|
| 背景（Navy） | ダークネイビー | `#1B3A5C` |
| テキスト（白） | ホワイト | `#FFFFFF` |
| アクセント | Accent Blue | `#4A7FB5` |
| サブテキスト | Light Blue | `#8EAED0` |
| ミュート | Footer Blue | `#6B8DB5` |
| ページ番号 | Muted | `#4A6A8A` |

### フォント

**デフォルト（Meiryo）:**

| 用途 | フォント | サイズ |
|------|--------|------|
| メインタイトル | Meiryo (Bold) | 36pt |
| スライド見出し | Meiryo (Bold) | 28pt |
| 本文 | Meiryo | 18pt |
| キャプション | Meiryo | 12pt |
| 箇条書き | Meiryo | 16pt |

**代替（Georgia + Calibri — セミナー向け）:**

| 用途 | フォント | サイズ |
|------|--------|------|
| 見出し | Georgia (Bold) | 24-40pt |
| 本文 | Calibri | 12-16pt |

> Noto Sans JPはpptx埋め込みが困難なため、Meiryoをデフォルトとする。
> Windows以外ではフォールバックとしてシステムフォントが使われる。

### スライドサイズ

- **16:9** (ワイドスクリーン): `Inches(13.333, 7.5)` ← デフォルト
- **16:9** (参考デッキ合わせ): `Inches(10.0, 5.625)` — 一部の参考デッキはこのサイズ
- 4:3 (スタンダード): `Inches(10, 7.5)`

### レイアウト原則

- 余白: 上下左右に十分な余白（スライド端から0.4"以上）
- テキスト量: 1スライドで6行以内（多い場合は分割）
- 画像: スライドの40-60%を占める（入れる場合）
- アクセントライン: スライド下部に細いアクセントカラーのライン
- **adaptive spacing**: アイテム数に応じて行間を自動調整 `min(max_spacing, available_height / item_count)`

### タイトルスライド レイアウト

**テキストのみ（フルワイド）**:
- テキスト幅: 11.333"（左右余白1"ずつ）
- タイトル(36pt) → アクセントライン → サブタイトル(20pt) → ゴール(16pt) → 日付(14pt)

**PIL背景画像あり（企業プレゼン風）**:
- 背景: PIL生成のスカイライン+斜めカット画像（フルスライド）
- テキスト: 斜めカットの右側（ダーク部分）に配置
- タイトル(40pt Bold) → アクセントライン → サブタイトル(16pt) → 日付(10pt)

**画像あり（左右分割）**:
- テキスト幅: 7"（左60%）、画像: 4"幅（右35%）
- 画像はアスペクト比を自動維持（width指定のみ）

### 扉（Divider / Fullbleed）スライド レイアウト

**divider（セクション区切り）**:
- 背景: Navy（フルスライド）
- ラベル: 中央揃え（14pt, Accent Blue）
- タイトル: 中央揃え（30pt Bold, 白）
- アクセントライン: 中央（2.40" 幅）

**fullbleed（キーメッセージ — ど真ん中）**:
- 背景: Navy（フルスライド）
- メインテキスト: **垂直・水平ともに中央揃え**（30pt Bold, 白, `v_center=True`）
- サブテキスト: メインの直下（14pt, Light Blue）
- 配置計算: `block_start = (slide_height - total_block_height) / 2`

---

## PIL画像生成（APIなしで背景画像を作る）

Pillow (PIL) を使ってプログラムで背景画像を生成する。Gemini API等が不要。

### 前提

```python
try:
    from PIL import Image, ImageDraw, ImageFilter
    HAS_PIL = True
except ImportError:
    HAS_PIL = False
```

PIL が無い場合はフォールバックで `_dark_bg()` を使う。

### 企業プレゼン風タイトル背景 (`_generate_title_bg`)

参考: セミナーデッキのスカイライン+斜めカットスタイル。

- **左側 (~55%)**: 抽象的なビル群シルエット（ネイビートーンの矩形 + 窓の光ドット）
- **斜めカット**: ポリゴン描画で左のスカイラインと右のダークネイビーを分離
- **アクセントストライプ**: 斜めの半透明ブルーライン
- **右側**: クリーンなダークネイビー（テキスト配置エリア）
- **パーティクル + グロー**: 右側に小さなドットとぼかしグロー

### テック風ヒーロー背景 (`_generate_hero`)

- ダークグラデーション（ネイビートーン）
- サブタルなグリッドパターン
- ネットワークノード（GaussianBlurでグロー効果）
- ノード間の接続線
- 浮遊パーティクル
- アクセントグロースポット

### 実装のポイント

- `random.seed(N)` で再現性を確保
- RGBA モードで描画 → `Image.alpha_composite()` で合成
- `ImageFilter.GaussianBlur(radius=N)` でグロー効果
- `draw.polygon()` で斜めカット/三角形
- `draw.rounded_rectangle()` でモダンな角丸
- 最終出力は `.convert("RGB")` で RGB に変換して保存

---

## テキストの垂直中央揃え（v_center）

python-pptx にはテキストフレームの垂直アンカー設定がないため、XML直接操作で実現する。

```python
def _text(slide, left, top, width, height, text, font_name, size, color,
          bold=False, align=None, wrap=True, v_center=False):
    tx = slide.shapes.add_textbox(left, top, width, height)
    tf = tx.text_frame; tf.word_wrap = wrap
    if v_center:
        from pptx.oxml.ns import qn
        body_pr = tf._txBody.find(qn("a:bodyPr"))
        if body_pr is not None:
            body_pr.set("anchor", "ctr")
    # ... テキスト設定
```

fullbleed スライドで「ど真ん中」配置する場合に使用。

---

## 画像埋め込み

ユーザーが画像パスを指定した場合、スライドに埋め込む:
- `title` タイプ: PIL生成背景 or `image_path` フィールドで右側に画像配置
- `two_column` タイプ: `image_path` フィールドで右側に画像配置
- ロゴやマスコットは指定位置に配置
- マスコットアセット: `98_assets/わど素材/mascot_*.png`
- 画像は `width` 指定のみでアスペクト比を自動維持

---

## グラフ対応

python-pptx のチャート機能で以下をサポート:

| タイプ | 用途 | python-pptxメソッド |
|------|------|----------------|
| 棒グラフ | 比較 | `add_chart(XL_CHART_TYPE.COLUMN_CLUSTERED, ...)` |
| 円グラフ | 割合 | `add_chart(XL_CHART_TYPE.PIE, ...)` |
| 折れ線 | 推移 | `add_chart(XL_CHART_TYPE.LINE, ...)` |
| 表 | データ一覧 | `add_table(rows, cols, ...)` |

---

## 出力先

```
assets/exports/slides/{テーマスラッグ}/{テーマスラッグ}.pptx
```

セミナー関連の場合:
```
projects/udemy/output/seminar/{案件名}/slides.pptx
```

ディレクトリがない場合は自動作成する。

---

## テンプレート

スクリプト生成時は `scripts/template.py` をベースにする。
`SLIDES` リストと `OUTPUT_PATH` をユーザーの内容に合わせて置き換える。

大規模デッキ（20枚以上）では、ビルダーごとに関数を分け `BUILDERS` ディスパッチテーブルで管理する:

```python
BUILDERS = {
    "title": build_title,
    "divider": build_divider,
    "fullbleed": build_fullbleed,
    "content": build_content,
    # ...
}
for slide_data in SLIDES:
    builder = BUILDERS.get(slide_data["type"])
    if builder:
        builder(prs, slide_data)
```

---

## 注意事項

- **ファイルサイズ**: 30MB以下推奨。画像が多い場合は圧縮を検討
- **フォント**: MeiryoはWindows標準搭載。Macで開くと代替フォントになる
- **グラフ**: データが必要。数値がない場合はサンプルデータで生成
- **日本語**: Unicodeエスケープでスクリプトに埋め込む
- **PIL画像**: `HAS_PIL` フラグでフォールバック対応。PILなしでも動作する
- **スライドサイズ**: 参考デッキがある場合はそのサイズに合わせる（デフォルト 13.333×7.5 と 10.0×5.625 の2種）
- **ページ番号**: 大規模デッキでは右下にページ番号（`N / TOTAL`）を追加
- **adaptive spacing**: アイテム数が多い場合は `min(max, available / count)` で自動調整
