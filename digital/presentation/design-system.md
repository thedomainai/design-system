# Presentation Design Rules

このファイルは AI がスライドデッキ（HTML）を生成する際に従うルールセットである。
template.html はこのルールで構築されたビジュアルリファレンスである。ブラウザで開いて見た目を確認できる。

## 基本設定

- サイズ: 1920×1080px（16:9）
- 操作: キーボード ←→ / スペースでスライド切り替え
- フォント: DM Sans (300,400,500,600) + JetBrains Mono (400,500)

```css
body {
  font-family: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  background: #000000;
  color: #e8e8ec;
  overflow: hidden;
  width: 100vw; height: 100vh;
}
```

## カラーパレット

```css
:root {
  /* ─── Primary (Steel Blue) ─── */
  --primary-50:  #eef1f8;
  --primary-100: #dae1f1;
  --primary-200: #b8c5e3;
  --primary-300: #8fa5d4;
  --primary-400: #6b84c0;
  --primary-500: #5068a4;
  --primary-600: #445076;
  --primary-700: #363f60;
  --primary-800: #292f47;
  --primary-900: #1c2035;
  --primary-950: #0f1220;

  /* ─── Secondary (Silver) ─── */
  --secondary-50:  #f9fafc;
  --secondary-100: #eef0f5;
  --secondary-200: #d7dded;
  --secondary-300: #b5bdd4;
  --secondary-400: #8f99b8;
  --secondary-500: #6e7899;
  --secondary-600: #565f7a;
  --secondary-700: #454c63;
  --secondary-800: #373c50;
  --secondary-900: #2b2f40;
  --secondary-950: #1a1d2a;

  /* ─── Neutral (Pure Black Base) ─── */
  --neutral-0:    #000000;
  --neutral-50:   #050506;
  --neutral-100:  #0a0a0c;
  --neutral-200:  #141418;
  --neutral-300:  #1e1e24;
  --neutral-400:  #2a2a32;
  --neutral-500:  #3d3d48;
  --neutral-600:  #5a5a68;
  --neutral-700:  #7e7e8c;
  --neutral-800:  #a5a5b0;
  --neutral-900:  #ccccd4;
  --neutral-950:  #e8e8ec;
  --neutral-1000: #ffffff;

  /* ─── Accent (Violet Smoke) ─── */
  --glow-50:  #f2f0fa;
  --glow-100: #e4def2;
  --glow-200: #cbc0e6;
  --glow-300: #ad9cce;
  --glow-400: #8e7cb4;
  --glow-500: #705c98;
  --glow-600: #5a4a80;
  --glow-700: #483e68;
  --glow-800: #36304f;
  --glow-900: #241e3a;
  --glow-950: #140e24;

  /* ─── Status Colors ─── */
  --success-400: #4ade80;  --success-500: #22c55e;  --success-600: #16a34a;  --success-900: #0a2615;
  --warning-400: #facc15;  --warning-500: #eab308;  --warning-600: #ca8a04;  --warning-900: #2a2008;
  --error-400:   #f87171;  --error-500:   #ef4444;  --error-600:   #dc2626;  --error-900:   #2a0a0a;
  --info-400:    #60a5fa;  --info-500:    #3b82f6;  --info-600:    #2563eb;  --info-900:    #0a1a2e;
}
```

## セマンティックトークン

### Dark Mode（デフォルト）

| トークン名 | マッピング | 値 | 用途 |
|-----------|-----------|-----|------|
| bg-page | neutral-0 | #000000 | スライド背景 |
| bg-surface | neutral-100 | #0a0a0c | Glass カード背景 |
| bg-surface-raised | neutral-200 | #141418 | コードブロック背景 |
| border-default | neutral-300 | #1e1e24 | カード・コードブロックのボーダー |
| text-primary | neutral-950 | #e8e8ec | 本文テキスト |
| text-secondary | neutral-700 | #7e7e8c | 補助テキスト・サブタイトル |
| text-muted | neutral-500 | #3d3d48 | 日付・URL |
| interactive | primary-500 | #5068a4 | 装飾番号・ブレットポイント |
| glow-effect | glow-400 | #8e7cb4 | グロウエフェクト |

### Light Mode

| トークン名 | マッピング | 値 | 用途 |
|-----------|-----------|-----|------|
| bg-page | neutral-1000 | #ffffff | スライド背景 |
| bg-surface | neutral-950 | #e8e8ec | カード背景 |
| bg-surface-raised | neutral-1000 | #ffffff | 浮上サーフェス |
| border-default | secondary-200 | #d7dded | ボーダー |
| text-primary | neutral-200 | #141418 | 本文テキスト |
| text-secondary | neutral-600 | #5a5a68 | 補助テキスト |
| text-muted | neutral-700 | #7e7e8c | 日付・URL |
| interactive | primary-500 | #5068a4 | 装飾番号・ブレットポイント |
| glow-effect | glow-300 | #ad9cce | グロウエフェクト |

## カラーの使い分け

### Dark Mode

| 役割 | 値 |
|------|-----|
| 背景 | #000000 + mesh gradient |
| テキスト primary | #e8e8ec |
| テキスト secondary | #7e7e8c |
| テキスト muted | #3d3d48 |
| 見出し | #ffffff |
| ラベル | #6b84c0 |
| 装飾番号 | #5068a4 (opacity 0.3) |

### Light Mode

| 役割 | 値 |
|------|-----|
| 背景 | #ffffff |
| テキスト primary | #141418 |
| テキスト secondary | #5a5a68 |
| テキスト muted | #7e7e8c |
| 見出し | #141418 |
| ラベル | #5068a4 |
| 装飾番号 | #5068a4 (opacity 0.3) |

### ステータスカラーの使い分け

| ステータス | Dark Mode (icon/text/bg) | Light Mode (icon/text/bg) |
|-----------|-------------------------|--------------------------|
| Success | 400 #4ade80 / 500 #22c55e / 900 #0a2615 | 600 #16a34a / 600 #16a34a / 50 #ecfdf5 |
| Warning | 400 #facc15 / 500 #eab308 / 900 #2a2008 | 600 #ca8a04 / 600 #ca8a04 / 50 #fefce8 |
| Error | 400 #f87171 / 500 #ef4444 / 900 #2a0a0a | 600 #dc2626 / 600 #dc2626 / 50 #fef2f2 |
| Info | 400 #60a5fa / 500 #3b82f6 / 900 #0a1a2e | 600 #2563eb / 600 #2563eb / 50 #eff6ff |

背景 mesh gradient（デッキ全体に適用）:
```css
background-image:
  radial-gradient(at 20% 30%, rgba(80,104,164,0.2) 0%, transparent 50%),
  radial-gradient(at 80% 70%, rgba(142,124,180,0.15) 0%, transparent 50%),
  radial-gradient(at 50% 50%, rgba(203,192,230,0.05) 0%, transparent 60%);
```

## タイポグラフィ

**注意: スライドでは本文 16px 未満を使わない（プロジェクション視認性）。**

| 用途 | size | weight | color | letter-spacing |
|------|------|--------|-------|----------------|
| タイトルスライド見出し | 56px | 300 | #ffffff | -1.5px |
| スライド見出し | 44px | 300 | #ffffff | -1px |
| カードタイトル | 28px | 400 | #ffffff | 0 |
| 本文（スライド基準） | 20px | 400 | #e8e8ec | 0 |
| カード本文 | 18px | 400 | #7e7e8c | 0 |
| ラベル(uppercase) | 14px | 600 | #6b84c0 | 2px |
| 数値ハイライト(大) | 64px | 500 | #ffffff | 0 |
| 数値ハイライト(小) | 48px | 500 | #ffffff | 0 |
| 装飾番号 | 72px | 300 | #5068a4 | 0, opacity 0.3 |
| サブタイトル | 28px | 300 | #7e7e8c | -0.5px |
| 連絡先 | 18px | 400 | #a5a5b0 | 0 |
| URL (mono) | 16px | 400 | #3d3d48 | 0 |
| スライド番号 (mono) | 14px | 500 | #7e7e8c | 0 |

テキストグラデーション:
```css
background: linear-gradient(90deg, #e8e8ec 0%, #8f99b8 100%);
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
```

## ボーダーラウンド

| トークン | 値 | 用途 |
|---------|-----|------|
| radius-xs | 2px | バッジ・インジケータ |
| radius-sm | 4px | 小要素・タグ |
| radius-md | 8px | カード・コードブロック・入力欄 |

**radius-md（8px）を超える border-radius は基本的に使用しない。** 唯一の例外は `border-radius: 50%`（円形アイコン・ブレットポイント）のみ。

## マテリアル

### Glass カード
```css
background: rgba(10, 10, 12, 0.6);
backdrop-filter: blur(24px); -webkit-backdrop-filter: blur(24px);
border: 1px solid rgba(255, 255, 255, 0.06);
border-radius: 8px;
padding: 48px 40px;
```

### Liquid Glass（強調カード）
```css
position: relative;
background: linear-gradient(135deg, rgba(80,104,164,0.08) 0%, rgba(142,124,180,0.05) 50%, rgba(80,104,164,0.08) 100%);
backdrop-filter: blur(40px) saturate(1.8) brightness(1.1);
border: 1px solid rgba(255, 255, 255, 0.12);
border-radius: 8px;
box-shadow: inset 0 1px 0 rgba(255,255,255,0.15), 0 8px 32px rgba(0,0,0,0.3);
```

### Liquid Divider（スライド内区切り線）
```css
width: 100%; height: 1px;
background: linear-gradient(90deg, transparent 0%, rgba(80,104,164,0.15) 20%, rgba(142,124,180,0.2) 50%, rgba(80,104,164,0.15) 80%, transparent 100%);
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
  <h1>タイトル (56px/300)</h1>
  <p>サブタイトル (28px/300/#7e7e8c)</p>
  <p>日付 (16px/mono/#3d3d48)</p>
</div>
```

**2. コンテンツスライド** — 見出し + 3列カードグリッド
```html
<div class="slide" style="flex-direction: column;">
  <div style="margin-bottom: 64px;">
    <span>LABEL (14px/600/#6b84c0/uppercase)</span>
    <h2>見出し (44px/300)</h2>
  </div>
  <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 40px; flex: 1;">
    <div class="glass-card">...</div>
    <div class="glass-card">...</div>
    <div class="glass-card">...</div>
  </div>
</div>
```

**3. 2カラムスライド** — テキスト + ビジュアル
```html
<div class="slide" style="flex-direction: column;">
  <div style="margin-bottom: 64px;">
    <h2>見出し (44px/300)</h2>
  </div>
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 64px; flex: 1; align-items: center;">
    <div>テキスト + 箇条書き</div>
    <div>ビジュアル（図表・コード等）</div>
  </div>
</div>
```

**4. データスライド** — 数値ハイライト
- 数値: 64px / weight 500 / #ffffff
- ラベル: 18px / #7e7e8c
- Glass カードに内包、text-align center

### 箇条書き
```css
li { font-size: 20px; color: #a5a5b0; line-height: 1.6; padding-left: 24px; }
li::before { width: 8px; height: 8px; border-radius: 50%; background: #5068a4; }
```

### コードブロック
```css
background: #0a0a0c; border: 1px solid #1e1e24; border-radius: 8px;
padding: 32px; font-family: 'JetBrains Mono'; font-size: 16px; line-height: 1.7; color: #a5a5b0;
```

## スライド番号
```css
position: fixed; bottom: 32px; right: 48px;
font-family: 'JetBrains Mono'; font-size: 14px; color: #7e7e8c;
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
- font-weight: 700 は使わない
- 1スライドにカード 3枚 or 箇条書き 5項目が上限目安
- 背景色を #000000 以外にしない
- スライドの padding を 64px 80px 未満にしない
- border-radius を radius-md（8px）を超えて使用しない（50% の円形を除く）
