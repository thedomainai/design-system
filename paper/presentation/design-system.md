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

**注意: スライドでは本文 16px 未満を使わない（プロジェクション視認性）。**

| 用途 | size | weight | color | letter-spacing | font |
|------|------|--------|-------|----------------|------|
| タイトルスライド見出し | 56px | 300 | #000000 | -1.5px | Serif |
| スライド見出し | 44px | 300 | #000000 | -1px | Serif |
| カードタイトル | 28px | 600 | #000000 | -0.3px | Serif |
| 本文（スライド基準） | 20px | 400 | #1a1a1a | 0 | Sans |
| カード本文 | 18px | 400 | #525252 | 0 | Sans |
| ラベル(uppercase) | 14px | 700 | #6b6b6b | 2px | Sans |
| 数値ハイライト(大) | 64px | 300 | #000000 | 0 | Serif |
| 数値ハイライト(小) | 48px | 300 | #000000 | 0 | Serif |
| 装飾番号 | 72px | 300 | #c4c4c4 | 0, opacity 0.4 | Serif |
| サブタイトル | 28px | 300 | #525252 | -0.5px | Serif |
| 連絡先 | 18px | 400 | #6b6b6b | 0 | Sans |
| URL (mono) | 16px | 400 | #8a8a8a | 0 | Mono |
| スライド番号 (mono) | 14px | 500 | #8a8a8a | 0 | Mono |

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

## レイアウト

### スライド共通
```css
.slide { width: 1920px; height: 1080px; padding: 64px 80px; }
```

### スライドパターン

**1. タイトルスライド** — 全要素中央配置
```html
<div class="slide" style="justify-content: center; align-items: center; text-align: center;">
  <div>THE DOMAIN AI (uppercase label)</div>
  <h1>タイトル (56px/Serif/300)</h1>
  <p>サブタイトル (28px/Serif/300/#525252)</p>
  <p>日付 (16px/mono/#8a8a8a)</p>
</div>
```

**2. コンテンツスライド** — 見出し + 3列カードグリッド
```html
<div class="slide" style="flex-direction: column;">
  <div style="margin-bottom: 64px;">
    <span>LABEL (14px/700/#6b6b6b/uppercase)</span>
    <h2>見出し (44px/Serif/300)</h2>
  </div>
  <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 40px; flex: 1;">
    <div class="paper-flat">...</div>
    <div class="paper-flat">...</div>
    <div class="paper-flat">...</div>
  </div>
</div>
```

**3. 2カラムスライド** — テキスト + ビジュアル
```html
<div class="slide" style="flex-direction: column;">
  <div style="margin-bottom: 64px;">
    <h2>見出し (44px/Serif/300)</h2>
  </div>
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 64px; flex: 1; align-items: center;">
    <div>テキスト + 箇条書き</div>
    <div>ビジュアル（図表・コード等）</div>
  </div>
</div>
```

**4. データスライド** — 数値ハイライト
- 数値: 64px / Serif / weight 300 / #000000
- ラベル: 18px / Sans / #8a8a8a
- Flat Paper カードに内包、text-align center

### 箇条書き
```css
li { font-size: 20px; color: #525252; line-height: 1.7; padding-left: 24px; }
li::before { width: 6px; height: 6px; border-radius: 50%; background: #1a1a1a; }
```

### コードブロック
```css
background: #f5f4f0; border: 1px solid #e0e0e0; border-radius: 0;
padding: 32px; font-family: 'JetBrains Mono'; font-size: 16px; line-height: 1.7; color: #525252;
```

## スライド番号
```css
position: fixed; bottom: 32px; right: 48px;
font-family: 'JetBrains Mono'; font-size: 14px; color: #8a8a8a;
```

## キーボード操作（JavaScript）
```javascript
document.addEventListener('keydown', function(e) {
  if (e.key === 'ArrowRight' || e.key === ' ') { nextSlide(); }
  else if (e.key === 'ArrowLeft') { prevSlide(); }
});
```

## 禁止事項

- 本文を 16px 未満にしない
- カラー（彩色）を使用しない（グレースケールのみ）
- カードに角丸をつけない（radius-none: 0px）
- 1スライドにカード 3枚 or 箇条書き 5項目が上限目安
- 背景色を #fdfdfc 以外にしない
- スライドの padding を 64px 80px 未満にしない
- border-radius を radius-md（4px）を超えて使用しない（50% の円形を除く）
- グラデーション・グロウ・ブラーなどの装飾エフェクトを使用しない
