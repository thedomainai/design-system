# Web UI Design Rules

このファイルは AI がウェブページ（LP・プロダクトページ等）を生成する際に従うルールセットである。
template.html はこのルールで構築されたビジュアルリファレンスである。ブラウザで開いて見た目を確認できる。

## 基本設定

```html
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
```

```css
body {
  font-family: 'DM Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  font-size: 16px;
  font-weight: 400;
  line-height: 1.6;
  color: #e8e8ec;
  background: #000000;
  -webkit-font-smoothing: antialiased;
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
| bg-page | neutral-0 | #000000 | ページ全体の背景 |
| bg-surface | neutral-100 | #0a0a0c | カード・パネル背景 |
| bg-surface-raised | neutral-200 | #141418 | 浮上サーフェス |
| border-default | neutral-300 | #1e1e24 | 通常のボーダー |
| border-hover | neutral-400 | #2a2a32 | ホバー時ボーダー |
| text-primary | neutral-950 | #e8e8ec | 本文テキスト |
| text-secondary | neutral-700 | #7e7e8c | 補助テキスト |
| text-muted | neutral-500 | #3d3d48 | 非活性テキスト |
| interactive | primary-500 | #5068a4 | ボタン・リンク |
| interactive-hover | primary-400 | #6b84c0 | ホバー状態 |
| focus-ring | primary-600 | #445076 | フォーカスインジケーター |
| glow-effect | glow-400 | #8e7cb4 | グロウエフェクト |

### Light Mode

| トークン名 | マッピング | 値 | 用途 |
|-----------|-----------|-----|------|
| bg-page | neutral-1000 | #ffffff | ページ全体の背景 |
| bg-surface | neutral-950 | #e8e8ec | カード・パネル背景 |
| bg-surface-raised | neutral-1000 | #ffffff | 浮上サーフェス |
| border-default | secondary-200 | #d7dded | 通常のボーダー |
| border-hover | secondary-300 | #b5bdd4 | ホバー時ボーダー |
| text-primary | neutral-200 | #141418 | 本文テキスト |
| text-secondary | neutral-600 | #5a5a68 | 補助テキスト |
| text-muted | neutral-700 | #7e7e8c | 非活性テキスト |
| interactive | primary-500 | #5068a4 | ボタン・リンク |
| interactive-hover | primary-600 | #445076 | ホバー状態 |
| focus-ring | primary-400 | #6b84c0 | フォーカスインジケーター |
| glow-effect | glow-300 | #ad9cce | グロウエフェクト |

## カラーの使い分け

### Dark Mode

| 役割 | 値 |
|------|-----|
| ページ背景 | #000000 |
| サーフェス（カード背景） | rgba(10,10,12,0.6) + backdrop-filter: blur(24px) |
| ボーダー通常 | rgba(255,255,255,0.06) |
| ボーダー hover | rgba(255,255,255,0.12) |
| テキスト primary（本文） | #e8e8ec |
| テキスト secondary（補助） | #7e7e8c |
| テキスト muted（非活性） | #3d3d48 |
| 見出し（h1〜h3） | #ffffff |
| ラベル・アクセント | #6b84c0 |
| インタラクティブ | #5068a4 |

### Light Mode

| 役割 | 値 |
|------|-----|
| ページ背景 | #ffffff |
| サーフェス（カード背景） | #e8e8ec |
| サーフェス浮上 | #ffffff |
| ボーダー通常 | #d7dded |
| ボーダー hover | #b5bdd4 |
| テキスト primary（本文） | #141418 |
| テキスト secondary（補助） | #5a5a68 |
| テキスト muted（非活性） | #7e7e8c |
| 見出し（h1〜h3） | #141418 |
| ラベル・アクセント | #5068a4 |
| インタラクティブ | #5068a4 |

### ステータスカラーの使い分け

| ステータス | Dark Mode (icon/text/bg) | Light Mode (icon/text/bg) |
|-----------|-------------------------|--------------------------|
| Success | 400 #4ade80 / 500 #22c55e / 900 #0a2615 | 600 #16a34a / 600 #16a34a / 50 #ecfdf5 |
| Warning | 400 #facc15 / 500 #eab308 / 900 #2a2008 | 600 #ca8a04 / 600 #ca8a04 / 50 #fefce8 |
| Error | 400 #f87171 / 500 #ef4444 / 900 #2a0a0a | 600 #dc2626 / 600 #dc2626 / 50 #fef2f2 |
| Info | 400 #60a5fa / 500 #3b82f6 / 900 #0a1a2e | 600 #2563eb / 600 #2563eb / 50 #eff6ff |

## タイポグラフィ

| 用途 | size | weight | line-height | letter-spacing | color |
|------|------|--------|-------------|----------------|-------|
| ヒーロー見出し | 56px | 300 | 1.1 | -1.5px | #ffffff |
| セクション見出し | 44px | 300 | 1.15 | -1px | #ffffff |
| ページタイトル | 36px | 300 | 1.2 | -0.5px | #ffffff |
| カードタイトル(大) | 28px | 500 | 1.3 | -0.3px | #ffffff |
| サブセクション | 22px | 500 | 1.35 | -0.2px | #ffffff |
| 小見出し | 18px | 600 | 1.4 | 0 | #e8e8ec |
| 本文（大） | 16px | 400 | 1.6 | 0 | #e8e8ec |
| 本文（標準） | 14px | 400 | 1.6 | 0 | #e8e8ec |
| 注釈 | 12px | 400 | 1.5 | 0.1px | #a5a5b0 |
| ラベル(uppercase) | 13px | 600 | — | 2px | #6b84c0 |
| サブタイトル | 20px | 400 | 1.6 | 0 | #7e7e8c |
| カード本文 | 14px | 400 | 1.6 | 0 | #7e7e8c |
| カードタイトル(小) | 20px | 600 | — | 0 | #e8e8ec |
| フッター | 13px | 400 | — | 0 | #3d3d48 |
| ナビリンク | 14px | 400 | — | 0 | #7e7e8c → hover: #e8e8ec |
| ロゴ | 20px | 600 | — | 0 | #e8e8ec |

フォント: コード・数値には `'JetBrains Mono', monospace` を使用。

テキストグラデーション（装飾用）:
```css
background: linear-gradient(90deg, #e8e8ec 0%, #8f99b8 100%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
```

## マテリアル（Glass / Liquid Glass）

### Standard Glass — カード・パネル
```css
background: rgba(10, 10, 12, 0.6);
backdrop-filter: blur(24px);
-webkit-backdrop-filter: blur(24px);
border: 1px solid rgba(255, 255, 255, 0.06);
border-radius: 12px;
```

### Frosted Glass — サイドバー・モーダル
```css
background: rgba(20, 20, 24, 0.8);
backdrop-filter: blur(40px) saturate(1.2);
-webkit-backdrop-filter: blur(40px) saturate(1.2);
border: 1px solid rgba(255, 255, 255, 0.08);
border-radius: 12px;
```

### Tinted Glass — ブランドカラー付き
```css
background: rgba(15, 18, 32, 0.7);
backdrop-filter: blur(24px);
-webkit-backdrop-filter: blur(24px);
border: 1px solid rgba(107, 132, 192, 0.15);
border-radius: 12px;
```

### Liquid Glass — ヒーロー・CTA・動的サーフェス
```css
position: relative;
background: linear-gradient(135deg, rgba(80,104,164,0.08) 0%, rgba(142,124,180,0.05) 50%, rgba(80,104,164,0.08) 100%);
backdrop-filter: blur(40px) saturate(1.8) brightness(1.1);
-webkit-backdrop-filter: blur(40px) saturate(1.8) brightness(1.1);
border: 1px solid rgba(255, 255, 255, 0.12);
border-radius: 16px;
box-shadow: inset 0 1px 0 rgba(255,255,255,0.15), inset 0 -1px 0 rgba(0,0,0,0.1), 0 8px 32px rgba(0,0,0,0.3);
```
スペキュラハイライト（::before 疑似要素）:
```css
content: "";  position: absolute;  inset: 0;  border-radius: inherit;
background: linear-gradient(180deg, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0.03) 30%, transparent 50%);
pointer-events: none;
```

### マテリアル選択ガイド
| 用途 | マテリアル |
|------|-----------|
| カード・パネル | Standard Glass |
| ヘッダー・ナビ | blur(20px) + rgba(0,0,0,0.8) |
| ヒーロー内のカード・CTA | Liquid Glass |
| サイドバー・モーダル | Frosted Glass |

## レイアウト

```css
.container { max-width: 1200px; margin: 0 auto; padding: 0 32px; }
section { padding: 96px 0; }
```

- カードグリッド: `display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px;`
- 2列グリッド: `repeat(2, 1fr); gap: 32px;`
- セクション見出し: text-align center, max-width 700px, margin 0 auto 64px
- セクション区切り線:
```css
height: 1px;
background: linear-gradient(90deg, transparent 0%, rgba(80,104,164,0.15) 20%, rgba(142,124,180,0.2) 50%, rgba(80,104,164,0.15) 80%, transparent 100%);
```

### ヘッダー
```css
header { position: fixed; top: 0; width: 100%; z-index: 1000;
  background: rgba(0,0,0,0.8); backdrop-filter: blur(20px);
  border-bottom: 1px solid rgba(255,255,255,0.06); }
nav { max-width: 1200px; margin: 0 auto; padding: 16px 32px;
  display: flex; justify-content: space-between; align-items: center; }
```

### ヒーロー
```css
.hero { min-height: 100vh; display: flex; align-items: center; padding-top: 64px; position: relative; overflow: hidden; }
```
背景（::before + ::after 疑似要素）:
```css
/* ::before — gradient-hero */
background: radial-gradient(ellipse 80% 60% at 50% 0%, rgba(80,104,164,0.15) 0%, rgba(0,0,0,0) 70%);
/* ::after — gradient-mesh */
background: radial-gradient(at 20% 30%, rgba(80,104,164,0.2) 0%, transparent 50%),
            radial-gradient(at 80% 70%, rgba(142,124,180,0.15) 0%, transparent 50%),
            radial-gradient(at 50% 50%, rgba(203,192,230,0.05) 0%, transparent 60%);
opacity: 0.5;
```

## ボタン

### Primary（Gradient Shift）— CTA
```css
padding: 14px 28px; font-size: 16px; font-weight: 600; border-radius: 8px; color: #ffffff;
background-size: 280% auto;
background-image: linear-gradient(325deg, #5068a4 0%, #798bb9 55%, #5068a4 90%);
box-shadow: 0 0 20px rgba(80,104,164,0.5), 0 5px 5px -1px rgba(68,80,118,0.25),
            inset 4px 4px 8px rgba(196,211,255,0.5), inset -4px -4px 8px rgba(54,63,96,0.35);
transition: 0.8s;
/* :hover */ background-position: right top; transform: translateY(-2px);
/* :focus-visible */ box-shadow: 0 0 0 3px #fff, 0 0 0 6px #5068a4;
```

### Secondary（Glow Line）— 補助アクション
```css
padding: 14px 28px; border-radius: 7px; color: rgba(232,232,236,0.66);
background: radial-gradient(ellipse at bottom, #2a2a32 0%, #0a0a0c 45%);
box-shadow: inset 0 0 0 1px rgba(255,255,255,0.1);
transition: all 1s cubic-bezier(0.15, 0.83, 0.66, 1);
/* ::before — 底辺グロウライン */
width: 70%; height: 1px; bottom: 0; left: 15%;
background: linear-gradient(90deg, transparent, #e8e8ec, transparent); opacity: 0.2;
/* :hover */ color: #e8e8ec; transform: scale(1.05) translateY(-2px); /* ::before opacity: 1 */
```

### Ghost（Liquid Hover）— 最小限
```css
padding: 14px 28px; border-radius: 12px; color: #e8e8ec;
background: rgba(10,10,12,0.5); backdrop-filter: blur(20px) saturate(1.4);
border: 1px solid rgba(255,255,255,0.1); overflow: hidden;
/* ::before — スペキュラスライド */
top: -100%; background: linear-gradient(180deg, rgba(255,255,255,0.12), transparent);
/* :hover */ border-color: rgba(255,255,255,0.18); background: rgba(80,104,164,0.15);
  box-shadow: inset 0 1px 0 rgba(255,255,255,0.15), 0 8px 24px rgba(0,0,0,0.3);
  /* ::before top: 0 */
```

## カード

```css
background: rgba(10,10,12,0.6); backdrop-filter: blur(24px);
border: 1px solid rgba(255,255,255,0.06); border-radius: 12px; padding: 32px;
/* :hover */ transform: translateY(-4px); border-color: rgba(255,255,255,0.12);
```

アイコン領域: 48x48px, border-radius 8px, background rgba(80,104,164,0.15)

## バッジ

```css
height: 22px; padding: 0 8px; font-size: 11px; font-weight: 500; border-radius: 4px;
/* default */ background: #1e1e24; color: #7e7e8c;
/* success */ background: #0a2615; color: #4ade80;
/* warning */ background: #2a2008; color: #facc15;
/* error */   background: #2a0a0a; color: #f87171;
/* info */    background: #0a1a2e; color: #60a5fa;
```

## 入力フィールド

```css
height: 40px; padding: 0 12px; font-size: 14px; color: #e8e8ec;
background: #0a0a0c; border: 1px solid #1e1e24; border-radius: 8px;
/* ::placeholder */ color: #3d3d48;
/* :hover */ border-color: #2a2a32;
/* :focus */ border-color: #5068a4; box-shadow: 0 0 0 2px rgba(68,80,118,0.6), 0 0 12px rgba(80,104,164,0.3);
```

## アニメーション

```css
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(8px); }
  to   { opacity: 1; transform: translateY(0); }
}
@keyframes glowPulse {
  0%, 100% { box-shadow: 0 0 20px rgba(80,104,164,0.1); }
  50%      { box-shadow: 0 0 40px rgba(80,104,164,0.25); }
}
```

## レスポンシブ

| ブレークポイント | 変更 |
|-----------------|------|
| max-width: 1023px | グリッド→2列、ヒーロー min-height auto、見出し縮小(40px/32px)、section padding 64px |
| max-width: 639px | グリッド→1列、container padding 16px、見出し縮小(32px/28px)、ナビ非表示、section padding 48px |

## ページ構造（HTML）

```html
<header>
  <nav>
    <a class="logo">...</a>
    <div class="nav-links"><a>...</a> ... </div>
  </nav>
</header>
<section class="hero">
  <div class="container">
    <div class="hero-content">
      <span class="label">LABEL</span>
      <h1>...</h1>
      <p class="hero-subtitle">...</p>
      <div class="hero-cta"><a class="btn btn-primary">...</a></div>
    </div>
  </div>
</section>
<div class="section-separator"></div>
<section>
  <div class="container">
    <div class="section-header">
      <span class="label">LABEL</span>
      <h2>...</h2>
      <p>...</p>
    </div>
    <div class="grid-3">
      <div class="card">...</div>
      ...
    </div>
  </div>
</section>
<footer>
  <div class="container">...</div>
</footer>
```

## 禁止事項

- font-weight: 700 は使わない（最大 600）
- 見出しに #e8e8ec より暗い色を使わない（見出しは #ffffff）
- border-radius を 12px より大きくしない（Liquid Glass の 16px、ピル型ボタンは例外）
- `!important` は使わない
- セクション間余白を 64px 未満にしない
- カード padding を 24px 未満にしない
