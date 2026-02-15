# The Domain AI Company Design System

The Domain AI Company のダークファーストデザインシステムです。
Glassmorphism・Liquid Glass の 2 つのマテリアルを基盤に、漆黒の中に浮かぶ光と透明感で情報階層を表現します。
Web Page / Web App / Mobile App / Visual Presentation の全アウトプットで統一的に使用します。

## 1. Design Principles

| # | 原則 | 説明 |
|---|------|------|
| 1 | **Dark-First** | 漆黒を基調に、光の濃淡とマテリアルの透過度で情報の重みを伝える |
| 2 | **Minimal & Precise** | 余白と抑制された要素数で、コンテンツそのものに没入させる |
| 3 | **Two Materials** | Glassmorphism（静）・Liquid Glass（動）の 2 層で奥行きと質感を構成する |
| 4 | **Systematic Consistency** | すべての値はトークンから導出し、マジックナンバーを排除する |
| 5 | **Platform Adaptive** | 共通トークンを持ちつつ、各プラットフォームの慣習に従う |


## 2. Color System

### 2.1 Color Palette

カラー定義の原本は `color-palette-thedomainai.html` を参照してください。

#### Primary — Steel Blue

知性・テクノロジーを表現するメインカラーです。

| Token | Hex | 用途 |
|-------|-----|------|
| `primary-50` | `#eef1f8` | ライトモード背景・ホバー |
| `primary-100` | `#dae1f1` | ライトモード薄い背景 |
| `primary-200` | `#b8c5e3` | サブテキスト（ライト） |
| `primary-300` | `#8fa5d4` | アイコン・装飾（ライト） |
| `primary-400` | `#6b84c0` | インタラクティブ hover |
| `primary-500` | `#5068a4` | **インタラクティブ default** |
| `primary-600` | `#445076` | フォーカスリング・押下時 |
| `primary-700` | `#363f60` | 濃いアクセント |
| `primary-800` | `#292f47` | カード背景（ダーク） |
| `primary-900` | `#1c2035` | セクション背景（ダーク） |
| `primary-950` | `#0f1220` | 最深背景 |

#### Secondary — Silver

テキスト・補助要素に使用するニュートラルブルーです。

| Token | Hex | 用途 |
|-------|-----|------|
| `secondary-50` | `#f9fafc` | ライトモード最明色 |
| `secondary-100` | `#eef0f5` | ライトモード背景 |
| `secondary-200` | `#d7dded` | ボーダー（ライト） |
| `secondary-300` | `#b5bdd4` | プレースホルダ |
| `secondary-400` | `#8f99b8` | 補助テキスト |
| `secondary-500` | `#6e7899` | セカンダリテキスト |
| `secondary-600` | `#565f7a` | ラベル |
| `secondary-700` | `#454c63` | 非アクティブ要素 |
| `secondary-800` | `#373c50` | サーフェス（ダーク） |
| `secondary-900` | `#2b2f40` | ボーダー強調（ダーク） |
| `secondary-950` | `#1a1d2a` | 深いサーフェス |

#### Accent — Violet Smoke

グロウエフェクト・ハイライトに使用するバイオレット系カラーです。`#36304f` をベースに色相 252° で構成しています。

| Token | Hex | 用途 |
|-------|-----|------|
| `glow-50` | `#f2f0fa` | グロウハイライト最明 |
| `glow-100` | `#e4def2` | グロウハイライト |
| `glow-200` | `#cbc0e6` | **グロウエフェクト基準色** |
| `glow-300` | `#ad9cce` | グロウ減衰 |
| `glow-400` | `#8e7cb4` | グロウサブ |
| `glow-500` | `#705c98` | 装飾アイコン |
| `glow-600` | `#5a4a80` | ボーダーグロウ |
| `glow-700` | `#483e68` | サーフェスアクセント |
| `glow-800` | `#36304f` | **ベースカラー**・深いサーフェス |
| `glow-900` | `#241e3a` | オーバーレイ |
| `glow-950` | `#140e24` | 最深アクセント |

#### Neutral — Black Scale

背景・テキスト・ボーダーを構成するピュアブラックベーススケールです。

| Token | Hex | 輝度目安 | 用途 |
|-------|-----|----------|------|
| `neutral-0` | `#000000` | 0% | 最深背景・ページ背景 |
| `neutral-50` | `#050506` | 2% | 微差レイヤー |
| `neutral-100` | `#0a0a0c` | 4% | サーフェス |
| `neutral-200` | `#141418` | 8% | サーフェス（浮上） |
| `neutral-300` | `#1e1e24` | 12% | ボーダー default |
| `neutral-400` | `#2a2a32` | 16% | ボーダー hover |
| `neutral-500` | `#3d3d48` | 24% | テキスト muted |
| `neutral-600` | `#5a5a68` | 35% | セパレーター |
| `neutral-700` | `#7e7e8c` | 50% | テキスト secondary |
| `neutral-800` | `#a5a5b0` | 65% | テキスト sub |
| `neutral-900` | `#ccccd4` | 80% | テキスト default（ライト系） |
| `neutral-950` | `#e8e8ec` | 91% | **テキスト primary** |
| `neutral-1000` | `#ffffff` | 100% | 純白（見出し・強調） |

### 2.2 Semantic Tokens

用途に基づく意味的トークンです。実装時はこちらを優先して使用します。

| Semantic Token | Maps To | Hex | 用途 |
|----------------|---------|-----|------|
| `bg-page` | neutral-0 | `#000000` | ページ全体の背景 |
| `bg-surface` | neutral-100 | `#0a0a0c` | カード・パネル背景 |
| `bg-surface-raised` | neutral-200 | `#141418` | 浮上サーフェス（モーダル等） |
| `border-default` | neutral-300 | `#1e1e24` | 通常のボーダー |
| `border-hover` | neutral-400 | `#2a2a32` | ホバー時のボーダー |
| `text-primary` | neutral-950 | `#e8e8ec` | 本文テキスト |
| `text-secondary` | neutral-700 | `#7e7e8c` | 補助テキスト |
| `text-muted` | neutral-500 | `#3d3d48` | 非活性・ヒントテキスト |
| `interactive` | primary-500 | `#5068a4` | ボタン・リンク |
| `interactive-hover` | primary-400 | `#6b84c0` | ホバー状態 |
| `focus-ring` | primary-600 | `#445076` | フォーカスインジケーター |
| `glow-effect` | glow-400 | `#8e7cb4` | グロウエフェクト |

### 2.3 Light Mode Semantic Tokens

ダークモードのトークンと対になるライトモード用の意味的トークンです。同じセマンティック名を使い、テーマ切り替え時に値を差し替えます。

| Semantic Token | Maps To (Light) | Hex | 用途 |
|----------------|-----------------|-----|------|
| `bg-page` | neutral-1000 | `#ffffff` | ページ全体の背景 |
| `bg-surface` | neutral-950 | `#e8e8ec` | カード・パネル背景 |
| `bg-surface-raised` | neutral-1000 | `#ffffff` | 浮上サーフェス（モーダル等） |
| `border-default` | secondary-200 | `#d7dded` | 通常のボーダー |
| `border-hover` | secondary-300 | `#b5bdd4` | ホバー時のボーダー |
| `text-primary` | neutral-200 | `#141418` | 本文テキスト |
| `text-secondary` | neutral-600 | `#5a5a68` | 補助テキスト |
| `text-muted` | neutral-700 | `#7e7e8c` | 非活性・ヒントテキスト |
| `interactive` | primary-500 | `#5068a4` | ボタン・リンク |
| `interactive-hover` | primary-600 | `#445076` | ホバー状態 |
| `focus-ring` | primary-400 | `#6b84c0` | フォーカスインジケーター |
| `glow-effect` | glow-300 | `#ad9cce` | グロウエフェクト |

- `interactive` は Dark / Light で同じ primary-500 を使用し、ブランドカラーの一貫性を保ちます。
- ステータスカラーはライトモードでは **600** をテキストに、**50 相当の薄い背景**をバッジに使用します。

### 2.4 Status Colors

| Status | 400（明） | 500（基準） | 600（暗） | 900（bg） |
|--------|-----------|------------|-----------|-----------|
| **Success** | `#4ade80` | `#22c55e` | `#16a34a` | `#0a2615` |
| **Warning** | `#facc15` | `#eab308` | `#ca8a04` | `#2a2008` |
| **Error** | `#f87171` | `#ef4444` | `#dc2626` | `#2a0a0a` |
| **Info** | `#60a5fa` | `#3b82f6` | `#2563eb` | `#0a1a2e` |

- ステータスカラーの **500** をアイコン・テキストに、**900** をバッジ背景に使用します。
- ダークUI上では **400** を使うとコントラスト比が確保しやすくなります。


## 3. Typography

### 3.1 Font Family

| Role | Font | Fallback | 用途 |
|------|------|----------|------|
| **Sans** | DM Sans | -apple-system, sans-serif | 本文・UI全般 |
| **Mono** | JetBrains Mono | SF Mono, monospace | コード・数値・トークン表示 |

```
--font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-mono: 'JetBrains Mono', 'SF Mono', 'Fira Code', monospace;
```

### 3.2 Type Scale

8px をベースに Major Third (1.25) スケールで構成します。

| Token | Size | Weight | Line Height | Letter Spacing | 用途 |
|-------|------|--------|-------------|----------------|------|
| `display-xl` | 56px / 3.5rem | 300 | 1.1 | -1.5px | ヒーロー見出し |
| `display-lg` | 44px / 2.75rem | 300 | 1.15 | -1px | セクション見出し |
| `display-md` | 36px / 2.25rem | 300 | 1.2 | -0.5px | ページタイトル |
| `heading-lg` | 28px / 1.75rem | 500 | 1.3 | -0.3px | カードタイトル |
| `heading-md` | 22px / 1.375rem | 500 | 1.35 | -0.2px | サブセクション |
| `heading-sm` | 18px / 1.125rem | 600 | 1.4 | 0 | 小見出し |
| `body-lg` | 16px / 1rem | 400 | 1.6 | 0 | 本文（大） |
| `body-md` | 14px / 0.875rem | 400 | 1.6 | 0 | **本文（基準）** |
| `body-sm` | 12px / 0.75rem | 400 | 1.5 | 0.1px | 注釈・キャプション |
| `label-lg` | 14px / 0.875rem | 600 | 1.2 | 0.5px | ボタンラベル |
| `label-md` | 13px / 0.8125rem | 600 | 1.2 | 2px | セクションラベル（uppercase） |
| `label-sm` | 11px / 0.6875rem | 500 | 1.2 | 1.5px | タグ・バッジ |
| `mono-md` | 13px / 0.8125rem | 400 | 1.7 | 0 | コードブロック |
| `mono-sm` | 11px / 0.6875rem | 400 | 1.5 | 0 | インラインコード |

### 3.3 Font Weight

| Token | Weight | 用途 |
|-------|--------|------|
| `light` | 300 | Display 見出し（ヒーロー・セクション見出しの装飾的な軽さ） |
| `regular` | 400 | 本文・説明テキスト |
| `medium` | 500 | 強調テキスト・Heading（heading-lg, heading-md） |
| `semibold` | 600 | ラベル・ボタン・小見出し（heading-sm, label-lg, label-md） |
| `bold` | 700 | カードタイトル・ナビゲーションのアクティブ状態・強調見出し |
| `extrabold` | 800 | ヒーローのキーワード強調・KPI数値・プライシングの価格表示 |
| `black` | 900 | ブランドロゴタイプ・インパクト見出し・1〜2語の最大強調 |

#### Weight 選択ガイド

| ユースケース | 推奨 Weight | 例 |
|-------------|------------|-----|
| ヒーロー見出し全体 | 300 (light) | "Dark-First Design System" |
| ヒーロー内のキーワード強調 | 800 (extrabold) | "Dark-First **Design System**" |
| セクション見出し | 300 (light) または 600 (semibold) | コンテキストに応じて使い分け |
| カードタイトル | 700 (bold) | "Standard Glass" |
| 本文中の強調 | 600 (semibold) | "すべての値は**トークン**から導出" |
| KPI・メトリクス数値 | 800 (extrabold) | "$12.5M" "99.9%" |
| ブランドロゴ・最大強調 | 900 (black) | "THE DOMAIN AI" |
| ボタンラベル | 600 (semibold) | "Get Started" |
| ナビゲーション（通常） | 400 (regular) | サイドバーリンク |
| ナビゲーション（アクティブ） | 700 (bold) | 選択中のリンク |
| バッジ・タグ | 500 (medium) | "Success" "v2.0" |

> **注意**: DM Sans は 100〜1000 の可変ウェイトに対応しています。Google Fonts 読み込み時に必要な weight を含めてください。
> ```html
> <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
> ```


## 4. Spacing

8px グリッドベースのスペーシングスケールです。

| Token | Value | 用途例 |
|-------|-------|--------|
| `space-0` | 0px | — |
| `space-1` | 2px | インラインギャップ最小 |
| `space-2` | 4px | アイコンとラベルの間 |
| `space-3` | 8px | コンパクトなパディング |
| `space-4` | 12px | ボタン内パディング |
| `space-5` | 16px | カード内パディング・要素間 |
| `space-6` | 24px | セクション内余白 |
| `space-7` | 32px | セクション間余白 |
| `space-8` | 48px | セクション区切り |
| `space-9` | 64px | ページセクション間 |
| `space-10` | 96px | ヒーロー余白 |
| `space-11` | 128px | ページ上下マージン |


## 5. Grid & Layout

### 5.1 Breakpoints

| Token | Width | 主な対象 |
|-------|-------|----------|
| `bp-mobile` | 0–639px | Mobile（縦） |
| `bp-tablet` | 640–1023px | Tablet / Mobile横 |
| `bp-desktop` | 1024–1439px | Desktop 標準 |
| `bp-wide` | 1440px+ | Desktop ワイド |

### 5.2 Grid System

| Context | Columns | Gutter | Margin | Max Width |
|---------|---------|--------|--------|-----------|
| **Mobile** | 4 | 16px | 16px | 100% |
| **Tablet** | 8 | 24px | 32px | 100% |
| **Desktop** | 12 | 24px | auto | 1200px |
| **Wide** | 12 | 32px | auto | 1440px |
| **Presentation** | 自由 | — | 48px+ | 1920×1080 |

### 5.3 Container

```
--container-sm:   640px   /* 記事・フォーム */
--container-md:   960px   /* ダッシュボード */
--container-lg:  1200px   /* メインレイアウト */
--container-xl:  1440px   /* ワイドレイアウト */
```


## 6. Shape & Radius

### 6.1 Border Radius

| Token | Value | 用途 |
|-------|-------|------|
| `radius-none` | 0px | 角丸なし |
| `radius-sm` | 4px | タグ・バッジ・チップ |
| `radius-md` | 8px | ボタン・インプット |
| `radius-lg` | 12px | カード・パネル |
| `radius-xl` | 16px | モーダル・ダイアログ |
| `radius-2xl` | 24px | ピル型ボタン・大型カード |
| `radius-full` | 9999px | アバター・完全ピル |

基本方針: **12px（`radius-lg`）** をカードの標準とし、ネスト要素は親より小さい radius を使用します。

### 6.2 Border & Stroke Width

| Token | Value | 用途 |
|-------|-------|------|
| `stroke-hairline` | 0.5px | 微細なセパレーター・装飾線 |
| `stroke-sm` | 1px | **ボーダー default**・カード境界・セパレーター |
| `stroke-md` | 1.5px | アイコンストローク・強調ボーダー |
| `stroke-lg` | 2px | フォーカスリング・アクティブ状態のボーダー |
| `stroke-xl` | 3px | 強い視覚的強調・装飾的アンダーライン |

基本方針: **1px（`stroke-sm`）** をデフォルトのボーダー幅とします。アイコンは **1.5px（`stroke-md`）** で統一します。


## 7. Material System

本デザインシステムの視覚表現を支える 2 つのマテリアルと、それらを補完するエフェクト群です。

### 7.1 Material Philosophy

2 つのマテリアルは、それぞれ異なる質感と役割を持ちます。漆黒のキャンバスの上に「霜 → 水面」という光の進化で、情報の階層と重要度を直感的に伝えます。

| Material | メタファー | 特性 | 主な用途 |
|----------|-----------|------|----------|
| **Glassmorphism** | 磨りガラス | 均一なブラー、柔らかい透過、静的な佇まい | カード、パネル、サイドバー、オーバーレイ |
| **Liquid Glass** | 水面・液体 | コンテンツ追従ティンティング、スペキュラハイライト、有機的な揺らぎ | ナビゲーション、ヒーロー、インタラクティブサーフェス |

```
光の進化: Frost ─── Flow
          静寂      流動

           Glassmorphism    Liquid Glass
           ─────────────    ────────────
 透過度     均一・高い        動的・中程度
 ブラー     強い (24-40px)   中程度 (20-40px)
 ボーダー   白の微線          スペキュラ上縁
 動き       なし             ティンティング
 輝度       抑制的           環境追従
```

#### Material Selection Guide

| ユースケース | 推奨マテリアル | 理由 |
|-------------|--------------|------|
| コンテンツカード | Glassmorphism | 読みやすさ優先、背景を穏やかに透過 |
| アプリヘッダー | Liquid Glass | スクロール時にコンテンツが溶け込む動的効果 |
| サイドバー | Glassmorphism (frosted) | 安定した視認性、主役はコンテンツ領域 |
| ヒーローセクション | Liquid Glass | 背景メッシュとの有機的な融合 |
| CTA ボタン | Liquid Glass | スペキュラハイライトで視線を引きつける |
| 料金カード（推奨プラン） | Liquid Glass (deep) | 深いティンティングで他プランと差別化 |
| モーダル・ダイアログ | Glassmorphism | 落ち着いた背景分離 |
| ツールチップ | Liquid Glass | 軽量かつコンテンツ追従する自然な佇まい |

#### 枠線と中塗りの使い分け

枠線（border/stroke）と中塗り（background fill）は基本的に併用しない。

- **併用可能な例外**: 中塗りが十分に薄く（低 opacity）、同系統の色で枠線を引く場合のみ許可（例: Glass カードの半透明背景 + 同系統の微細ボーダー）

### 7.2 Glassmorphism

磨りガラスのように背景を柔らかくぼかし、静的で落ち着いた透過面を構成します。
情報を読み取るサーフェスの基本マテリアルです。

```css
/* ─── Dark Mode ─── */

/* Standard Glass — カード・パネルの基本 */
.glass {
  background: rgba(10, 10, 12, 0.6);       /* neutral-100 @ 60% */
  backdrop-filter: blur(24px);
  -webkit-backdrop-filter: blur(24px);
  border: 1px solid rgba(255, 255, 255, 0.06);
}

/* Frosted Glass — より強い曇りで背景を遮断 */
.glass-frosted {
  background: rgba(20, 20, 24, 0.8);       /* neutral-200 @ 80% */
  backdrop-filter: blur(40px) saturate(1.2);
  -webkit-backdrop-filter: blur(40px) saturate(1.2);
  border: 1px solid rgba(255, 255, 255, 0.08);
}

/* Tinted Glass — ブランドカラーを帯びた Glass */
.glass-tinted {
  background: rgba(15, 18, 32, 0.7);       /* primary-950 @ 70% */
  backdrop-filter: blur(24px);
  -webkit-backdrop-filter: blur(24px);
  border: 1px solid rgba(107, 132, 192, 0.15);  /* primary-400 @ 15% */
}

/* Violet Glass — アクセントカラーの Glass */
.glass-violet {
  background: rgba(36, 30, 58, 0.6);       /* glow-900 @ 60% */
  backdrop-filter: blur(24px) saturate(1.3);
  -webkit-backdrop-filter: blur(24px) saturate(1.3);
  border: 1px solid rgba(142, 124, 180, 0.12);  /* glow-400 @ 12% */
}

/* ─── Light Mode ─── */

/* Light Glass — ライトモード・LP ヒーロー */
.glass-light {
  background: rgba(218, 225, 241, 0.5);    /* primary-100 @ 50% */
  backdrop-filter: blur(24px);
  -webkit-backdrop-filter: blur(24px);
  border: 1px solid rgba(255, 255, 255, 0.6);
}

/* Light Frosted Glass — ライトモード・カード */
.glass-light-frosted {
  background: rgba(238, 240, 245, 0.6);    /* secondary-100 @ 60% */
  backdrop-filter: blur(40px) saturate(1.3);
  -webkit-backdrop-filter: blur(40px) saturate(1.3);
  border: 1px solid rgba(255, 255, 255, 0.7);
}

/* Light Violet Glass — ライトモード・アクセント */
.glass-light-violet {
  background: rgba(228, 222, 242, 0.5);    /* glow-100 @ 50% */
  backdrop-filter: blur(24px);
  -webkit-backdrop-filter: blur(24px);
  border: 1px solid rgba(173, 156, 206, 0.2);  /* glow-300 @ 20% */
}
```

### 7.3 Liquid Glass

Apple Liquid Glass にインスパイアされた動的マテリアルです。
背景コンテンツに応じてティンティングが変化し、上縁にスペキュラハイライト（光沢の帯）が走ることで、水面のような生きた透明感を生み出します。

```css
/* ─── Dark Mode ─── */

/* Liquid Glass — Base */
.liquid-glass {
  position: relative;
  background: linear-gradient(
    135deg,
    rgba(80, 104, 164, 0.08) 0%,     /* primary-500 tint */
    rgba(142, 124, 180, 0.05) 50%,   /* glow-400 tint */
    rgba(80, 104, 164, 0.08) 100%
  );
  backdrop-filter: blur(40px) saturate(1.8) brightness(1.1);
  -webkit-backdrop-filter: blur(40px) saturate(1.8) brightness(1.1);
  border: 1px solid rgba(255, 255, 255, 0.12);
  border-radius: 16px;
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.15),   /* specular top edge */
    inset 0 -1px 0 rgba(0, 0, 0, 0.1),          /* bottom shadow */
    0 8px 32px rgba(0, 0, 0, 0.3);
}

/* Liquid Glass — Specular Highlight Overlay */
.liquid-glass::before {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0.1) 0%,
    rgba(255, 255, 255, 0.03) 30%,
    transparent 50%
  );
  pointer-events: none;
}

/* Liquid Glass — Deep (ヘッダー・ナビゲーション用) */
.liquid-glass-deep {
  position: relative;
  background: linear-gradient(
    135deg,
    rgba(15, 18, 32, 0.4) 0%,       /* primary-950 */
    rgba(54, 48, 79, 0.2) 50%,      /* glow-800 */
    rgba(15, 18, 32, 0.4) 100%
  );
  backdrop-filter: blur(60px) saturate(2.0) brightness(0.95);
  -webkit-backdrop-filter: blur(60px) saturate(2.0) brightness(0.95);
  border: 1px solid rgba(142, 124, 180, 0.1);
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.08),
    0 16px 48px rgba(0, 0, 0, 0.4);
}

/* Liquid Glass — Subtle (ツールチップ・ポップオーバー用) */
.liquid-glass-subtle {
  position: relative;
  background: rgba(10, 10, 12, 0.5);
  backdrop-filter: blur(30px) saturate(1.6);
  -webkit-backdrop-filter: blur(30px) saturate(1.6);
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow:
    inset 0 0.5px 0 rgba(255, 255, 255, 0.1),
    0 4px 16px rgba(0, 0, 0, 0.3);
}

/* ─── Light Mode ─── */

/* Liquid Glass — Light */
.liquid-glass-light {
  position: relative;
  background: linear-gradient(
    135deg,
    rgba(218, 225, 241, 0.3) 0%,    /* primary-100 */
    rgba(228, 222, 242, 0.2) 50%,   /* glow-100 */
    rgba(218, 225, 241, 0.3) 100%
  );
  backdrop-filter: blur(40px) saturate(1.6) brightness(1.15);
  -webkit-backdrop-filter: blur(40px) saturate(1.6) brightness(1.15);
  border: 1px solid rgba(255, 255, 255, 0.5);
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.6),
    0 8px 32px rgba(80, 104, 164, 0.1);
}

/* Liquid Glass — Light Deep */
.liquid-glass-light-deep {
  position: relative;
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0.7) 0%,
    rgba(238, 240, 245, 0.5) 100%
  );
  backdrop-filter: blur(60px) saturate(1.8) brightness(1.1);
  -webkit-backdrop-filter: blur(60px) saturate(1.8) brightness(1.1);
  border: 1px solid rgba(255, 255, 255, 0.8);
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.9),
    0 12px 40px rgba(80, 104, 164, 0.08);
}
```

### 7.4 Gradients

```css
/* ─── Dark Mode ─── */

/* Hero Gradient — メインビジュアル背景 */
--gradient-hero: radial-gradient(
  ellipse 80% 60% at 50% 0%,
  rgba(80, 104, 164, 0.15) 0%,    /* primary-500 */
  rgba(0, 0, 0, 0) 70%
);

/* Surface Gradient — カード・パネル背景 */
--gradient-surface: linear-gradient(
  180deg,
  rgba(30, 30, 36, 0.5) 0%,       /* neutral-300 */
  rgba(10, 10, 12, 0.8) 100%      /* neutral-100 */
);

/* Glow Gradient — CTA・アクセント */
--gradient-glow: linear-gradient(
  135deg,
  #5068a4 0%,                      /* primary-500 */
  #8e7cb4 50%,                     /* glow-400 */
  #cbc0e6 100%                     /* glow-200 */
);

/* Text Gradient — 見出し装飾 */
--gradient-text: linear-gradient(
  90deg,
  #e8e8ec 0%,                      /* neutral-950 */
  #8f99b8 100%                     /* secondary-400 */
);

/* Mesh Gradient — ヒーロー・プレゼン背景 */
--gradient-mesh:
  radial-gradient(at 20% 30%, rgba(80, 104, 164, 0.2) 0%, transparent 50%),
  radial-gradient(at 80% 70%, rgba(142, 124, 180, 0.15) 0%, transparent 50%),
  radial-gradient(at 50% 50%, rgba(203, 192, 230, 0.05) 0%, transparent 60%);

/* Liquid Gradient — Liquid Glass の下地 */
--gradient-liquid: linear-gradient(
  135deg,
  rgba(80, 104, 164, 0.1) 0%,
  rgba(142, 124, 180, 0.06) 50%,
  rgba(80, 104, 164, 0.1) 100%
);

/* ─── Light Mode ─── */

/* Light Hero Gradient */
--gradient-hero-light: radial-gradient(
  ellipse 80% 60% at 50% 0%,
  rgba(218, 225, 241, 0.6) 0%,    /* primary-100 */
  rgba(255, 255, 255, 0) 70%
);

/* Light Surface Gradient */
--gradient-surface-light: linear-gradient(
  180deg,
  rgba(238, 240, 245, 0.8) 0%,    /* secondary-100 */
  rgba(255, 255, 255, 0.9) 100%
);

/* Light Violet Gradient */
--gradient-violet-light: linear-gradient(
  135deg,
  #dae1f1 0%,                      /* primary-100 */
  #e4def2 50%,                     /* glow-100 */
  #eef0f5 100%                     /* secondary-100 */
);

/* Light Mesh Gradient */
--gradient-mesh-light:
  radial-gradient(at 20% 30%, rgba(218, 225, 241, 0.4) 0%, transparent 50%),
  radial-gradient(at 80% 70%, rgba(228, 222, 242, 0.3) 0%, transparent 50%),
  radial-gradient(at 50% 50%, rgba(238, 240, 245, 0.2) 0%, transparent 60%);
```

### 7.5 Glow Effects

#### Basic — box-shadow ベース

要素に `box-shadow` で適用する発光エフェクトです。ホバー・フォーカスなど状態変化に伴う輝きに使用します。

```css
/* Subtle Glow — ホバー・フォーカス */
--glow-subtle: 0 0 20px rgba(80, 104, 164, 0.15);

/* Medium Glow — CTA・アクティブ要素 */
--glow-medium: 0 0 40px rgba(80, 104, 164, 0.25),
               0 0 80px rgba(142, 124, 180, 0.1);

/* Strong Glow — ヒーロー・アクセント */
--glow-strong: 0 0 60px rgba(80, 104, 164, 0.3),
               0 0 120px rgba(203, 192, 230, 0.1),
               0 0 200px rgba(142, 124, 180, 0.05);

/* Liquid Glow — Liquid Glass 用の拡散エフェクト */
--glow-liquid: 0 0 30px rgba(80, 104, 164, 0.12),
               0 8px 40px rgba(0, 0, 0, 0.2);

/* Glow Ring — フォーカスインジケーター */
--glow-ring: 0 0 0 2px rgba(68, 80, 118, 0.6),
             0 0 12px rgba(80, 104, 164, 0.3);
```

#### Gradients — background ベース

要素の背景や `::after` 疑似要素に `background-image` として適用するグラデーショングロウです。
静的な装飾や環境光の演出に使用します。

```css
/* Radial Glow — 要素中心からのオーラ状の輝き */
--glow-gradient-radial: radial-gradient(
  ellipse 60% 60% at 50% 50%,
  rgba(80, 104, 164, 0.15) 0%,
  transparent 70%
);

/* Edge Glow — 上縁からの方向性グロウ */
--glow-gradient-edge: linear-gradient(
  180deg,
  rgba(80, 104, 164, 0.2) 0%,
  rgba(142, 124, 180, 0.05) 30%,
  transparent 60%
);

/* Ambient Glow — 複数のラディアルを重ねた環境光 */
--glow-gradient-ambient:
  radial-gradient(at 20% 30%, rgba(80, 104, 164, 0.12) 0%, transparent 50%),
  radial-gradient(at 80% 70%, rgba(142, 124, 180, 0.08) 0%, transparent 50%);

/* Violet Glow — アクセントカラーの拡散グロウ */
--glow-gradient-violet: radial-gradient(
  ellipse 50% 50% at 50% 50%,
  rgba(142, 124, 180, 0.15) 0%,
  rgba(203, 192, 230, 0.05) 40%,
  transparent 70%
);
```

### 7.6 Shadows (Elevation)

ダークUIでは影よりも「明るさの差」と「ボーダー」で高さを表現します。
Liquid Glass では `inset` シャドウによるスペキュラ表現が主要な高さの手がかりとなります。

| Token | Value | 用途 |
|-------|-------|------|
| `shadow-sm` | `0 1px 2px rgba(0,0,0,0.5)` | 微小な浮き |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.4)` | カード・ドロップダウン |
| `shadow-lg` | `0 8px 32px rgba(0,0,0,0.5)` | モーダル・ポップオーバー |
| `shadow-xl` | `0 16px 48px rgba(0,0,0,0.6)` | フルスクリーンオーバーレイ |

### 7.7 Decorative Lines & Separators

```css
/* Standard Separator */
--separator: 1px solid var(--neutral-300);   /* #1e1e24 */

/* Glowing Separator */
--separator-glow: 1px solid rgba(107, 132, 192, 0.2);

/* Gradient Line — セクション区切り */
--line-gradient: linear-gradient(
  90deg,
  transparent 0%,
  rgba(107, 132, 192, 0.3) 50%,
  transparent 100%
);

/* Liquid Line — Liquid Glass セクション区切り */
--line-liquid: linear-gradient(
  90deg,
  transparent 0%,
  rgba(80, 104, 164, 0.15) 20%,
  rgba(142, 124, 180, 0.2) 50%,
  rgba(80, 104, 164, 0.15) 80%,
  transparent 100%
);
```


## 8. Elevation & Layers

| Token | z-index | 用途 |
|-------|---------|------|
| `z-base` | 0 | 通常コンテンツ |
| `z-raised` | 10 | スティッキーヘッダー |
| `z-dropdown` | 100 | ドロップダウン・ポップオーバー |
| `z-overlay` | 200 | オーバーレイ背景 |
| `z-modal` | 300 | モーダル・ダイアログ |
| `z-toast` | 400 | トースト通知 |
| `z-tooltip` | 500 | ツールチップ |


## 9. Motion & Animation

### 9.1 Duration

| Token | Value | 用途 |
|-------|-------|------|
| `duration-instant` | 100ms | ホバー・フォーカス |
| `duration-fast` | 150ms | ボタン・切り替え |
| `duration-normal` | 250ms | パネル展開・フェード |
| `duration-slow` | 400ms | モーダル表示 |
| `duration-slower` | 600ms | ページ遷移 |

### 9.2 Easing

| Token | Value | 用途 |
|-------|-------|------|
| `ease-default` | `cubic-bezier(0.25, 0.1, 0.25, 1)` | 汎用 |
| `ease-in` | `cubic-bezier(0.4, 0, 1, 1)` | 退出アニメーション |
| `ease-out` | `cubic-bezier(0, 0, 0.2, 1)` | 出現アニメーション |
| `ease-spring` | `cubic-bezier(0.34, 1.56, 0.64, 1)` | バウンス感のある動き |

### 9.3 Hover Patterns

#### Gradient Shift — CTA・プライマリボタン

グラデーション背景がスライドし、多層グロウシャドウで深みを出すパターンです。

```css
.btn-gradient-shift {
  padding: 0.9em 1.4em;
  min-width: 120px;
  min-height: 44px;
  font-size: 1rem;
  font-weight: 500;
  border: none;
  border-radius: 8px;
  color: #ffffff;
  cursor: pointer;
  transition: 0.8s;
  background-size: 280% auto;
  background-image: linear-gradient(
    325deg,
    #5068a4 0%,       /* primary-500 */
    #798bb9 55%,      /* glow-400 */
    #5068a4 90%       /* primary-500 */
  );
  box-shadow:
    0px 0px 20px rgba(80, 104, 164, 0.5),
    0px 5px 5px -1px rgba(68, 80, 118, 0.25),
    inset 4px 4px 8px rgba(196, 211, 255, 0.5),
    inset -4px -4px 8px rgba(54, 63, 96, 0.35);
}

.btn-gradient-shift:hover {
  background-position: right top;
}

.btn-gradient-shift:is(:focus, :focus-visible, :active) {
  outline: none;
  box-shadow:
    0 0 0 3px #ffffff,
    0 0 0 6px #5068a4;
}
```

#### Glow Line — セカンダリ・ゴーストボタン

底辺のグロウラインがフェードインし、ボタン全体が浮上するパターンです。

```css
.btn-glow-line {
  min-width: 120px;
  position: relative;
  cursor: pointer;
  padding: 12px 17px;
  border: 0;
  border-radius: 7px;
  box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.1);
  background: radial-gradient(
    ellipse at bottom,
    #2a2a32 0%,        /* neutral-400 */
    #0a0a0c 45%        /* neutral-100 */
  );
  color: rgba(232, 232, 236, 0.66);  /* neutral-950 @ 66% */
  transition: all 1s cubic-bezier(0.15, 0.83, 0.66, 1);
}

.btn-glow-line::before {
  content: "";
  width: 70%;
  height: 1px;
  position: absolute;
  bottom: 0;
  left: 15%;
  background: linear-gradient(
    90deg,
    transparent 0%,
    #e8e8ec 50%,       /* neutral-950 */
    transparent 100%
  );
  opacity: 0.2;
  transition: all 1s cubic-bezier(0.15, 0.83, 0.66, 1);
}

.btn-glow-line:hover {
  color: #e8e8ec;      /* neutral-950 */
  transform: scale(1.1) translateY(-3px);
}

.btn-glow-line:hover::before {
  opacity: 1;
}
```

#### Liquid Hover — Liquid Glass ボタン

ホバー時にスペキュラハイライトが上縁から流れ落ち、背景ティントが深まるパターンです。

```css
.btn-liquid {
  position: relative;
  padding: 12px 24px;
  min-width: 120px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 12px;
  color: #e8e8ec;
  cursor: pointer;
  background: rgba(10, 10, 12, 0.5);
  backdrop-filter: blur(20px) saturate(1.4);
  -webkit-backdrop-filter: blur(20px) saturate(1.4);
  overflow: hidden;
  transition: all 0.4s cubic-bezier(0.25, 0.1, 0.25, 1);
}

.btn-liquid::before {
  content: "";
  position: absolute;
  top: -100%;
  left: 0;
  right: 0;
  height: 100%;
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0.12) 0%,
    transparent 100%
  );
  transition: top 0.6s cubic-bezier(0, 0, 0.2, 1);
  pointer-events: none;
}

.btn-liquid:hover {
  border-color: rgba(255, 255, 255, 0.18);
  background: rgba(80, 104, 164, 0.15);
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.15),
    0 8px 24px rgba(0, 0, 0, 0.3);
}

.btn-liquid:hover::before {
  top: 0;
}
```

### 9.4 Animation Patterns

```css
/* Fade In */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(8px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* Glow Pulse — ローディング・注目 */
@keyframes glowPulse {
  0%, 100% { box-shadow: 0 0 20px rgba(80, 104, 164, 0.1); }
  50%      { box-shadow: 0 0 40px rgba(80, 104, 164, 0.25); }
}

/* Shimmer — スケルトンローディング */
@keyframes shimmer {
  from { background-position: -200% 0; }
  to   { background-position: 200% 0; }
}
/* Usage: background: linear-gradient(90deg, #141418 25%, #1e1e24 50%, #141418 75%); background-size: 200% 100%; */

/* Liquid Ripple — Liquid Glass の波紋 */
@keyframes liquidRipple {
  0%   { transform: scale(0.95); opacity: 0.6; }
  50%  { transform: scale(1.02); opacity: 1; }
  100% { transform: scale(1); opacity: 1; }
}

/* Specular Slide — Liquid Glass のスペキュラ移動 */
@keyframes specularSlide {
  0%   { background-position: -100% 0; }
  100% { background-position: 200% 0; }
}
/* Usage: 疑似要素に linear-gradient(90deg, transparent, rgba(255,255,255,0.08), transparent) を適用 */
```


## 10. Iconography

| Property | Value |
|----------|-------|
| Style | Outline（線幅 1.5px）、角丸 |
| Optical Size | 20×20px（UI）、24×24px（ナビ）、32×32px（装飾） |
| Color | `text-secondary`（通常）、`text-primary`（アクティブ） |
| Recommended Set | Lucide / Phosphor（Outline） |


## 11. Platform-Specific Guidelines

### 11.1 Web Page / LP

- ヒーローには `gradient-hero` + `gradient-mesh` を背景に、`liquid-glass` パネルを配置
- セクション間は `space-9`（64px）以上の余白
- CTA ボタンは `btn-liquid` パターンで視線を集中させる
- 料金表の推奨プランには `liquid-glass-deep` を適用し、他プランは `glass` で差別化
- タイポグラフィは `display-xl` ～ `display-md` をヒーローに使用
- セクション区切りには `--line-liquid` を使用

### 11.2 Web App

- サーフェス階層を厳密に守る: `bg-page` → `bg-surface` → `bg-surface-raised`
- サイドバーには `glass-frosted` を適用し、コンテンツ領域との境界を柔らかく表現
- ヘッダーには `liquid-glass-deep` を適用し、スクロール時のコンテンツ溶け込み効果を活用
- インタラクティブ要素には必ず `focus-ring`（`glow-ring`）を適用
- 本文は `body-md`（14px）、密度の高いUIでは `body-sm`（12px）

### 11.3 Mobile App (iOS)

- iOS Human Interface Guidelines / Liquid Glass ガイドラインを優先し、トークンで色・タイポを上書き
- `liquid-glass` は iOS ネイティブの `.glass` modifier と対応させて実装
- タッチターゲット: 最小 44×44pt
- Spacing: `space-4`（12px）を最小パディング
- SF Pro を基本フォントとし、カラートークンのみ本システムから適用
- Dynamic Type をサポートし、Type Scale は参考値として扱う

### 11.4 Visual Presentation

- アスペクト比: **16:9**（1920×1080）
- 背景: `neutral-0` + `gradient-mesh`
- タイトル: `display-xl`（56px）、DM Sans Light 300
- 本文: `body-lg`（16px）以上（視認性確保）
- コードブロック: `mono-md`、`glass` 背景 + `radius-lg`
- キーワード・数値強調には `glow-medium` + テキストグラデーションで注目喚起
- セクション区切りに `--line-liquid` を使用
- 余白はデスクトップより大きく取る（`space-8` 以上）


## 12. Usage Quick Reference

### 12.1 Material Layer Map

```
┌─ Page: neutral-0 (#000000) + gradient-mesh ─────────────────────────┐
│                                                                       │
│  ┌─ Header ▸ liquid-glass-deep ──────────────────────────────────┐  │
│  │  Logo + Nav    specular highlight on top edge                  │  │
│  └────────────────────────────────────────────────────────────────┘  │
│                                                                       │
│  ┌─ Sidebar ▸ glass-frosted ──┐  ┌─ Content Area ──────────────┐  │
│  │  Nav items: glass on hover  │  │                              │  │
│  │                             │  │  ┌─ Card ▸ glass ────────┐  │  │
│  │                             │  │  │  Heading → #ffffff     │  │  │
│  │                             │  │  │  Body    → #e8e8ec     │  │  │
│  │                             │  │  │  Sub     → #7e7e8c     │  │  │
│  │                             │  │  └────────────────────────┘  │  │
│  │                             │  │                              │  │
│  │                             │  │  ┌─ CTA ▸ btn-liquid ────┐  │  │
│  │                             │  │  │  Specular highlight     │  │  │
│  │                             │  │  │  btn-liquid hover       │  │  │
│  │                             │  │  └────────────────────────┘  │  │
│  └─────────────────────────────┘  └──────────────────────────────┘  │
│                                                                       │
│  ┌─ Hero ▸ liquid-glass + gradient-hero ─────────────────────────┐  │
│  │  display-xl title, specular overlay                            │  │
│  │  CTA: liquid-glass-deep + glow-liquid                          │  │
│  └────────────────────────────────────────────────────────────────┘  │
└───────────────────────────────────────────────────────────────────────┘
```

### 12.2 Material × Component 早見表

| Component | Default | Accent | Light Mode |
|-----------|---------|--------|------------|
| Card | `glass` | `liquid-glass` | `glass-light-frosted` |
| Header | `liquid-glass-deep` | — | `liquid-glass-light-deep` |
| Sidebar | `glass-frosted` | — | `glass-light-frosted` |
| Button (Primary) | `btn-gradient-shift` | `btn-liquid` | 同左 |
| Button (Secondary) | `btn-glow-line` | — | 同左 |
| Modal | `glass-frosted` | — | `glass-light-frosted` |
| Tooltip | `liquid-glass-subtle` | — | `liquid-glass-light` |
| Pricing (Featured) | `glass` | `liquid-glass-deep` | `liquid-glass-light-deep` |

### 12.3 ステータス表示

```
Success  → アイコン: success-400, テキスト: success-500, 背景: success-900
Warning  → アイコン: warning-400, テキスト: warning-500, 背景: warning-900
Error    → アイコン: error-400,   テキスト: error-500,   背景: error-900
Info     → アイコン: info-400,    テキスト: info-500,    背景: info-900
```


## 13. Component Guidelines

UIコンポーネントの仕様をここで定義します。すべてのコンポーネントはデザイントークンから値を導出し、2 つのマテリアル（Glassmorphism / Liquid Glass）を用途に応じて適用します。

### 13.1 Button

#### Variants

| Variant | Background | Text | Border | 用途 |
|---------|-----------|------|--------|------|
| **Primary** | `interactive` (primary-500) | neutral-1000 (#fff) | none | CTA・主要アクション |
| **Secondary** | transparent | `text-primary` | `stroke-sm` solid `border-default` | 補助アクション |
| **Ghost** | transparent | `text-secondary` | none | 最小限のアクション |
| **Danger** | error-500 | neutral-1000 (#fff) | none | 破壊的アクション |

#### Sizes

| Size | Height | Padding (h) | Font | Radius |
|------|--------|-------------|------|--------|
| **sm** | 32px | 12px | `body-sm` (12px), semibold | `radius-md` |
| **md** | 40px | 16px | `body-md` (14px), semibold | `radius-md` |
| **lg** | 48px | 24px | `body-lg` (16px), semibold | `radius-md` |

#### States

| State | 変化 |
|-------|------|
| Default | 上記 Variants の通り |
| Hover | Primary → `gradient-shift` or `btn-liquid` / Secondary → `glow-line` |
| Active / Pressed | opacity: 0.8、transform: scale(0.98) |
| Focus | `glow-ring`（0 0 0 2px primary-600, 0 0 12px primary-500 @ 30%） |
| Disabled | opacity: 0.4、cursor: not-allowed |
| Loading | テキストを spinner に差し替え、pointer-events: none |

#### ライトモード差分

- Primary: background は同じ primary-500、text は neutral-1000
- Secondary: border-color → `border-default`（secondary-200）
- Ghost: text → `text-secondary`（neutral-600）

### 13.2 Card

| Property | Value |
|----------|-------|
| Background | `bg-surface` |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-lg` (12px) |
| Padding | `space-5` (16px) ～ `space-6` (24px) |
| Hover（optional） | border-color → `border-hover`、transition `duration-fast` |

#### Card Variants by Material

| Variant | Class | 用途 |
|---------|-------|------|
| **Glass Card** | `.glass` + `radius-lg` | 背景画像・グラデーション上に配置する標準カード |
| **Liquid Card** | `.liquid-glass` | ヒーロー内や動的コンテンツ上のカード |

```css
/* Glass Card */
.card-glass {
  background: rgba(10, 10, 12, 0.6);
  backdrop-filter: blur(24px);
  -webkit-backdrop-filter: blur(24px);
  border: 1px solid rgba(255, 255, 255, 0.06);
  border-radius: 12px;
  padding: 24px;
}

```

#### ライトモード差分

- Background: `bg-surface`（neutral-950 → #e8e8ec）
- Border: `border-default`（secondary-200 → #d7dded）
- Glass Card → `glass-light-frosted` を使用

### 13.3 Input / Text Field

| Property | Value |
|----------|-------|
| Background | `bg-surface` |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-md` (8px) |
| Height | 40px（md）/ 32px（sm） |
| Padding | 0 `space-4` (12px) |
| Font | `body-md` (14px) |
| Text Color | `text-primary` |
| Placeholder | `text-muted` |

#### States

| State | 変化 |
|-------|------|
| Default | 上記の通り |
| Hover | border-color → `border-hover` |
| Focus | border-color → `interactive`、`glow-ring` 適用 |
| Error | border-color → error-500、`glow-ring` を error-500 基調に差し替え |
| Disabled | background → neutral-200、opacity: 0.5 |

#### ライトモード差分

- Background: `bg-surface-raised`（#ffffff）
- Border: `border-default`（secondary-200）
- Text: `text-primary`（neutral-200 → #141418）

### 13.4 Badge / Tag

| Property | Value |
|----------|-------|
| Height | 22px |
| Padding | 0 `space-3` (8px) |
| Font | `label-sm` (11px), medium |
| Radius | `radius-sm` (4px) |
| Background | neutral-300 |
| Text Color | `text-secondary` |

ステータス表示の場合は Status Colors を使用します。

| Status | Background | Text |
|--------|-----------|------|
| Success | success-900 | success-400 |
| Warning | warning-900 | warning-400 |
| Error | error-900 | error-400 |
| Info | info-900 | info-400 |

### 13.5 Modal / Dialog

| Property | Value |
|----------|-------|
| Material | `glass-frosted` |
| Background | `bg-surface-raised` or Glass variant |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-xl` (16px) |
| Shadow | `shadow-lg` |
| Max Width | `container-sm` (640px) |
| Padding | `space-6` (24px) ～ `space-7` (32px) |
| Overlay | neutral-0 @ 60% opacity + `backdrop-filter: blur(8px)` |
| Entry Animation | `liquidRipple` `duration-slow` `ease-out` |

### 13.6 Toast / Notification

| Property | Value |
|----------|-------|
| Background | neutral-400 |
| Text Color | `text-primary` |
| Font | `mono-md` (13px) |
| Radius | `radius-md` (8px) |
| Padding | `space-3` (8px) `space-5` (16px) |
| Position | fixed、bottom: 24px、center |
| z-index | `z-toast` (400) |
| Animation | fadeIn + translateY(20px → 0)、`duration-normal` |
| Auto Dismiss | 3000ms default |

### 13.7 Navigation / Sidebar

| Property | Value |
|----------|-------|
| Material | `glass-frosted`（推奨）/ `bg-surface`（フォールバック） |
| Width | 240px ～ 280px |
| Border Right | `stroke-sm` solid `border-default` |
| Nav Item Height | 36px |
| Nav Item Padding | `space-3` (8px) `space-4` (12px) |
| Nav Item Font | `body-md` (14px) |
| Nav Item Radius | `radius-md` (8px) |
| Active State | background → neutral-200、text → `text-primary`、font-weight: 500 |
| Hover State | background → neutral-200、text → `text-primary` |

サイドバーには `glass-frosted` を標準適用し、コンテンツ領域との境界を柔らかく表現します。
ヘッダーバーには `liquid-glass-deep` を適用し、スクロール時に背景コンテンツが自然に溶け込む効果を活用します。

### 13.8 Table

| Property | Value |
|----------|-------|
| Header Font | `label-md` (13px), semibold, uppercase |
| Header Color | `text-secondary` |
| Header Border Bottom | `stroke-sm` solid `border-default` |
| Cell Font | `body-md` (14px) |
| Cell Padding | `space-5` (16px) |
| Row Border Bottom | `stroke-hairline` solid neutral-200 |
| Row Hover | background → neutral-100 |
| Mono Values | `mono-md` を使用（数値・コード） |
