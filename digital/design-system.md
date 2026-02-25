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

カラー定義の原本は `viewers/color-palette.html` を参照してください。

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

#### 設計原則

| 原則 | 詳細 |
|------|------|
| **背景依存性** | ガラスは背後に動きや色のある要素（グラデーション・ビデオ・メッシュ）があるとき最も映える。白・黒の無地背景には使わない |
| **使用量の制御** | 画面内の Liquid Glass 要素は最大 3〜4 個。すべてをガラスにすると奥行きが失われる |
| **レイヤー構成** | ベース（backdrop-filter）→ スペキュラ（::before）→ 屈折（::after / refraction） の順で疑似要素を重ねる |
| **アニメーションの節度** | `specularSweep` はユーザー操作（hover/click）にのみ発火させる。自動ループには `liquidFloat` を使う |
| **パフォーマンス** | `backdrop-filter` は GPU 負荷が高い。モバイルでは `blur` を 20px 以下に抑えるか `@supports` でフォールバックを用意する |

#### バリアント早見表

| クラス | blur | 用途 |
|--------|------|------|
| `.liquid-glass` | 40px | カード・パネル（標準） |
| `.liquid-glass-deep` | 60px | ヘッダー・ナビゲーション |
| `.liquid-glass-subtle` | 30px | ツールチップ・ポップオーバー |
| `.liquid-glass-pill` | 20px | バッジ・タグ・チップ |
| `.liquid-glass-input` | 20px | フォーム入力 |
| `.liquid-glass-nav-item` | 16px | サイドバー・タブ ナビアイテム |
| `.liquid-glass-refraction` | +2px hue-rotate | 屈折エフェクト（::after で重ねる） |
| `.liquid-glass-edge-sheen` | — | 側縁ハイライト（::after で重ねる） |

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

/* ─── Compact Variants ─── */

/* Liquid Glass — Pill (タグ・バッジ・チップ) */
.liquid-glass-pill {
  position: relative;
  display: inline-flex;
  align-items: center;
  background: linear-gradient(
    135deg,
    rgba(80, 104, 164, 0.12) 0%,
    rgba(142, 124, 180, 0.08) 50%,
    rgba(80, 104, 164, 0.12) 100%
  );
  backdrop-filter: blur(20px) saturate(1.6);
  -webkit-backdrop-filter: blur(20px) saturate(1.6);
  border: 1px solid rgba(255, 255, 255, 0.14);
  border-radius: 9999px;
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.18),
    inset 0 -1px 0 rgba(0, 0, 0, 0.08),
    0 2px 8px rgba(0, 0, 0, 0.2);
  overflow: hidden;
}

.liquid-glass-pill::before {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.12) 0%, transparent 50%);
  pointer-events: none;
}

/* Liquid Glass — Input / Form Element */
.liquid-glass-input {
  background: rgba(10, 10, 12, 0.4);
  backdrop-filter: blur(20px) saturate(1.4);
  -webkit-backdrop-filter: blur(20px) saturate(1.4);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 8px;
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.06),
    inset 0 2px 4px rgba(0, 0, 0, 0.15);
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}

.liquid-glass-input:focus {
  border-color: rgba(107, 132, 192, 0.4);
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.08),
    inset 0 2px 4px rgba(0, 0, 0, 0.1),
    0 0 0 2px rgba(80, 104, 164, 0.2),
    0 0 16px rgba(80, 104, 164, 0.1);
}

/* Liquid Glass — Nav Item (サイドバー・タブ ナビゲーション) */
.liquid-glass-nav-item {
  position: relative;
  background: transparent;
  border-radius: 8px;
  border: 1px solid transparent;
  transition: background 0.2s ease, border-color 0.2s ease, box-shadow 0.2s ease;
  overflow: hidden;
}

.liquid-glass-nav-item:hover {
  background: linear-gradient(
    135deg,
    rgba(80, 104, 164, 0.1) 0%,
    rgba(142, 124, 180, 0.06) 100%
  );
  backdrop-filter: blur(16px) saturate(1.4);
  -webkit-backdrop-filter: blur(16px) saturate(1.4);
  border-color: rgba(255, 255, 255, 0.08);
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.1),
    0 2px 8px rgba(0, 0, 0, 0.15);
}

.liquid-glass-nav-item.active {
  background: linear-gradient(
    135deg,
    rgba(80, 104, 164, 0.16) 0%,
    rgba(142, 124, 180, 0.1) 100%
  );
  backdrop-filter: blur(20px) saturate(1.6);
  -webkit-backdrop-filter: blur(20px) saturate(1.6);
  border-color: rgba(107, 132, 192, 0.2);
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.15),
    0 4px 12px rgba(0, 0, 0, 0.2);
}

/* ─── Effect Utilities ─── */

/* Refraction Layer — 光の屈折・色収差を疑似要素で演出 */
/* Usage: .liquid-glass-refraction クラスを追加して ::after で屈折オーバーレイを有効化 */
.liquid-glass-refraction::after {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  background: linear-gradient(
    135deg,
    rgba(255, 255, 255, 0.04) 0%,
    transparent 35%,
    rgba(80, 104, 164, 0.03) 65%,
    rgba(255, 255, 255, 0.02) 100%
  );
  backdrop-filter: blur(2px) hue-rotate(8deg);
  -webkit-backdrop-filter: blur(2px) hue-rotate(8deg);
  pointer-events: none;
}

/* Edge Sheen — 左右・上縁に光沢帯を追加するユーティリティ */
/* Usage: .liquid-glass-edge-sheen クラスを追加（::after が必要なコンポーネントと競合しない場合） */
.liquid-glass-edge-sheen::after {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  background:
    linear-gradient(90deg,
      rgba(255, 255, 255, 0.08) 0%,
      transparent 15%,
      transparent 85%,
      rgba(255, 255, 255, 0.04) 100%),
    linear-gradient(180deg,
      rgba(255, 255, 255, 0.1) 0%,
      transparent 30%);
  pointer-events: none;
}

/* ─── Light Mode Compact ─── */

/* Liquid Glass — Light Pill */
.liquid-glass-light-pill {
  position: relative;
  display: inline-flex;
  align-items: center;
  background: linear-gradient(
    135deg,
    rgba(255, 255, 255, 0.6) 0%,
    rgba(238, 240, 245, 0.4) 50%,
    rgba(255, 255, 255, 0.6) 100%
  );
  backdrop-filter: blur(20px) saturate(1.5);
  -webkit-backdrop-filter: blur(20px) saturate(1.5);
  border: 1px solid rgba(255, 255, 255, 0.7);
  border-radius: 9999px;
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.8),
    0 2px 8px rgba(80, 104, 164, 0.08);
  overflow: hidden;
}

/* Liquid Glass — Light Input */
.liquid-glass-light-input {
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(20px) saturate(1.3);
  -webkit-backdrop-filter: blur(20px) saturate(1.3);
  border: 1px solid rgba(255, 255, 255, 0.6);
  border-radius: 8px;
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.8),
    inset 0 2px 4px rgba(0, 0, 0, 0.04),
    0 1px 3px rgba(80, 104, 164, 0.06);
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}

.liquid-glass-light-input:focus {
  border-color: rgba(80, 104, 164, 0.4);
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.9),
    inset 0 2px 4px rgba(0, 0, 0, 0.02),
    0 0 0 2px rgba(80, 104, 164, 0.15),
    0 0 16px rgba(80, 104, 164, 0.06);
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

/* Specular Sweep — ホバー時にスペキュラが左端から右端へ一閃する */
@keyframes specularSweep {
  0%   { background-position: -200% 0; opacity: 0; }
  10%  { opacity: 1; }
  90%  { opacity: 1; }
  100% { background-position: 200% 0; opacity: 0; }
}
/* Usage: .liquid-glass:hover::after {
     animation: specularSweep 0.8s ease-out forwards;
     background: linear-gradient(90deg, transparent 0%, rgba(255,255,255,0.12) 50%, transparent 100%);
     background-size: 200% 100%;
   } */

/* Glass Edge Shine — エッジハイライトが呼吸するように輝く */
@keyframes glassEdgeShine {
  0%, 100% { opacity: 0.5; }
  50%       { opacity: 1; }
}
/* Usage: animation: glassEdgeShine 2.5s ease-in-out infinite; */

/* Liquid Float — 浮遊感のある縦揺れ（ヒーロー内カード・CTA に使用） */
@keyframes liquidFloat {
  0%, 100% { transform: translateY(0px); }
  50%       { transform: translateY(-5px); }
}
/* Usage: animation: liquidFloat 4s ease-in-out infinite; */
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

AI がウェブページ（LP・プロダクトページ等）を生成する際に従うルールセット。カラーパレット・セマンティックトークン・カラーの使い分けはセクション 2 を参照。マテリアル CSS 定義はセクション 7 を参照。

#### タイポグラフィ

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

コード・数値には `'JetBrains Mono', monospace` を使用。

テキストグラデーション（装飾用）:
```css
background: linear-gradient(90deg, #e8e8ec 0%, #8f99b8 100%);
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
```

#### マテリアル選択ガイド

| 用途 | マテリアル |
|------|-----------|
| カード・パネル | Standard Glass |
| ヘッダー・ナビ | blur(20px) + rgba(0,0,0,0.8) |
| ヒーロー内のカード・CTA | Liquid Glass |
| サイドバー・モーダル | Frosted Glass |

#### レイアウト

```css
.container { max-width: 1200px; margin: 0 auto; padding: 0 32px; }
section { padding: 96px 0; }
```

- カードグリッド: `display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px;`
- 2列グリッド: `repeat(2, 1fr); gap: 32px;`
- セクション見出し: text-align center, margin 0 auto 64px（横幅はコンテナ幅 1200px に統一。内部の `p` のみ可読性のため max-width 720px を適用）
- セクション区切り線:
```css
height: 1px;
background: linear-gradient(90deg, transparent 0%, rgba(80,104,164,0.15) 20%, rgba(142,124,180,0.2) 50%, rgba(80,104,164,0.15) 80%, transparent 100%);
```

##### ヘッダー
```css
header { position: fixed; top: 0; width: 100%; z-index: 1000;
  background: rgba(0,0,0,0.8); backdrop-filter: blur(20px);
  border-bottom: 1px solid rgba(255,255,255,0.06); }
nav { max-width: 1200px; margin: 0 auto; padding: 16px 32px;
  display: flex; justify-content: space-between; align-items: center; }
```

##### ヒーロー
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

#### ボタン

##### Primary（Gradient Shift）— CTA
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

##### Secondary（Glow Line）— 補助アクション
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

##### Ghost（Liquid Hover）— 最小限
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

#### カード

```css
background: rgba(10,10,12,0.6); backdrop-filter: blur(24px);
border: 1px solid rgba(255,255,255,0.06); border-radius: 12px; padding: 32px;
/* :hover */ transform: translateY(-4px); border-color: rgba(255,255,255,0.12);
```

アイコン領域: 48x48px, border-radius 8px, background rgba(80,104,164,0.15)

#### バッジ

```css
height: 22px; padding: 0 8px; font-size: 11px; font-weight: 500; border-radius: 4px;
/* default */ background: #1e1e24; color: #7e7e8c;
/* success */ background: #0a2615; color: #4ade80;
/* warning */ background: #2a2008; color: #facc15;
/* error */   background: #2a0a0a; color: #f87171;
/* info */    background: #0a1a2e; color: #60a5fa;
```

#### 入力フィールド

```css
height: 40px; padding: 0 12px; font-size: 14px; color: #e8e8ec;
background: #0a0a0c; border: 1px solid #1e1e24; border-radius: 8px;
/* ::placeholder */ color: #3d3d48;
/* :hover */ border-color: #2a2a32;
/* :focus */ border-color: #5068a4; box-shadow: 0 0 0 2px rgba(68,80,118,0.6), 0 0 12px rgba(80,104,164,0.3);
```

#### アニメーション

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

#### レスポンシブ

| ブレークポイント | 変更 |
|-----------------|------|
| max-width: 1023px | グリッド→2列、ヒーロー min-height auto、見出し縮小(40px/32px)、section padding 64px |
| max-width: 639px | グリッド→1列、container padding 16px、見出し縮小(32px/28px)、ナビ非表示、section padding 48px |

#### ページ構造（HTML）

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

#### 禁止事項

- font-weight: 700 は使わない（最大 600）
- 見出しに #e8e8ec より暗い色を使わない（見出しは #ffffff）
- border-radius を 12px より大きくしない（Liquid Glass の 16px、ピル型ボタンは例外）
- `!important` は使わない
- セクション間余白を 64px 未満にしない
- カード padding を 24px 未満にしない

### 11.2 Web App

- サーフェス階層を厳密に守る: `bg-page` → `bg-surface` → `bg-surface-raised`
- サイドバーには `glass-frosted` を適用し、コンテンツ領域との境界を柔らかく表現
- ヘッダーには `liquid-glass-deep` を適用し、スクロール時のコンテンツ溶け込み効果を活用
- インタラクティブ要素には必ず `focus-ring`（`glow-ring`）を適用
- 本文は `body-md`（14px）、密度の高いUIでは `body-sm`（12px）

### 11.3 Mobile App (iOS)

#### 基本方針

- iOS Human Interface Guidelines / Liquid Glass ガイドラインを優先し、トークンで色・タイポを上書き
- `Liquid Glass` は iOS ネイティブの `.glass` modifier と対応させて実装
- SF Pro を基本フォントとし、カラートークンのみ本システムから適用
- Dynamic Type をサポートし、Type Scale は参考値として扱う
- テクスチャ・マテリアルはパフォーマンスを考慮し、背景色のみでフォールバックする

#### Layout & Touch Targets

**Touch Target Size**:
- 最小: 44×44pt（HIG 必須）
- 推奨: 48×48pt（よりタップしやすい）
- アイコンボタンは視覚サイズが小さくてもタッチ領域を44pt確保する

**Spacing**:
- 最小パディング: `space-4`（12px）
- コンテンツ間マージン: `space-5`（16px）
- セクション間マージン: `space-7`（32px）

**Safe Area** — 全コンテンツを Safe Area 内に配置する。背景のみ Safe Area を無視して画面全体に広げる:
```swift
ZStack {
  backgroundView.ignoresSafeArea()
  contentView.padding(.horizontal, 16)
}
```

#### Navigation Patterns

**Tab Bar** — アプリのプライマリナビゲーション:
- タブ数: 3～5個（推奨4個）
- 選択状態: `accent-default` カラー + 太字アイコン
- バッジ表示: 通知数を `.badge()` modifier で表示
- 常時表示: コンテンツスクロールで隠さない

**Navigation Bar** — 階層的ナビゲーション:
- Large Title 使用: トップレベル画面のみ `.navigationBarTitleDisplayMode(.large)`
- 戻るボタン: 自動生成される `< 前の画面` を使用（カスタマイズ不要）
- トレイリングボタン: 最大2個まで（3個以上は `...` メニューに集約）

**Modal / Sheet** — 一時的なコンテキスト:
- `.sheet()` 使用: 軽量なタスク（フォーム入力、詳細表示）
- `.fullScreenCover()` 使用: 没入型タスク（カメラ、画像編集）
- スワイプ解除: デフォルト有効、破壊的アクションがある場合のみ `.interactiveDismissDisabled()` で無効化

**Alert / Action Sheet** — 確認・選択ダイアログ:
- 破壊的アクション: `.destructive` で赤表示（例: "削除"、"ログアウト"）
- キャンセルボタン: 常に下部に配置（Action Sheet）、右側に配置（Alert）
- デフォルトアクション: `.default` でシステム推奨スタイル

#### Interaction & Feedback

**Response Time** — タップから100ms以内に視覚フィードバックを提供する:
```swift
Button("送信") { /* ... */ }
  .buttonStyle(.borderedProminent)  // 即座に押下状態を表示
```

**Haptics** — 適切な触覚フィードバックで操作感を向上させる:
- 成功アクション: `UIImpactFeedbackGenerator(style: .light).impactOccurred()`
- 通常操作: `.medium`
- 重要操作: `.heavy`
- エラー: `UINotificationFeedbackGenerator().notificationOccurred(.error)`

**Loading Indicators**:
- 不定期間: `.progressView(style: .circular)` （くるくる回るインジケータ）
- 確定期間: `.progressView(value: progress)` （プログレスバー）
- 全画面ローディング: 半透明オーバーレイ + `.progressView` 中央配置
- インラインローディング: `.redacted(reason: .placeholder)` で骨組み表示

#### Typography Mapping

**SF Pro Font Selection** — iOS システムフォントの正しい使い分け:
- SF Pro Text: 19pt以下のテキスト（本文・ラベル・キャプション）
- SF Pro Display: 20pt以上のテキスト（見出し・タイトル）
- SF Mono: コードブロック・固定幅が必要な場合（セクション 3 の `mono-*` トークンに対応）

**Dynamic Type Mapping** — iOS の Dynamic Type サイズクラスとデザインシステムの Type Scale の対応:
- Large (default): `body-md` (14px) を基準とする
- xSmall～Small: `body-sm` (12px) 相当
- xLarge～xxxLarge: `body-lg` (16px) ～ `heading-sm` (18px) 相当
- 最小フォントサイズ: 11pt（copyright・法的表示のみ）

**Line Height & Spacing** — iOS 標準の行送り:
- 見出し: 1.1～1.3
- 本文: 1.4～1.5（日本語混在時は 1.6～1.7 推奨）

#### Component Mapping

デザインシステムのコンポーネントと iOS ネイティブコンポーネントの対応:

| Design System | iOS Component | Token Application |
|---------------|---------------|-------------------|
| Button (Primary) | `.buttonStyle(.borderedProminent)` | `bg`: `interactive-default`, `text`: `text-on-accent` |
| Button (Secondary) | `.buttonStyle(.bordered)` | `border`: `border-strong`, `text`: `text-primary` |
| Button (Ghost) | `.buttonStyle(.plain)` | `text`: `interactive-default` |
| Card | `List` with `.listStyle(.insetGrouped)` | `bg`: `bg-surface-raised`, Glassmorphism 適用 |
| Input | `TextField` with `.textFieldStyle(.roundedBorder)` | `border`: `border-default`, `bg`: `bg-surface` |
| Badge | `.badge()` modifier | `bg`: Status Colors（Success/Warning/Error） |
| Modal | `.sheet()` / `.fullScreenCover()` | `bg`: `bg-page`, Liquid Glass 適用（Hero 背景） |

#### Motion & Animation

**Spring Animation** — iOS 標準の spring アニメーションパラメータ:
```swift
// 標準（UI要素の表示/非表示）
.spring(response: 0.3, dampingFraction: 0.8)

// 軽快（小さな変化・インタラクティブ操作）
.spring(response: 0.15, dampingFraction: 0.9)

// ゆったり（大きな変化・画面遷移）
.spring(response: 0.5, dampingFraction: 0.75)
```

**Transition Duration**:
- シート表示: 0.3s（デフォルト）
- アラート表示: 0.2s
- リスト項目の挿入/削除: 0.25s
- ページ遷移: 0.35s

**Easing Curve**:
- 標準: `.easeInOut`（SwiftUI default）
- 進入: `.easeOut`
- 退出: `.easeIn`

### 11.4 Presentation (pptx)

AI がスライドデッキ（pptx）を生成する際に従うルールセット。カラーパレット・セマンティックトークンはセクション 2 を参照。マテリアル CSS 定義はセクション 7 を参照。ボーダーラウンドはセクション 6 を参照。

#### 基本設定

- 出力形式: pptx（PowerPoint）
- サイズ: 1920×1080px（16:9） — pptx 換算 13.333" × 7.5"
- フォント: DM Sans (300,400,500,600,700) + JetBrains Mono (400,500,600)

#### タイポグラフィ

**注意: スライドでは 10px 未満を使わない。**

テキストカラーはタイポグラフィでは固定しない。セマンティックトークン（text-primary, text-secondary, text-muted 等）を背景色との組み合わせで選択する。具体的な対応は「カラーの使い分け」セクション（2.3 相当）を参照のこと。

| 用途 | size | weight | line-height | letter-spacing |
|------|------|--------|-------------|----------------|
| タイトルスライド見出し | 56px | 400 | 1.1 | -1.5px |
| スライド見出し | 44px | 400 | 1.15 | -1px |
| カードタイトル | 28px | 600 | 1.3 | 0 |
| 本文（スライド基準） | 20px | 500 | 1.6 | 0 |
| カード本文 | 18px | 500 | 1.6 | 0 |
| ラベル(uppercase) | 12px | 700 | 1.2 | 2px |
| 数値ハイライト(大) | 64px | 600 | 1.0 | 0 |
| 数値ハイライト(小) | 48px | 600 | 1.0 | 0 |
| 装飾番号 | 72px | 400 | 1.0 | 0, opacity 0.3 |
| サブタイトル | 24px | 400 | 1.4 | -0.5px |
| 連絡先 | 16px | 500 | 1.5 | 0 |
| URL (mono) | 14px | 500 | 1.5 | 0 |
| スライド番号 (mono) | 11px | 600 | 1.0 | 0.5px |
| copyright (mono) | 10px | 500 | 1.0 | 0 |

テキストグラデーション:
```css
background: linear-gradient(90deg, #e8e8ec 0%, #8f99b8 100%);
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
```

#### マテリアル使用ルール

##### マテリアル内テキスト配置

マテリアルグループ（同一種類のマテリアルが横に並ぶ集合）では、代表となる1つのマテリアルについてテキスト配置を決定し、グループ内の全マテリアルに同一ルールを適用する。個別のマテリアルごとに配置を変えない。

| マテリアル | 水平方向 | 垂直方向 | 備考 |
|-----------|---------|---------|------|
| Glass カード | left | top | コンテンツは上から下へ流す |
| Liquid Glass（強調カード） | center | center | インパクト重視、短いテキスト向け |
| データカード（数値ハイライト） | center | center | 数値を中央に大きく配置 |
| コードブロック | left | top | コードは左上起点 |

##### 枠線と中塗りの使い分け

枠線（border/stroke）と中塗り（background fill）は基本的に併用しない。

- **併用可能な例外**: 中塗りが十分に薄く（低 opacity）、同系統の色で枠線を引く場合のみ許可（例: Glass カードの半透明背景 + 同系統の微細ボーダー）

#### レイアウト

##### スライド共通
```css
.slide { width: 1920px; height: 1080px; padding: 64px 80px; }
```

##### スライドコンポーネント

スライドは header / body / footer の3コンポーネントで構成する。各コンポーネントを組み合わせてスライドパターンを作成する。

**Header** — スライド上部の見出し領域。

| サブ要素 | 内容 | タイポグラフィ |
|---------|------|--------------|
| agenda | セクションラベル（例: 「01 INTRODUCTION」） | 12px / 700 / uppercase / letter-spacing: 2px |
| title | スライド見出し | 44px / 400 / letter-spacing: -1px |
| main message | メインメッセージ・要点 | 20px / 500 |

Grid（pptx 座標）:

| プロパティ | px | inch |
|-----------|-----|------|
| left | 80 | 0.56" |
| top | 64 | 0.44" |
| width | 1760 | 12.22" |
| height（agenda + title） | 160 | 1.11" |
| height（+ main message） | 200 | 1.39" |

**Body** — メインコンテンツ領域。カード・テキスト・図表等を配置する。

Grid（pptx 座標）:

| プロパティ | px | inch |
|-----------|-----|------|
| left | 80 | 0.56" |
| top | header 下端 + 40 | header 下端 + 0.28" |
| width | 1760 | 12.22" |
| height | footer 上端まで（auto） | — |

**Footer** — スライド下部の固定領域。

| サブ要素 | 内容 | タイポグラフィ | 配置 |
|---------|------|--------------|------|
| page number | スライド番号 | 11px / 600 / mono / letter-spacing: 0.5px | 右寄せ |
| copyright | 著作権表示 | 10px / 500 / mono | 左寄せ |

Grid（pptx 座標）:

| プロパティ | px | inch |
|-----------|-----|------|
| left | 80 | 0.56" |
| top | 1032 | 7.17" |
| width | 1760 | 12.22" |
| height | 48 | 0.33" |

#### スライドパターン

**1. タイトルスライド**
- Header: 使用しない
- Body: 全要素中央配置 — logo → タイトル（56px / 400）→ サブタイトル（24px / 400）→ 日付（14px / mono）
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
- Body: 数値カード（center 配置、64px / 600 + ラベル 18px / 500）、Glass カードに内包
- Footer: page number + copyright

#### 箇条書き
```css
li { font-size: 20px; color: #a5a5b0; line-height: 1.6; padding-left: 24px; }
li::before { width: 8px; height: 8px; border-radius: 50%; background: #5068a4; }
```

#### コードブロック
```css
background: #0a0a0c; border: 1px solid #1e1e24; border-radius: 8px;
padding: 32px; font-family: 'JetBrains Mono'; font-size: 16px; line-height: 1.7; color: #a5a5b0;
```

#### 表（テーブル）

| プロパティ | 値 |
|-----------|-----|
| ヘッダーフォント | 12px / 700 / uppercase / letter-spacing: 1px |
| ヘッダーカラー | text-secondary |
| ヘッダー下ボーダー | 1px solid border-default |
| セルフォント | 18px / 500 |
| セルカラー | text-primary |
| セルパディング | 16px 20px |
| セル line-height | 1.5 |
| 行ボーダー | 0.5px solid border-default |
| 交互行背景 | なし（ダーク背景では不使用） |
| 数値セル | mono / right-aligned |

#### 画像・図表

| プロパティ | ルール |
|-----------|-------|
| 最大幅 | body 幅（1760px / 12.22"） |
| アスペクト比 | 元画像の比率を維持 |
| 配置 | body 領域内で水平中央 |
| キャプション | 画像下部、text-secondary、14px / 500、margin-top: 12px |
| スクリーンショット枠 | 1px solid border-default + radius-md |
| チャート内テキスト | 14px 以上（視認性確保） |
| チャートカラー | primary / glow パレットから選択 |
| 背景透過 | 図表の背景は透過させスライド背景と一体化する |

#### ロゴ

| スライドタイプ | 配置 | サイズ |
|-------------|------|-------|
| タイトルスライド | body 中央、タイトル上部 | height: 48px |
| コンテンツスライド | 使用しない | — |

ロゴは単色版を使用する。Dark Mode では #ffffff、Light Mode では #141418。

#### トランジション

| 項目 | ルール |
|------|-------|
| スライド切替 | カット（瞬時切替）をデフォルトとする |
| セクション間切替 | フェード（0.3s）を許可 |
| オブジェクトアニメーション | 使用しない |

#### 禁止事項

- 10px 未満のフォントサイズを使用しない
- font-weight: 800 以上は使わない
- タイポグラフィにカラーを固定指定しない（セマンティックトークンで背景色と合わせて決定する）
- 枠線（border）と中塗り（fill）を併用しない（薄い中塗り + 同系統の枠線の場合を除く）
- 1スライドにカード 3枚 or 箇条書き 5項目が上限目安
- 背景色を #000000 以外にしない
- スライドの padding を 64px 80px 未満にしない
- border-radius を radius-md（8px）を超えて使用しない（50% の円形を除く）

### 11.5 Thumbnail / OGP

AI がサムネイル・OGP 画像用 HTML を生成する際に従うルールセット。カラーパレットはセクション 2 を参照。

#### サイズ

| パターン | サイズ | 用途 |
|---------|--------|------|
| OGP | 1200×630px | og:image, Twitter Card, Slack preview |
| YouTube | 1280×720px | YouTube サムネイル |

#### タイポグラフィ

| 要素 | OGP (1200×630) | YouTube (1280×720) | weight | color |
|------|----------------|---------------------|--------|-------|
| タイトル | 48px | 56px | 300 | #ffffff |
| サブタイトル | 20px | 24px | 400 | #7e7e8c |
| タグ | 13px | 13px | 600 | #6b84c0 |
| ロゴ | 14px | 14px | 600 | #7e7e8c |

letter-spacing: タイトルは -1.5px、タグは 1.5px (uppercase)、ロゴは 3px (uppercase)

#### 背景

mesh gradient + hero gradient を疑似要素で適用:
```css
/* ::before — mesh gradient */
background:
  radial-gradient(at 20% 30%, rgba(80,104,164,0.25) 0%, transparent 50%),
  radial-gradient(at 80% 70%, rgba(142,124,180,0.2) 0%, transparent 50%),
  radial-gradient(at 50% 50%, rgba(203,192,230,0.08) 0%, transparent 60%);

/* ::after — hero gradient（上部からの光） */
background: radial-gradient(ellipse 80% 50% at 50% 0%, rgba(80,104,164,0.2) 0%, transparent 70%);
```

#### 構成要素

すべて任意。タイトルのみ必須。全要素中央配置。

##### タグ（上部ラベル）
```css
padding: 6px 16px; font-size: 13px; font-weight: 600;
letter-spacing: 1.5px; text-transform: uppercase; color: #6b84c0;
background: rgba(80,104,164,0.15); border: 1px solid rgba(107,132,192,0.3);
border-radius: 4px;
```

##### タイトル
```css
/* OGP */ font-size: 48px;
/* YouTube */ font-size: 56px;
font-weight: 300; line-height: 1.1; letter-spacing: -1.5px; color: #ffffff;
max-width: 80%;
```

##### サブタイトル
```css
/* OGP */ font-size: 20px;
/* YouTube */ font-size: 24px;
font-weight: 400; color: #7e7e8c; max-width: 70%; line-height: 1.4;
```

##### ロゴ
```css
font-size: 14px; font-weight: 600; letter-spacing: 3px;
text-transform: uppercase; color: #7e7e8c;
```

##### ボトム装飾ライン
```css
position: absolute; bottom: 0; left: 0; right: 0; height: 3px;
background: linear-gradient(90deg, transparent 0%, #5068a4 30%, #8e7cb4 50%, #5068a4 70%, transparent 100%);
```

##### テキストグラデーション（装飾用）
```css
background: linear-gradient(90deg, #e8e8ec 0%, #8f99b8 100%);
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
```

#### HTML 構造

```html
<div style="width: 1200px; height: 630px; /* or 1280x720 */
  position: relative; overflow: hidden; background: #000;
  display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;">
  <!-- ::before, ::after で背景 gradient -->
  <div style="position: relative; z-index: 1; display: flex; flex-direction: column; align-items: center; gap: 16px;">
    <div>TAG</div>
    <h1>TITLE</h1>
    <p>SUBTITLE</p>
    <div>LOGO</div>
  </div>
  <!-- ボトムライン -->
  <div style="position: absolute; bottom: 0; left: 0; right: 0; height: 3px; background: ...;"></div>
</div>
```

#### 禁止事項

- 背景色を #000000 以外にしない
- タイトルを 40px 未満にしない
- font-weight: 700 は使わない
- テキストを 4行以上にしない（1〜2行推奨）
- コンテンツの max-width を 80% より広くしない


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
| Sidebar Nav Item | `liquid-glass-nav-item` | — | 同左 |
| Button (Primary) | `btn-gradient-shift` | `btn-liquid` | 同左 |
| Button (Secondary) | `btn-glow-line` | — | 同左 |
| Badge / Tag | `liquid-glass-pill` | — | `liquid-glass-light-pill` |
| Input / Select | `liquid-glass-input` | — | `liquid-glass-light-input` |
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
