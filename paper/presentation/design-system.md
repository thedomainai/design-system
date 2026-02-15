# Presentation Design Rules — Paper

このファイルは AI がスライドデッキ（pptx）を生成する際に従うルールセットである。
CSS ブロックは視覚仕様のリファレンスとして記載している。pptx 出力時は同等の値をスライドプロパティに変換して適用する。

## 基本設定

- 出力形式: pptx（PowerPoint）
- サイズ: 1920×1080px（16:9） — pptx 換算 13.333" × 7.5"
- フォント: Crimson Pro (300,400,600) + Instrument Sans (400,600,700) + JetBrains Mono (400,500)

```css
body {
  font-family: 'Instrument Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  background: #fdfdfc;
  color: #1a1a1a;
  overflow: hidden;
  width: 100vw; height: 100vh;
}
```

## カラーパレット

```css
:root {
  /* ─── Ink Scale ─── */
  --ink-1000: #000000;
  --ink-900:  #1a1a1a;
  --ink-800:  #2d2d2d;
  --ink-700:  #404040;
  --ink-600:  #525252;
  --ink-500:  #6b6b6b;
  --ink-400:  #8a8a8a;
  --ink-300:  #a3a3a3;
  --ink-200:  #c4c4c4;
  --ink-100:  #e0e0e0;
  --ink-50:   #f0f0f0;

  /* ─── Paper Scale ─── */
  --paper-white:  #fdfdfc;
  --paper-cream:  #faf9f7;
  --paper-warm:   #f5f4f0;
  --paper-kraft:  #eeedea;
  --paper-aged:   #e8e7e3;
  --paper-shadow: #dddcd8;
}
```

## セマンティックトークン

| トークン名 | マッピング | 値 | 用途 |
|-----------|-----------|-----|------|
| bg-page | paper-white | #fdfdfc | スライド背景 |
| bg-surface | paper-cream | #faf9f7 | カード背景 |
| bg-surface-raised | paper-warm | #f5f4f0 | コードブロック背景 |
| border-default | ink-100 | #e0e0e0 | カードのボーダー |
| border-heavy | ink-1000 | #000000 | セクション区切りの太い線 |
| text-primary | ink-900 | #1a1a1a | 本文テキスト |
| text-heading | ink-1000 | #000000 | 見出し |
| text-secondary | ink-600 | #525252 | 補助テキスト |
| text-muted | ink-400 | #8a8a8a | 日付・注釈 |
| interactive | ink-900 | #1a1a1a | ブレットポイント |

## カラーの使い分け

| 役割 | 値 |
|------|-----|
| 背景 | #fdfdfc（paper-white） |
| テキスト primary | #1a1a1a |
| テキスト secondary | #525252 |
| テキスト muted | #8a8a8a |
| 見出し | #000000 |
| ラベル（uppercase） | #6b6b6b |
| 装飾番号 | #c4c4c4 (opacity 0.4) |

Paper テーマでは色を使用しない。グレースケールのみで情報階層を表現する。

## タイポグラフィ

**注意: スライドでは 10px 未満を使わない。**

テキストカラーはタイポグラフィでは固定しない。セマンティックトークン（text-heading, text-primary, text-secondary, text-muted 等）を背景色との組み合わせで選択する。具体的な対応は「カラーの使い分け」セクションを参照のこと。

| 用途 | size | weight | line-height | letter-spacing | font |
|------|------|--------|-------------|----------------|------|
| タイトルスライド見出し | 56px | 400 | 1.1 | -1.5px | Serif |
| スライド見出し | 44px | 400 | 1.15 | -1px | Serif |
| カードタイトル | 28px | 700 | 1.3 | -0.3px | Serif |
| 本文（スライド基準） | 20px | 500 | 1.6 | 0 | Sans |
| カード本文 | 18px | 500 | 1.6 | 0 | Sans |
| ラベル(uppercase) | 14px | 700 | 1.2 | 2px | Sans |
| 数値ハイライト(大) | 64px | 400 | 1.0 | 0 | Serif |
| 数値ハイライト(小) | 48px | 400 | 1.0 | 0 | Serif |
| 装飾番号 | 72px | 400 | 1.0 | 0, opacity 0.4 | Serif |
| サブタイトル | 28px | 400 | 1.4 | -0.5px | Serif |
| 連絡先 | 18px | 500 | 1.5 | 0 | Sans |
| URL (mono) | 16px | 500 | 1.5 | 0 | Mono |
| スライド番号 (mono) | 11px | 600 | 1.0 | 0.5px | Mono |
| copyright (mono) | 10px | 500 | 1.0 | 0 | Mono |

## ボーダーラウンド

| トークン | 値 | 用途 |
|---------|-----|------|
| radius-none | 0px | カード・パネル（デフォルト） |
| radius-sm | 2px | バッジ・タグ |
| radius-md | 4px | ボタン |

**Paper テーマではカードに角丸を使用しない（radius-none: 0px）。** 唯一の例外はステータスドット（border-radius: 50%）のみ。

## マテリアル

### Flat Paper（基本カード）
```css
background: #faf9f7;
border: 1px solid #e0e0e0;
border-radius: 0;
padding: 48px 40px;
```

### Layered Paper（強調カード）
```css
background: #fdfdfc;
border: 1px solid #c4c4c4;
border-radius: 0;
box-shadow: 2px 2px 0 #f0f0f0;
```

### Editorial Rule（セクション区切り）
```css
width: 100%; height: 2px;
background: #000000;
margin: 48px 0;
```

### Double Line（重要区切り）
```css
width: 100%; height: 0;
border-top: 3px double #000000;
margin: 48px 0;
```

### マテリアル内テキスト配置

マテリアルグループ（同一種類のマテリアルが横に並ぶ集合）では、代表となる1つのマテリアルについてテキスト配置を決定し、グループ内の全マテリアルに同一ルールを適用する。個別のマテリアルごとに配置を変えない。

| マテリアル | 水平方向 | 垂直方向 | 備考 |
|-----------|---------|---------|------|
| Flat Paper（基本カード） | left | top | コンテンツは上から下へ流す |
| Layered Paper（強調カード） | center | center | インパクト重視、短いテキスト向け |
| データカード（数値ハイライト） | center | center | 数値を中央に大きく配置 |
| コードブロック | left | top | コードは左上起点 |

### 枠線と中塗りの使い分け

枠線（border/stroke）と中塗り（background fill）は基本的に併用しない。

- **併用可能な例外**: 中塗りがページ背景色に十分近い薄さで、同系統のグレーで枠線を引く場合のみ許可（例: Flat Paper の paper-cream 背景 + ink-100 ボーダー）

## レイアウト

### スライド共通
```css
.slide { width: 1920px; height: 1080px; padding: 64px 80px; }
```

### スライドコンポーネント

スライドは header / body / footer の3コンポーネントで構成する。各コンポーネントを組み合わせてスライドパターンを作成する。

#### Header

スライド上部の見出し領域。

| サブ要素 | 内容 | タイポグラフィ |
|---------|------|--------------|
| agenda | セクションラベル（例: 「01 OVERVIEW」） | 14px / 700 / uppercase / letter-spacing: 2px |
| title | スライド見出し | 44px / 400 / Serif / letter-spacing: -1px |
| main message | メインメッセージ・要点 | 20px / 500 |

**Grid（pptx 座標）:**

| プロパティ | px | inch |
|-----------|-----|------|
| left | 80 | 0.56" |
| top | 64 | 0.44" |
| width | 1760 | 12.22" |
| height（agenda + title） | 160 | 1.11" |
| height（+ main message） | 200 | 1.39" |

#### Body

メインコンテンツ領域。カード・テキスト・図表等を配置する。

**Grid（pptx 座標）:**

| プロパティ | px | inch |
|-----------|-----|------|
| left | 80 | 0.56" |
| top | header 下端 + 40 | header 下端 + 0.28" |
| width | 1760 | 12.22" |
| height | footer 上端まで（auto） | — |

#### Footer

スライド下部の固定領域。

| サブ要素 | 内容 | タイポグラフィ | 配置 |
|---------|------|--------------|------|
| page number | スライド番号 | 11px / 600 / mono / letter-spacing: 0.5px | 右寄せ |
| copyright | 著作権表示 | 10px / 500 / mono | 左寄せ |

**Grid（pptx 座標）:**

| プロパティ | px | inch |
|-----------|-----|------|
| left | 80 | 0.56" |
| top | 1032 | 7.17" |
| width | 1760 | 12.22" |
| height | 48 | 0.33" |

### スライドパターン

**1. タイトルスライド**
- Header: 使用しない
- Body: 全要素中央配置 — logo → タイトル（56px / 400 / Serif）→ サブタイトル（28px / 400 / Serif）→ 日付（16px / mono）
- Footer: copyright のみ

**2. コンテンツスライド** — 見出し + 3列カードグリッド
- Header: agenda + title
- Body: `grid-template-columns: repeat(3, 1fr); gap: 40px`
- Footer: page number + copyright

**3. 2カラムスライド** — テキスト + ビジュアル
- Header: title
- Body: `grid-template-columns: 1fr 1fr; gap: 64px; align-items: center`
- Footer: page number + copyright

**4. データスライド** — 数値ハイライト
- Header: title
- Body: 数値カード（center 配置、64px / 400 / Serif + ラベル 18px / 500 / Sans）、Flat Paper カードに内包
- Footer: page number + copyright

### 箇条書き
```css
li { font-size: 20px; line-height: 1.7; padding-left: 24px; }
li::before { width: 6px; height: 6px; border-radius: 50%; background: #1a1a1a; }
```

### コードブロック
```css
background: #f5f4f0; border: 1px solid #e0e0e0; border-radius: 0;
padding: 32px; font-family: 'JetBrains Mono'; font-size: 16px; line-height: 1.7;
```

### 表（テーブル）

| プロパティ | 値 |
|-----------|-----|
| ヘッダーフォント | 14px / 700 / uppercase / letter-spacing: 1px |
| ヘッダーカラー | text-secondary |
| ヘッダー下ボーダー | 2px solid ink-900 |
| セルフォント | 18px / 500 |
| セルカラー | text-primary |
| セルパディング | 16px 20px |
| セル line-height | 1.5 |
| 行ボーダー | 0.5px solid border-default |
| 交互行背景 | なし |
| 数値セル | mono / right-aligned |

### 画像・図表

| プロパティ | ルール |
|-----------|-------|
| 最大幅 | body 幅（1760px / 12.22"） |
| アスペクト比 | 元画像の比率を維持 |
| 配置 | body 領域内で水平中央 |
| キャプション | 画像下部、text-secondary、14px / 500、margin-top: 12px |
| スクリーンショット枠 | 1px solid border-default、border-radius: 0 |
| チャート内テキスト | 14px 以上（視認性確保） |
| チャートカラー | グレースケールのみ（ink-900, ink-600, ink-300, ink-100） |
| 背景透過 | 図表の背景は透過させスライド背景と一体化する |

### ロゴ

| スライドタイプ | 配置 | サイズ |
|-------------|------|-------|
| タイトルスライド | body 中央、タイトル上部 | height: 48px |
| コンテンツスライド | 使用しない | — |

ロゴは単色版（#000000）を使用する。

### トランジション

| 項目 | ルール |
|------|-------|
| スライド切替 | カット（瞬時切替）をデフォルトとする |
| セクション間切替 | カット（Paper テーマではフェードも使用しない） |
| オブジェクトアニメーション | 使用しない |

Paper テーマでは紙の静的な性質に従い、一切のトランジション・アニメーションを排除する。

## 禁止事項

- 10px 未満のフォントサイズを使用しない
- font-weight: 800 以上は使わない
- タイポグラフィにカラーを固定指定しない（セマンティックトークンで背景色と合わせて決定する）
- カラー（彩色）を使用しない（グレースケールのみ）
- 枠線（border）と中塗り（fill）を併用しない（ページ背景色に近い薄い中塗り + 同系統グレーの枠線の場合を除く）
- カードに角丸をつけない（radius-none: 0px）
- 1スライドにカード 3枚 or 箇条書き 5項目が上限目安
- 背景色を #fdfdfc 以外にしない
- スライドの padding を 64px 80px 未満にしない
- border-radius を radius-md（4px）を超えて使用しない（50% の円形を除く）
- グラデーション・グロウ・ブラーなどの装飾エフェクトを使用しない
- トランジション・アニメーションを使用しない
