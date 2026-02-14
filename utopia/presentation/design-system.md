# Presentation Design Rules — Utopia

このファイルは AI がスライドデッキ（HTML）を生成する際に従うルールセットです。
template.html はこのルールで構築されたビジュアルリファレンスです。ブラウザで開いて見た目を確認できます。

## 基本設定

- サイズ: 1920×1080px（16:9）
- 操作: キーボード ←→ / スペースでスライド切り替え
- フォント: Playfair Display (400,600,700,800,900) + Source Sans 3 (400,500,600,700,800) + JetBrains Mono (400,500)

```css
body {
  font-family: 'Source Sans 3', -apple-system, BlinkMacSystemFont, sans-serif;
  background: #0c0a08;  /* Raw Umber キャンバス */
  color: #ece5d8;
  overflow: hidden;
  width: 100vw; height: 100vh;
}
```

## カラーパレット

```css
:root {
  /* ─── Primary (Ultramarine / Lapis Lazuli) ─── */
  --primary-50:  #edf0f9;
  --primary-100: #d4daf0;
  --primary-200: #a9b5e1;
  --primary-300: #7e8fd2;
  --primary-400: #5a6db8;
  --primary-500: #3d4f9e;
  --primary-600: #2e3b78;
  --primary-700: #232d5c;
  --primary-800: #1a2145;
  --primary-900: #111630;
  --primary-950: #0a0d1e;

  /* ─── Secondary (Burnt Sienna) ─── */
  --secondary-50:  #faf6f3;
  --secondary-100: #f0e8e0;
  --secondary-200: #dcc8b5;
  --secondary-300: #c4a78c;
  --secondary-400: #a88464;
  --secondary-500: #8b6543;
  --secondary-600: #6e4f35;
  --secondary-700: #553d29;
  --secondary-800: #3e2d1e;
  --secondary-900: #2a1e14;
  --secondary-950: #1a130c;

  /* ─── Accent (Vermillion) ─── */
  --accent-50:  #fdf0ee;
  --accent-100: #f9d8d3;
  --accent-200: #f0ada3;
  --accent-300: #e3806f;
  --accent-400: #d45a45;
  --accent-500: #b83a24;
  --accent-600: #93301e;
  --accent-700: #712618;
  --accent-800: #521c12;
  --accent-900: #38120c;
  --accent-950: #200a06;

  /* ─── Gold (Gold Ochre) ─── */
  --gold-50:  #fdf8ee;
  --gold-100: #f8ecd0;
  --gold-200: #eed6a0;
  --gold-300: #dfbc6e;
  --gold-400: #cca044;
  --gold-500: #b38628;
  --gold-600: #8f6b20;
  --gold-700: #6d5218;
  --gold-800: #4e3b12;
  --gold-900: #33270c;
  --gold-950: #1c1507;

  /* ─── Neutral (Raw Umber Canvas) ─── */
  --neutral-0:    #0c0a08;
  --neutral-50:   #110f0c;
  --neutral-100:  #18150f;
  --neutral-200:  #211d16;
  --neutral-300:  #2c2720;
  --neutral-400:  #3a342b;
  --neutral-500:  #524a3f;
  --neutral-600:  #6e6456;
  --neutral-700:  #8e8272;
  --neutral-800:  #b0a494;
  --neutral-900:  #d2c8b8;
  --neutral-950:  #ece5d8;
  --neutral-1000: #faf5ed;

  /* ─── Status Colors ─── */
  --success-400: #6abf7b;  --success-500: #3a9e4e;  --success-600: #2a7d3a;  --success-900: #12261a;
  --warning-400: #e0b84a;  --warning-500: #c89b2a;  --warning-600: #a07820;  --warning-900: #2a2210;
  --error-400:   #d46860;  --error-500:   #b84040;  --error-600:   #943030;  --error-900:   #2a1210;
  --info-400:    #6a8ec0;  --info-500:    #4a70a8;  --info-600:   #365890;  --info-900:   #101c2a;
}
```

## セマンティックトークン

### Dark Mode（デフォルト）

| トークン名 | マッピング | 値 | 用途 |
|-----------|-----------|-----|------|
| bg-page | neutral-0 | #0c0a08 | スライド背景（Raw Umber キャンバス） |
| bg-surface | neutral-100 | #18150f | Impasto カード背景 |
| bg-surface-raised | neutral-200 | #211d16 | コードブロック背景 |
| border-default | neutral-300 | #2c2720 | カード・コードブロックのボーダー |
| text-primary | neutral-950 | #ece5d8 | 本文テキスト |
| text-secondary | neutral-700 | #8e8272 | 補助テキスト・サブタイトル |
| text-muted | neutral-500 | #524a3f | 日付・URL |
| interactive | primary-500 | #3d4f9e | 装飾番号・ブレットポイント |
| glow-effect | gold-300 | #dfbc6e | グロウエフェクト |

## カラーの使い分け

### Dark Mode

| 役割 | 値 |
|------|-----|
| 背景 | #0c0a08 + canvas texture + mesh gradient |
| テキスト primary | #ece5d8 |
| テキスト secondary | #8e8272 |
| テキスト muted | #524a3f |
| 見出し | #faf5ed (ivory white) |
| ラベル | #8b6543 (secondary-500) |
| 装飾番号 | #3d4f9e (opacity 0.3) |

背景 mesh gradient（デッキ全体に適用）:
```css
background-image:
  radial-gradient(at 15% 25%, rgba(61, 79, 158, 0.15) 0%, transparent 50%),
  radial-gradient(at 75% 65%, rgba(184, 58, 36, 0.08) 0%, transparent 45%),
  radial-gradient(at 50% 80%, rgba(204, 160, 68, 0.06) 0%, transparent 50%);
```

## タイポグラフィ

**注意: スライドでは本文 16px 未満を使わない（プロジェクション視認性）。**

| 用途 | size | weight | color | letter-spacing | font |
|------|------|--------|-------|----------------|------|
| タイトルスライド見出し | 64px | 700 | #faf5ed | -2px | Serif |
| スライド見出し | 48px | 700 | #faf5ed | -1.5px | Serif |
| カードタイトル | 28px | 600 | #faf5ed | -0.5px | Serif |
| 本文（スライド基準） | 20px | 400 | #ece5d8 | 0 | Sans |
| カード本文 | 18px | 400 | #8e8272 | 0.1px | Sans |
| ラベル(uppercase) | 14px | 600 | #8b6543 | 2px | Sans |
| 数値ハイライト(大) | 64px | 800 | #faf5ed | 0 | Sans |
| 数値ハイライト(小) | 48px | 800 | #faf5ed | 0 | Sans |
| 装飾番号 | 72px | 700 | #3d4f9e | 0, opacity 0.3 | Serif |
| サブタイトル | 28px | 400 | #8e8272 | -0.5px | Sans |
| 連絡先 | 18px | 400 | #b0a494 | 0 | Sans |
| URL (mono) | 16px | 400 | #524a3f | 0 | Mono |
| スライド番号 (mono) | 14px | 500 | #8e8272 | 0 | Mono |

テキストグラデーション（ゴールド装飾）:
```css
background: linear-gradient(90deg, #ece5d8 0%, #dfbc6e 100%);
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
```

## ボーダーラウンド

| トークン | 値 | 用途 |
|---------|-----|------|
| radius-xs | 2px | バッジ・インジケータ |
| radius-sm | 3px | 小要素・タグ |
| radius-md | 8px | カード・コードブロック・入力欄 |

**Presentation では radius-md（8px）が上限です。** これを超える border-radius は使用しません（50% の円形を除く）。

## マテリアル

### Impasto カード（厚塗り）

```css
position: relative;
background:
  url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E"),
  linear-gradient(
    145deg,
    rgba(33, 29, 22, 0.95) 0%,        /* neutral-200 */
    rgba(24, 21, 15, 0.98) 100%        /* neutral-100 */
  );
border: 1px solid rgba(223, 188, 110, 0.12);  /* gold-300 @ 12% */
border-radius: 8px;
padding: 48px 40px;
box-shadow:
  inset 0 1px 0 rgba(223, 188, 110, 0.08),    /* 上縁ゴールドハイライト */
  inset 0 -2px 4px rgba(0, 0, 0, 0.3),         /* 下部の深い影 */
  0 4px 16px rgba(0, 0, 0, 0.4),
  0 12px 40px rgba(0, 0, 0, 0.2);
```

### Glaze カード（薄塗り）

```css
background: rgba(24, 21, 15, 0.65);            /* neutral-100 @ 65% */
backdrop-filter: blur(20px) saturate(1.1);
-webkit-backdrop-filter: blur(20px) saturate(1.1);
border: 1px solid rgba(236, 229, 216, 0.05);   /* neutral-950 @ 5% */
border-radius: 8px;
padding: 48px 40px;
```

### Gold Separator（装飾区切り線）

```css
width: 100%; height: 1px;
background: linear-gradient(
  90deg,
  transparent 0%,
  rgba(223, 188, 110, 0.2) 30%,
  rgba(204, 160, 68, 0.25) 50%,
  rgba(223, 188, 110, 0.2) 70%,
  transparent 100%
);
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
  <div>LOGO</div>
  <h1>タイトル (64px/700/Serif/#faf5ed)</h1>
  <p>サブタイトル (28px/400/Sans/#8e8272)</p>
  <p>日付 (16px/mono/#524a3f)</p>
</div>
```

**2. コンテンツスライド** — 見出し + 3列カードグリッド
```html
<div class="slide" style="flex-direction: column;">
  <div style="margin-bottom: 64px;">
    <span>LABEL (14px/600/#8b6543/uppercase)</span>
    <h2>見出し (48px/700/Serif/#faf5ed)</h2>
  </div>
  <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 40px; flex: 1;">
    <div class="impasto-card">...</div>
    <div class="impasto-card">...</div>
    <div class="impasto-card">...</div>
  </div>
</div>
```

**3. 2カラムスライド** — テキスト + ビジュアル
```html
<div class="slide" style="flex-direction: column;">
  <div style="margin-bottom: 64px;">
    <h2>見出し (48px/700/Serif/#faf5ed)</h2>
  </div>
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 64px; flex: 1; align-items: center;">
    <div>テキスト + 箇条書き</div>
    <div>ビジュアル（図表・コード等）</div>
  </div>
</div>
```

**4. データスライド** — 数値ハイライト
- 数値: 64px / weight 800 / #faf5ed
- ラベル: 18px / #8e8272
- Impasto カードに内包、text-align center

### 箇条書き
```css
li { font-size: 20px; color: #b0a494; line-height: 1.6; padding-left: 24px; }
li::before { width: 8px; height: 8px; border-radius: 50%; background: #3d4f9e; }
```

### コードブロック
```css
background: #18150f; border: 1px solid #2c2720; border-radius: 8px;
padding: 32px; font-family: 'JetBrains Mono'; font-size: 16px; line-height: 1.7; color: #b0a494;
```

## スライド番号
```css
position: fixed; bottom: 32px; right: 48px;
font-family: 'JetBrains Mono'; font-size: 14px; color: #8e8272;
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
- 1スライドにカード 3枚 or 箇条書き 5項目が上限目安
- 背景色を #0c0a08 以外にしない
- スライドの padding を 64px 80px 未満にしない
- border-radius を radius-md（8px）を超えて使用しない（50% の円形を除く）
- 見出しに Sans 体を使わない（必ず Playfair Display Serif）
