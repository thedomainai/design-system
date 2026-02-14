# The Domain AI Company — Utopia Design System

ルネサンス期の油絵に着想を得た、深い色彩と厚塗り（Impasto）テクスチャのデザインシステムです。
漆黒の Raw Umber キャンバスの上に、ラピスラズリの深い青、バーミリオンの赤、ゴールドオーカーの輝きを重ね、古典絵画の重厚さとモダンデザインの精緻さを両立します。
Web Page / Web App / Mobile App / Visual Presentation の全アウトプットで統一的に使用します。

## 1. Design Principles

| # | 原則 | 説明 |
|---|------|------|
| 1 | **Old Masters' Canvas** | 温かみのあるダークキャンバスを基調に、顔料の深みと光の階調で情報の重みを伝える |
| 2 | **Impasto & Glaze** | 厚塗り（Impasto）の存在感と、薄塗り（Glaze）の透明な奥行きの 2 層で質感を構成する |
| 3 | **Chromatic Depth** | ルネサンス絵画の限られた顔料が生む深い色相環を踏襲し、彩度を抑えた重厚な色彩で統一する |
| 4 | **Tactile Warmth** | すべてのサーフェスに触れたくなるような「手触り」を持たせ、デジタルでありながら有機的な温もりを実現する |
| 5 | **Modern Precision** | 古典の美意識を土台にしつつ、トークンベースの厳密な設計で一貫性と拡張性を担保する |

## 2. Color System

### 2.1 Color Palette

ルネサンス期の画家が用いた顔料に基づくカラーパレットです。各色は歴史的な顔料名を冠し、11 段階のシェードで構成します。

#### Primary — Ultramarine (ラピスラズリ)

ルネサンス期に最も高価だった顔料、ラピスラズリの深い青です。知性・崇高さ・信頼を象徴します。

| Token | Hex | 用途 |
|-------|-----|------|
| `primary-50` | `#edf0f9` | ライトモード背景・ホバー |
| `primary-100` | `#d4daf0` | ライトモード薄い背景 |
| `primary-200` | `#a9b5e1` | サブテキスト（ライト） |
| `primary-300` | `#7e8fd2` | アイコン・装飾（ライト） |
| `primary-400` | `#5a6db8` | インタラクティブ hover |
| `primary-500` | `#3d4f9e` | **インタラクティブ default** |
| `primary-600` | `#2e3b78` | フォーカスリング・押下時 |
| `primary-700` | `#232d5c` | 濃いアクセント |
| `primary-800` | `#1a2145` | カード背景（ダーク） |
| `primary-900` | `#111630` | セクション背景（ダーク） |
| `primary-950` | `#0a0d1e` | 最深背景 |

#### Secondary — Burnt Sienna (焼きシエナ)

大地の温もりを伝えるアーストーンです。テキスト・補助要素・ナビゲーションに使用します。

| Token | Hex | 用途 |
|-------|-----|------|
| `secondary-50` | `#faf6f3` | ライトモード最明色 |
| `secondary-100` | `#f0e8e0` | ライトモード背景 |
| `secondary-200` | `#dcc8b5` | ボーダー（ライト） |
| `secondary-300` | `#c4a78c` | プレースホルダ |
| `secondary-400` | `#a88464` | 補助テキスト |
| `secondary-500` | `#8b6543` | セカンダリテキスト |
| `secondary-600` | `#6e4f35` | ラベル |
| `secondary-700` | `#553d29` | 非アクティブ要素 |
| `secondary-800` | `#3e2d1e` | サーフェス（ダーク） |
| `secondary-900` | `#2a1e14` | ボーダー強調（ダーク） |
| `secondary-950` | `#1a130c` | 深いサーフェス |

#### Accent — Vermillion (バーミリオン)

ティツィアーノやカラヴァッジオが多用した深紅です。CTA・強調・視線誘導に使用します。

| Token | Hex | 用途 |
|-------|-----|------|
| `accent-50` | `#fdf0ee` | アクセント最明 |
| `accent-100` | `#f9d8d3` | アクセント背景 |
| `accent-200` | `#f0ada3` | **ホバーエフェクト基準色** |
| `accent-300` | `#e3806f` | アクセントサブ |
| `accent-400` | `#d45a45` | インタラクティブ hover（アクセント） |
| `accent-500` | `#b83a24` | **CTA・プライマリアクセント** |
| `accent-600` | `#93301e` | 押下時 |
| `accent-700` | `#712618` | 濃いアクセント |
| `accent-800` | `#521c12` | ダークサーフェスアクセント |
| `accent-900` | `#38120c` | オーバーレイ |
| `accent-950` | `#200a06` | 最深アクセント |

#### Gold — Gold Ochre (ゴールドオーカー)

額縁やイルミネーション装飾に見られる黄金の輝きです。ハイライト・装飾・グロウエフェクトに使用します。

| Token | Hex | 用途 |
|-------|-----|------|
| `gold-50` | `#fdf8ee` | ゴールド最明 |
| `gold-100` | `#f8ecd0` | ゴールド背景 |
| `gold-200` | `#eed6a0` | **グロウエフェクト基準色** |
| `gold-300` | `#dfbc6e` | グロウ減衰 |
| `gold-400` | `#cca044` | グロウサブ |
| `gold-500` | `#b38628` | 装飾アイコン |
| `gold-600` | `#8f6b20` | ボーダーグロウ |
| `gold-700` | `#6d5218` | サーフェスアクセント |
| `gold-800` | `#4e3b12` | **ベースカラー**・深いサーフェス |
| `gold-900` | `#33270c` | オーバーレイ |
| `gold-950` | `#1c1507` | 最深ゴールド |

#### Neutral — Raw Umber Canvas

油絵のキャンバス地をベースにした、温かみのあるニュートラルスケールです。ピュアブラックではなく、Raw Umber（生アンバー）の温かみが微かに残ります。

| Token | Hex | 輝度目安 | 用途 |
|-------|-----|----------|------|
| `neutral-0` | `#0c0a08` | 3% | 最深背景・ページ背景 |
| `neutral-50` | `#110f0c` | 5% | 微差レイヤー |
| `neutral-100` | `#18150f` | 7% | サーフェス |
| `neutral-200` | `#211d16` | 11% | サーフェス（浮上） |
| `neutral-300` | `#2c2720` | 15% | ボーダー default |
| `neutral-400` | `#3a342b` | 20% | ボーダー hover |
| `neutral-500` | `#524a3f` | 29% | テキスト muted |
| `neutral-600` | `#6e6456` | 39% | セパレーター |
| `neutral-700` | `#8e8272` | 52% | テキスト secondary |
| `neutral-800` | `#b0a494` | 66% | テキスト sub |
| `neutral-900` | `#d2c8b8` | 80% | テキスト default |
| `neutral-950` | `#ece5d8` | 92% | **テキスト primary** |
| `neutral-1000` | `#faf5ed` | 98% | アイボリーホワイト（見出し・強調） |

### 2.2 Semantic Tokens

用途に基づく意味的トークンです。実装時はこちらを優先して使用します。

| Semantic Token | Maps To | Hex | 用途 |
|----------------|---------|-----|------|
| `bg-page` | neutral-0 | `#0c0a08` | ページ全体の背景 |
| `bg-surface` | neutral-100 | `#18150f` | カード・パネル背景 |
| `bg-surface-raised` | neutral-200 | `#211d16` | 浮上サーフェス（モーダル等） |
| `border-default` | neutral-300 | `#2c2720` | 通常のボーダー |
| `border-hover` | neutral-400 | `#3a342b` | ホバー時のボーダー |
| `text-primary` | neutral-950 | `#ece5d8` | 本文テキスト |
| `text-secondary` | neutral-700 | `#8e8272` | 補助テキスト |
| `text-muted` | neutral-500 | `#524a3f` | 非活性・ヒントテキスト |
| `interactive` | primary-500 | `#3d4f9e` | ボタン・リンク |
| `interactive-hover` | primary-400 | `#5a6db8` | ホバー状態 |
| `focus-ring` | primary-600 | `#2e3b78` | フォーカスインジケーター |
| `glow-effect` | gold-300 | `#dfbc6e` | グロウエフェクト |
| `cta` | accent-500 | `#b83a24` | CTA ボタン・強調 |
| `cta-hover` | accent-400 | `#d45a45` | CTA ホバー状態 |

### 2.3 Light Mode Semantic Tokens

ダークモードのトークンと対になるライトモード用の意味的トークンです。同じセマンティック名を使い、テーマ切り替え時に値を差し替えます。

| Semantic Token | Maps To (Light) | Hex | 用途 |
|----------------|-----------------|-----|------|
| `bg-page` | neutral-1000 | `#faf5ed` | ページ全体の背景 |
| `bg-surface` | secondary-50 | `#faf6f3` | カード・パネル背景 |
| `bg-surface-raised` | neutral-1000 | `#faf5ed` | 浮上サーフェス（モーダル等） |
| `border-default` | secondary-200 | `#dcc8b5` | 通常のボーダー |
| `border-hover` | secondary-300 | `#c4a78c` | ホバー時のボーダー |
| `text-primary` | neutral-200 | `#211d16` | 本文テキスト |
| `text-secondary` | neutral-600 | `#6e6456` | 補助テキスト |
| `text-muted` | neutral-700 | `#8e8272` | 非活性・ヒントテキスト |
| `interactive` | primary-500 | `#3d4f9e` | ボタン・リンク |
| `interactive-hover` | primary-600 | `#2e3b78` | ホバー状態 |
| `focus-ring` | primary-400 | `#5a6db8` | フォーカスインジケーター |
| `glow-effect` | gold-400 | `#cca044` | グロウエフェクト |
| `cta` | accent-500 | `#b83a24` | CTA ボタン・強調 |
| `cta-hover` | accent-600 | `#93301e` | CTA ホバー状態 |

- `interactive` は Dark / Light で同じ primary-500 を使用し、ブランドカラーの一貫性を保ちます。
- ステータスカラーはライトモードでは **600** をテキストに、**50 相当の薄い背景** をバッジに使用します。

### 2.4 Status Colors

| Status | 400（明） | 500（基準） | 600（暗） | 900（bg） |
|--------|-----------|------------|-----------|-----------|
| **Success** | `#6abf7b` | `#3a9e4e` | `#2a7d3a` | `#12261a` |
| **Warning** | `#e0b84a` | `#c89b2a` | `#a07820` | `#2a2210` |
| **Error** | `#d46860` | `#b84040` | `#943030` | `#2a1210` |
| **Info** | `#6a8ec0` | `#4a70a8` | `#365890` | `#101c2a` |

- ステータスカラーの **500** をアイコン・テキストに、**900** をバッジ背景に使用します。
- ダーク UI 上では **400** を使うとコントラスト比が確保しやすくなります。
- 全体の色調と調和するよう、ルネサンス絵画の顔料に見られる若干くすんだトーンで統一しています。

## 3. Typography

### 3.1 Font Family

| Role | Font | Fallback | 用途 |
|------|------|----------|------|
| **Serif** | Playfair Display | Georgia, 'Times New Roman', serif | 見出し・ヒーロー・装飾的テキスト |
| **Sans** | Source Sans 3 | -apple-system, sans-serif | 本文・UI 全般 |
| **Mono** | JetBrains Mono | SF Mono, monospace | コード・数値・トークン表示 |

```
--font-serif: 'Playfair Display', Georgia, 'Times New Roman', serif;
--font-sans: 'Source Sans 3', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-mono: 'JetBrains Mono', 'SF Mono', 'Fira Code', monospace;
```

ルネサンスの書体文化を反映し、見出しにはセリフ体を使用します。Playfair Display のハイコントラストなストロークは、油絵の太い筆致と細い線描の対比を想起させます。本文は可読性を最優先し、モダンなサンセリフで構成します。

### 3.2 Type Scale

8px をベースに Major Third (1.25) スケールで構成します。

| Token | Size | Weight | Line Height | Letter Spacing | Font | 用途 |
|-------|------|--------|-------------|----------------|------|------|
| `display-xl` | 64px / 4rem | 700 | 1.05 | -2px | Serif | ヒーロー見出し |
| `display-lg` | 48px / 3rem | 700 | 1.1 | -1.5px | Serif | セクション見出し |
| `display-md` | 36px / 2.25rem | 600 | 1.15 | -1px | Serif | ページタイトル |
| `heading-lg` | 28px / 1.75rem | 600 | 1.25 | -0.5px | Serif | カードタイトル |
| `heading-md` | 22px / 1.375rem | 600 | 1.3 | -0.3px | Serif | サブセクション |
| `heading-sm` | 18px / 1.125rem | 600 | 1.35 | 0 | Sans | 小見出し |
| `body-lg` | 16px / 1rem | 400 | 1.65 | 0 | Sans | 本文（大） |
| `body-md` | 14px / 0.875rem | 400 | 1.6 | 0.1px | Sans | **本文（基準）** |
| `body-sm` | 12px / 0.75rem | 400 | 1.5 | 0.2px | Sans | 注釈・キャプション |
| `label-lg` | 14px / 0.875rem | 600 | 1.2 | 0.8px | Sans | ボタンラベル |
| `label-md` | 13px / 0.8125rem | 600 | 1.2 | 2.5px | Sans | セクションラベル（uppercase） |
| `label-sm` | 11px / 0.6875rem | 500 | 1.2 | 2px | Sans | タグ・バッジ |
| `mono-md` | 13px / 0.8125rem | 400 | 1.7 | 0 | Mono | コードブロック |
| `mono-sm` | 11px / 0.6875rem | 400 | 1.5 | 0 | Mono | インラインコード |

### 3.3 Font Weight

| Token | Weight | 用途 |
|-------|--------|------|
| `regular` | 400 | 本文・説明テキスト |
| `medium` | 500 | 強調テキスト・バッジ |
| `semibold` | 600 | ラベル・ボタン・見出し（Heading） |
| `bold` | 700 | Display 見出し・カードタイトル強調 |
| `extrabold` | 800 | KPI 数値・インパクト強調 |
| `black` | 900 | ブランドロゴタイプ・1〜2 語の最大強調 |

#### Weight 選択ガイド

| ユースケース | 推奨 Weight | Font | 例 |
|-------------|------------|------|-----|
| ヒーロー見出し全体 | 700 (bold) | Serif | "The Renaissance of AI" |
| ヒーロー内のキーワード強調 | 900 (black) + イタリック | Serif | "*RenAIssance*" |
| セクション見出し | 700 (bold) | Serif | "Color System" |
| カードタイトル | 600 (semibold) | Serif | "Impasto Surface" |
| 本文中の強調 | 600 (semibold) | Sans | "すべての値は**トークン**から導出" |
| KPI・メトリクス数値 | 800 (extrabold) | Sans | "$12.5M" "99.9%" |
| ブランドロゴ | 900 (black) | Serif | "THE DOMAIN AI" |
| ボタンラベル | 600 (semibold) | Sans | "Get Started" |
| ナビゲーション（通常） | 400 (regular) | Sans | サイドバーリンク |
| ナビゲーション（アクティブ） | 600 (semibold) | Sans | 選択中のリンク |

> **注意**: Playfair Display は 400〜900 の可変ウェイトおよびイタリックに対応しています。Google Fonts 読み込み時に必要な weight を含めてください。
> ```html
> <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;0,800;0,900;1,400;1,700&family=Source+Sans+3:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
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
| `bp-tablet` | 640–1023px | Tablet / Mobile 横 |
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
| `radius-sm` | 3px | タグ・バッジ・チップ |
| `radius-md` | 6px | ボタン・インプット |
| `radius-lg` | 10px | カード・パネル |
| `radius-xl` | 14px | モーダル・ダイアログ |
| `radius-2xl` | 20px | 大型カード・フィーチャーパネル |
| `radius-full` | 9999px | アバター・完全ピル |

基本方針: digital 版よりやや控えめな角丸で、油絵のキャンバスフレームのような堅牢さを残します。**10px（`radius-lg`）** をカードの標準とし、ネスト要素は親より小さい radius を使用します。

### 6.2 Border & Stroke Width

| Token | Value | 用途 |
|-------|-------|------|
| `stroke-hairline` | 0.5px | 微細なセパレーター・装飾線 |
| `stroke-sm` | 1px | **ボーダー default**・カード境界・セパレーター |
| `stroke-md` | 1.5px | アイコンストローク・強調ボーダー |
| `stroke-lg` | 2px | フォーカスリング・アクティブ状態のボーダー |
| `stroke-xl` | 3px | 額縁風の装飾ボーダー・視覚的強調 |

基本方針: **1px（`stroke-sm`）** をデフォルトのボーダー幅とします。アイコンは **1.5px（`stroke-md`）** で統一します。

## 7. Material System

本デザインシステムの視覚表現を支える 2 つのマテリアルと、それらを補完するエフェクト群です。

### 7.1 Material Philosophy

油絵の技法体系に基づく 2 つのマテリアルを定義します。「厚塗り → 薄塗り」という絵画の基本構造で、情報の階層と重要度を直感的に伝えます。

| Material | メタファー | 特性 | 主な用途 |
|----------|-----------|------|----------|
| **Impasto** | 厚塗り・盛り上げ | 可視的なテクスチャ、重厚な存在感、力強い陰影 | ヒーロー、CTA、フィーチャーカード、ナビゲーション |
| **Glaze** | 薄塗り・透明釉 | 半透明の層の重なり、柔らかな色彩の深み、静的な佇まい | カード、パネル、サイドバー、オーバーレイ |

```
絵画技法の進化: Impasto ─── Glaze
                  存在感      透明感

                   Impasto           Glaze
                   ─────────────     ────────────
 テクスチャ        強い（粗い面）     なめらか（均一）
 背景との関係      前面に突出         背景を透かす
 ボーダー         金箔調の縁取り      柔らかい光の縁
 陰影             強いドロップ        内部グロウ
 色彩の深み       厚い単色の重なり    多色の透過レイヤ
```

#### Material Selection Guide

| ユースケース | 推奨マテリアル | 理由 |
|-------------|--------------|------|
| ヒーローセクション | Impasto | 厚塗りテクスチャで圧倒的な第一印象を演出 |
| CTA ボタン | Impasto | 盛り上がった質感で視線を強制的に集める |
| 料金カード（推奨プラン） | Impasto (gilded) | 金箔装飾で他プランと差別化 |
| コンテンツカード | Glaze | 読みやすさ優先、背景を穏やかに透過 |
| アプリヘッダー | Impasto (subtle) | テクスチャを抑えつつ存在感を確保 |
| サイドバー | Glaze (frosted) | 安定した視認性、主役はコンテンツ領域 |
| モーダル・ダイアログ | Glaze | 落ち着いた背景分離 |
| ツールチップ | Glaze (subtle) | 軽量で邪魔にならない |

### 7.2 Impasto — 厚塗りマテリアル

油絵の厚塗り技法を再現するマテリアルです。微細なノイズテクスチャ、深い陰影、そしてゴールドの縁取りにより、キャンバスの上に盛り上がった絵具のような存在感を表現します。

```css
/* ─── Dark Mode ─── */

/* Standard Impasto — ヒーロー・フィーチャーカードの基本 */
.impasto {
  position: relative;
  background:
    /* キャンバスノイズ */
    url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E"),
    linear-gradient(
      145deg,
      rgba(33, 29, 22, 0.95) 0%,        /* neutral-200 */
      rgba(24, 21, 15, 0.98) 100%        /* neutral-100 */
    );
  border: 1px solid rgba(223, 188, 110, 0.12);  /* gold-300 @ 12% */
  box-shadow:
    inset 0 1px 0 rgba(223, 188, 110, 0.08),    /* 上縁ゴールドハイライト */
    inset 0 -2px 4px rgba(0, 0, 0, 0.3),         /* 下部の深い影 */
    0 4px 16px rgba(0, 0, 0, 0.4),
    0 12px 40px rgba(0, 0, 0, 0.2);
}

/* Impasto Gilded — 金箔装飾付き（推奨プラン・特別カード） */
.impasto-gilded {
  position: relative;
  background:
    url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.8' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E"),
    linear-gradient(
      145deg,
      rgba(78, 59, 18, 0.2) 0%,          /* gold-800 */
      rgba(33, 29, 22, 0.95) 30%,
      rgba(24, 21, 15, 0.98) 100%
    );
  border: 1px solid rgba(204, 160, 68, 0.2);    /* gold-400 @ 20% */
  box-shadow:
    inset 0 1px 0 rgba(238, 214, 160, 0.12),    /* 上縁ゴールドグロウ */
    inset 0 -2px 4px rgba(0, 0, 0, 0.4),
    0 0 30px rgba(204, 160, 68, 0.08),            /* 金色のオーラ */
    0 8px 32px rgba(0, 0, 0, 0.4);
}

/* Impasto Vermillion — CTA・アクセントカード */
.impasto-vermillion {
  position: relative;
  background:
    url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E"),
    linear-gradient(
      145deg,
      rgba(184, 58, 36, 0.9) 0%,         /* accent-500 */
      rgba(113, 38, 24, 0.95) 100%        /* accent-700 */
    );
  border: 1px solid rgba(212, 90, 69, 0.2);     /* accent-400 @ 20% */
  box-shadow:
    inset 0 1px 0 rgba(240, 173, 163, 0.1),     /* 上縁ハイライト */
    inset 0 -2px 4px rgba(0, 0, 0, 0.3),
    0 0 24px rgba(184, 58, 36, 0.15),
    0 8px 32px rgba(0, 0, 0, 0.4);
  color: #faf5ed;                                 /* neutral-1000 */
}

/* Impasto Subtle — ヘッダー・ナビゲーション用 */
.impasto-subtle {
  position: relative;
  background:
    url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='1.0' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.02'/%3E%3C/svg%3E"),
    linear-gradient(
      180deg,
      rgba(24, 21, 15, 0.9) 0%,
      rgba(12, 10, 8, 0.95) 100%
    );
  border-bottom: 1px solid rgba(223, 188, 110, 0.06);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
}

/* ─── Light Mode ─── */

/* Light Impasto */
.impasto-light {
  position: relative;
  background:
    url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.02'/%3E%3C/svg%3E"),
    linear-gradient(
      145deg,
      rgba(250, 245, 237, 0.95) 0%,      /* neutral-1000 */
      rgba(236, 229, 216, 0.98) 100%      /* neutral-950 */
    );
  border: 1px solid rgba(196, 167, 140, 0.3);   /* secondary-300 @ 30% */
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.8),
    0 4px 16px rgba(42, 30, 20, 0.08);
}

/* Light Impasto Gilded */
.impasto-light-gilded {
  position: relative;
  background:
    url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.8' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.025'/%3E%3C/svg%3E"),
    linear-gradient(
      145deg,
      rgba(253, 248, 238, 0.9) 0%,       /* gold-50 */
      rgba(250, 245, 237, 0.95) 50%,
      rgba(248, 236, 208, 0.3) 100%       /* gold-100 */
    );
  border: 1px solid rgba(204, 160, 68, 0.2);
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.9),
    0 0 20px rgba(204, 160, 68, 0.06),
    0 4px 16px rgba(42, 30, 20, 0.06);
}
```

### 7.3 Glaze — 薄塗りマテリアル

油絵のグレーズ（薄塗り透明釉）技法を再現するマテリアルです。半透明の色彩レイヤーを重ね、背景が柔らかく透けて見える静かで深い佇まいを表現します。

```css
/* ─── Dark Mode ─── */

/* Standard Glaze — カード・パネルの基本 */
.glaze {
  background: rgba(24, 21, 15, 0.65);            /* neutral-100 @ 65% */
  backdrop-filter: blur(20px) saturate(1.1);
  -webkit-backdrop-filter: blur(20px) saturate(1.1);
  border: 1px solid rgba(236, 229, 216, 0.05);   /* neutral-950 @ 5% */
}

/* Frosted Glaze — より強い曇りで背景を遮断 */
.glaze-frosted {
  background: rgba(33, 29, 22, 0.82);            /* neutral-200 @ 82% */
  backdrop-filter: blur(36px) saturate(1.15);
  -webkit-backdrop-filter: blur(36px) saturate(1.15);
  border: 1px solid rgba(236, 229, 216, 0.07);
}

/* Tinted Glaze — ウルトラマリンを帯びた Glaze */
.glaze-tinted {
  background: rgba(17, 22, 48, 0.7);             /* primary-900 @ 70% */
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(90, 109, 184, 0.12);    /* primary-400 @ 12% */
}

/* Warm Glaze — バーントシエナを帯びた Glaze */
.glaze-warm {
  background: rgba(42, 30, 20, 0.6);             /* secondary-900 @ 60% */
  backdrop-filter: blur(20px) saturate(1.2);
  -webkit-backdrop-filter: blur(20px) saturate(1.2);
  border: 1px solid rgba(168, 132, 100, 0.1);    /* secondary-400 @ 10% */
}

/* ─── Light Mode ─── */

/* Light Glaze */
.glaze-light {
  background: rgba(250, 246, 243, 0.6);          /* secondary-50 @ 60% */
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.6);
}

/* Light Frosted Glaze */
.glaze-light-frosted {
  background: rgba(240, 232, 224, 0.65);         /* secondary-100 @ 65% */
  backdrop-filter: blur(36px) saturate(1.2);
  -webkit-backdrop-filter: blur(36px) saturate(1.2);
  border: 1px solid rgba(255, 255, 255, 0.7);
}

/* Light Tinted Glaze */
.glaze-light-tinted {
  background: rgba(212, 218, 240, 0.5);          /* primary-100 @ 50% */
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.5);
}
```

### 7.4 Gradients

```css
/* ─── Dark Mode ─── */

/* Hero Gradient — ルネサンス絵画のキアロスクーロ（明暗法） */
--gradient-hero: radial-gradient(
  ellipse 70% 50% at 50% 20%,
  rgba(61, 79, 158, 0.18) 0%,          /* primary-500 */
  rgba(184, 58, 36, 0.05) 40%,         /* accent-500 微量 */
  rgba(12, 10, 8, 0) 70%
);

/* Surface Gradient — カード・パネル背景 */
--gradient-surface: linear-gradient(
  170deg,
  rgba(44, 39, 32, 0.5) 0%,            /* neutral-300 */
  rgba(24, 21, 15, 0.85) 100%          /* neutral-100 */
);

/* Gold Gradient — CTA・アクセント装飾 */
--gradient-gold: linear-gradient(
  135deg,
  #b38628 0%,                           /* gold-500 */
  #dfbc6e 50%,                          /* gold-300 */
  #cca044 100%                          /* gold-400 */
);

/* Vermillion Gradient — CTA ボタン */
--gradient-vermillion: linear-gradient(
  135deg,
  #93301e 0%,                           /* accent-600 */
  #b83a24 40%,                          /* accent-500 */
  #d45a45 100%                          /* accent-400 */
);

/* Text Gradient — 見出し装飾 */
--gradient-text: linear-gradient(
  90deg,
  #ece5d8 0%,                           /* neutral-950 */
  #dfbc6e 100%                          /* gold-300 */
);

/* Mesh Gradient — ヒーロー・プレゼン背景 */
--gradient-mesh:
  radial-gradient(at 15% 25%, rgba(61, 79, 158, 0.15) 0%, transparent 50%),
  radial-gradient(at 75% 65%, rgba(184, 58, 36, 0.08) 0%, transparent 45%),
  radial-gradient(at 50% 80%, rgba(204, 160, 68, 0.06) 0%, transparent 50%);

/* Canvas Gradient — Impasto の下地 */
--gradient-canvas: linear-gradient(
  145deg,
  rgba(33, 29, 22, 0.6) 0%,
  rgba(24, 21, 15, 0.8) 50%,
  rgba(33, 29, 22, 0.6) 100%
);

/* ─── Light Mode ─── */

/* Light Hero Gradient */
--gradient-hero-light: radial-gradient(
  ellipse 70% 50% at 50% 20%,
  rgba(212, 218, 240, 0.5) 0%,          /* primary-100 */
  rgba(249, 216, 211, 0.2) 40%,         /* accent-100 微量 */
  rgba(250, 245, 237, 0) 70%
);

/* Light Surface Gradient */
--gradient-surface-light: linear-gradient(
  170deg,
  rgba(250, 246, 243, 0.8) 0%,          /* secondary-50 */
  rgba(250, 245, 237, 0.95) 100%        /* neutral-1000 */
);

/* Light Warm Gradient */
--gradient-warm-light: linear-gradient(
  135deg,
  #faf6f3 0%,                           /* secondary-50 */
  #f0e8e0 50%,                          /* secondary-100 */
  #fdf8ee 100%                          /* gold-50 */
);

/* Light Mesh Gradient */
--gradient-mesh-light:
  radial-gradient(at 15% 25%, rgba(169, 181, 225, 0.3) 0%, transparent 50%),
  radial-gradient(at 75% 65%, rgba(249, 216, 211, 0.2) 0%, transparent 45%),
  radial-gradient(at 50% 80%, rgba(248, 236, 208, 0.25) 0%, transparent 50%);
```

### 7.5 Glow Effects

#### Basic — box-shadow ベース

油絵に描かれたキャンドルライトのような温かみのある発光エフェクトです。

```css
/* Subtle Glow — ホバー・フォーカス */
--glow-subtle: 0 0 16px rgba(223, 188, 110, 0.1);

/* Medium Glow — CTA・アクティブ要素 */
--glow-medium: 0 0 30px rgba(223, 188, 110, 0.18),
               0 0 60px rgba(204, 160, 68, 0.06);

/* Strong Glow — ヒーロー・アクセント */
--glow-strong: 0 0 40px rgba(223, 188, 110, 0.22),
               0 0 80px rgba(204, 160, 68, 0.1),
               0 0 160px rgba(184, 58, 36, 0.04);

/* Vermillion Glow — CTA ボタン用 */
--glow-vermillion: 0 0 24px rgba(184, 58, 36, 0.2),
                   0 0 60px rgba(184, 58, 36, 0.08);

/* Glow Ring — フォーカスインジケーター */
--glow-ring: 0 0 0 2px rgba(46, 59, 120, 0.7),
             0 0 10px rgba(61, 79, 158, 0.25);
```

#### Gradients — background ベース

```css
/* Radial Glow — 要素中心からの温かいオーラ */
--glow-gradient-radial: radial-gradient(
  ellipse 60% 60% at 50% 50%,
  rgba(223, 188, 110, 0.1) 0%,
  transparent 70%
);

/* Edge Glow — 上縁からのゴールドグロウ */
--glow-gradient-edge: linear-gradient(
  180deg,
  rgba(223, 188, 110, 0.12) 0%,
  rgba(204, 160, 68, 0.03) 30%,
  transparent 60%
);

/* Ambient Glow — 複数のラディアルを重ねた環境光 */
--glow-gradient-ambient:
  radial-gradient(at 20% 30%, rgba(61, 79, 158, 0.08) 0%, transparent 50%),
  radial-gradient(at 80% 70%, rgba(184, 58, 36, 0.05) 0%, transparent 50%);

/* Candlelight Glow — キャンドルの揺らぐ光 */
--glow-gradient-candlelight: radial-gradient(
  ellipse 40% 60% at 50% 40%,
  rgba(223, 188, 110, 0.12) 0%,
  rgba(204, 160, 68, 0.04) 40%,
  transparent 70%
);
```

### 7.6 Shadows (Elevation)

ダーク UI では shadow に加え、Impasto テクスチャの隆起感と Gold ボーダーの光で高さを表現します。

| Token | Value | 用途 |
|-------|-------|------|
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.5)` | 微小な浮き |
| `shadow-md` | `0 4px 14px rgba(0,0,0,0.45)` | カード・ドロップダウン |
| `shadow-lg` | `0 10px 36px rgba(0,0,0,0.5)` | モーダル・ポップオーバー |
| `shadow-xl` | `0 20px 56px rgba(0,0,0,0.6)` | フルスクリーンオーバーレイ |

### 7.7 Decorative Lines & Separators

```css
/* Standard Separator — Raw Umber の境界線 */
--separator: 1px solid var(--neutral-300);         /* #2c2720 */

/* Gold Separator — ゴールドの輝く区切り線 */
--separator-gold: 1px solid rgba(223, 188, 110, 0.15);

/* Gradient Line — セクション区切り（キアロスクーロ） */
--line-gradient: linear-gradient(
  90deg,
  transparent 0%,
  rgba(223, 188, 110, 0.2) 30%,
  rgba(204, 160, 68, 0.25) 50%,
  rgba(223, 188, 110, 0.2) 70%,
  transparent 100%
);

/* Ornament Line — 額縁風の装飾ライン */
--line-ornament: linear-gradient(
  90deg,
  transparent 0%,
  rgba(204, 160, 68, 0.05) 10%,
  rgba(223, 188, 110, 0.18) 25%,
  rgba(238, 214, 160, 0.25) 50%,
  rgba(223, 188, 110, 0.18) 75%,
  rgba(204, 160, 68, 0.05) 90%,
  transparent 100%
);

/* Canvas Line — キャンバスの織り目風 */
--line-canvas: linear-gradient(
  90deg,
  transparent 0%,
  rgba(142, 130, 114, 0.15) 20%,
  rgba(142, 130, 114, 0.2) 50%,
  rgba(142, 130, 114, 0.15) 80%,
  transparent 100%
);
```

### 7.8 Canvas Texture

ページ背景やヒーローセクションに適用するキャンバステクスチャです。SVG ベースのノイズで油絵のキャンバス地を表現します。

```css
/* Canvas Noise — ページ全体の背景テクスチャ */
.canvas-texture {
  background-color: var(--neutral-0);             /* #0c0a08 */
  background-image:
    url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='canvas'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='5' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23canvas)' opacity='0.025'/%3E%3C/svg%3E");
}

/* Canvas Warm — 温かみのあるキャンバス（LP 向け） */
.canvas-warm {
  background-color: var(--neutral-0);
  background-image:
    url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='canvas'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='5' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23canvas)' opacity='0.03'/%3E%3C/svg%3E"),
    var(--gradient-mesh);
}
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
| `duration-normal` | 300ms | パネル展開・フェード |
| `duration-slow` | 500ms | モーダル表示 |
| `duration-slower` | 800ms | ページ遷移・ドラマティック演出 |

### 9.2 Easing

| Token | Value | 用途 |
|-------|-------|------|
| `ease-default` | `cubic-bezier(0.25, 0.1, 0.25, 1)` | 汎用 |
| `ease-in` | `cubic-bezier(0.4, 0, 1, 1)` | 退出アニメーション |
| `ease-out` | `cubic-bezier(0, 0, 0.2, 1)` | 出現アニメーション |
| `ease-brush` | `cubic-bezier(0.22, 1, 0.36, 1)` | 筆致を模した有機的な緩急 |

### 9.3 Hover Patterns

#### Impasto Shift — CTA・プライマリボタン

厚塗りのテクスチャが浮き上がり、ゴールドのグロウが広がるパターンです。

```css
.btn-impasto {
  padding: 0.9em 1.6em;
  min-width: 120px;
  min-height: 44px;
  font-family: var(--font-sans);
  font-size: 1rem;
  font-weight: 600;
  border: 1px solid rgba(223, 188, 110, 0.15);
  border-radius: 6px;
  color: #faf5ed;
  cursor: pointer;
  transition: all 0.5s cubic-bezier(0.22, 1, 0.36, 1);
  background:
    url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E"),
    linear-gradient(
      145deg,
      #93301e 0%,        /* accent-600 */
      #b83a24 50%,       /* accent-500 */
      #93301e 100%
    );
  box-shadow:
    inset 0 1px 0 rgba(240, 173, 163, 0.12),
    inset 0 -2px 4px rgba(0, 0, 0, 0.2),
    0 4px 16px rgba(184, 58, 36, 0.2);
}

.btn-impasto:hover {
  transform: translateY(-2px);
  box-shadow:
    inset 0 1px 0 rgba(240, 173, 163, 0.18),
    inset 0 -2px 4px rgba(0, 0, 0, 0.2),
    0 0 24px rgba(184, 58, 36, 0.25),
    0 8px 32px rgba(0, 0, 0, 0.3);
}

.btn-impasto:is(:focus, :focus-visible, :active) {
  outline: none;
  box-shadow:
    0 0 0 2px #faf5ed,
    0 0 0 5px #3d4f9e;
}
```

#### Glaze Line — セカンダリ・ゴーストボタン

底辺にゴールドラインが浮かび、Glaze の透明感が深まるパターンです。

```css
.btn-glaze {
  min-width: 120px;
  position: relative;
  cursor: pointer;
  padding: 12px 20px;
  border: 0;
  border-radius: 6px;
  box-shadow: inset 0 0 0 1px rgba(236, 229, 216, 0.08);
  background: radial-gradient(
    ellipse at bottom,
    #3a342b 0%,         /* neutral-400 */
    #18150f 50%         /* neutral-100 */
  );
  color: rgba(236, 229, 216, 0.65);  /* neutral-950 @ 65% */
  font-family: var(--font-sans);
  font-weight: 600;
  transition: all 0.8s cubic-bezier(0.22, 1, 0.36, 1);
}

.btn-glaze::before {
  content: "";
  width: 60%;
  height: 1px;
  position: absolute;
  bottom: 0;
  left: 20%;
  background: linear-gradient(
    90deg,
    transparent 0%,
    #dfbc6e 50%,        /* gold-300 */
    transparent 100%
  );
  opacity: 0.15;
  transition: all 0.8s cubic-bezier(0.22, 1, 0.36, 1);
}

.btn-glaze:hover {
  color: #ece5d8;       /* neutral-950 */
  transform: scale(1.05) translateY(-2px);
}

.btn-glaze:hover::before {
  opacity: 0.7;
  width: 80%;
  left: 10%;
}
```

#### Canvas Hover — Impasto カード

ホバー時にキャンバスのテクスチャが際立ち、ゴールドの額縁ボーダーが浮かぶパターンです。

```css
.card-impasto {
  position: relative;
  padding: 24px;
  border: 1px solid rgba(223, 188, 110, 0.08);
  border-radius: 10px;
  cursor: pointer;
  transition: all 0.5s cubic-bezier(0.22, 1, 0.36, 1);
  background:
    url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.025'/%3E%3C/svg%3E"),
    linear-gradient(
      145deg,
      rgba(33, 29, 22, 0.9) 0%,
      rgba(24, 21, 15, 0.95) 100%
    );
  box-shadow:
    inset 0 1px 0 rgba(223, 188, 110, 0.05),
    0 2px 8px rgba(0, 0, 0, 0.3);
}

.card-impasto:hover {
  border-color: rgba(223, 188, 110, 0.18);
  transform: translateY(-3px);
  box-shadow:
    inset 0 1px 0 rgba(223, 188, 110, 0.1),
    0 0 20px rgba(223, 188, 110, 0.06),
    0 8px 32px rgba(0, 0, 0, 0.35);
}
```

### 9.4 Animation Patterns

```css
/* Fade In — キャンバスから浮かび上がる出現 */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(12px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* Golden Pulse — ゴールドの脈動グロウ */
@keyframes goldenPulse {
  0%, 100% { box-shadow: 0 0 16px rgba(223, 188, 110, 0.06); }
  50%      { box-shadow: 0 0 32px rgba(223, 188, 110, 0.15); }
}

/* Shimmer — スケルトンローディング（金色の筆致） */
@keyframes shimmer {
  from { background-position: -200% 0; }
  to   { background-position: 200% 0; }
}
/* Usage: background: linear-gradient(90deg, #18150f 25%, #2c2720 50%, #18150f 75%); background-size: 200% 100%; */

/* Candlelight — キャンドルの揺らぎ */
@keyframes candlelight {
  0%   { opacity: 0.85; filter: brightness(1); }
  25%  { opacity: 0.92; filter: brightness(1.02); }
  50%  { opacity: 0.88; filter: brightness(0.98); }
  75%  { opacity: 0.95; filter: brightness(1.01); }
  100% { opacity: 0.85; filter: brightness(1); }
}

/* Brushstroke — 筆致が描かれる出現 */
@keyframes brushstroke {
  from {
    clip-path: inset(0 100% 0 0);
    opacity: 0.5;
  }
  to {
    clip-path: inset(0 0 0 0);
    opacity: 1;
  }
}
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

- ページ全体に `.canvas-warm`（キャンバステクスチャ + Mesh Gradient）を背景に適用
- ヒーローには `gradient-hero` を重ね、`.impasto` パネルで厚塗りの迫力を演出
- セクション間は `space-9`（64px）以上の余白
- CTA ボタンは `.btn-impasto`（Vermillion）で視線を集中させる
- 料金表の推奨プランには `.impasto-gilded` を適用し、他プランは `.glaze` で差別化
- タイポグラフィは Serif 体の `display-xl`〜`display-md` をヒーローに使用
- セクション区切りには `--line-ornament` を使用

### 11.2 Web App

- サーフェス階層を厳密に守る: `bg-page` → `bg-surface` → `bg-surface-raised`
- ページ背景に `.canvas-texture` を適用し、微細なキャンバス質感を全体に与える
- サイドバーには `.glaze-frosted` を適用し、コンテンツ領域との境界を柔らかく表現
- ヘッダーには `.impasto-subtle` を適用し、ナビゲーションに存在感を与える
- インタラクティブ要素には必ず `focus-ring`（`glow-ring`）を適用
- 本文は Sans 体の `body-md`（14px）、密度の高い UI では `body-sm`（12px）

### 11.3 Mobile App (iOS)

- iOS Human Interface Guidelines を優先し、トークンで色・タイポを上書き
- タッチターゲット: 最小 44×44pt
- Spacing: `space-4`（12px）を最小パディング
- SF Pro を基本フォントとし、カラートークンのみ本システムから適用
- Dynamic Type をサポートし、Type Scale は参考値として扱う
- キャンバステクスチャはパフォーマンスを考慮し、背景色のみでフォールバック

### 11.4 Visual Presentation

- アスペクト比: **16:9**（1920×1080）
- 背景: `neutral-0` + `.canvas-warm` + `gradient-mesh`
- タイトル: `display-xl`（64px）、Playfair Display Bold 700
- 本文: `body-lg`（16px）以上（視認性確保）
- コードブロック: `mono-md`、`.glaze` 背景 + `radius-lg`
- キーワード・数値強調には `glow-medium` + `gradient-text`（ゴールドグラデーション）
- セクション区切りに `--line-ornament` を使用
- 余白はデスクトップより大きく取る（`space-8` 以上）

## 12. Usage Quick Reference

### 12.1 Material Layer Map

```
┌─ Page: neutral-0 (#0c0a08) + canvas-warm ──────────────────────────┐
│                                                                       │
│  ┌─ Header ▸ impasto-subtle ───────────────────────────────────┐    │
│  │  Logo + Nav    gold border-bottom                            │    │
│  └──────────────────────────────────────────────────────────────┘    │
│                                                                       │
│  ┌─ Sidebar ▸ glaze-frosted ───┐  ┌─ Content Area ──────────────┐  │
│  │  Nav items: glaze on hover   │  │                              │  │
│  │                              │  │  ┌─ Card ▸ glaze ─────────┐  │  │
│  │                              │  │  │  Heading → #faf5ed      │  │  │
│  │                              │  │  │  Body    → #ece5d8      │  │  │
│  │                              │  │  │  Sub     → #8e8272      │  │  │
│  │                              │  │  └─────────────────────────┘  │  │
│  │                              │  │                              │  │
│  │                              │  │  ┌─ CTA ▸ btn-impasto ────┐  │  │
│  │                              │  │  │  Vermillion gradient     │  │  │
│  │                              │  │  │  Gold glow on hover      │  │  │
│  │                              │  │  └─────────────────────────┘  │  │
│  └──────────────────────────────┘  └──────────────────────────────┘  │
│                                                                       │
│  ┌─ Hero ▸ impasto + gradient-hero ─────────────────────────────┐  │
│  │  display-xl Serif title, gold text gradient                    │  │
│  │  CTA: impasto-vermillion + glow-vermillion                     │  │
│  └──────────────────────────────────────────────────────────────┘    │
└───────────────────────────────────────────────────────────────────────┘
```

### 12.2 Material × Component 早見表

| Component | Default | Accent | Light Mode |
|-----------|---------|--------|------------|
| Card | `.glaze` | `.impasto` | `.glaze-light-frosted` |
| Header | `.impasto-subtle` | — | `.impasto-light` |
| Sidebar | `.glaze-frosted` | — | `.glaze-light-frosted` |
| Button (Primary) | `.btn-impasto` | `.impasto-vermillion` | 同左 |
| Button (Secondary) | `.btn-glaze` | — | 同左 |
| Modal | `.glaze-frosted` | — | `.glaze-light-frosted` |
| Tooltip | `.glaze` (small) | — | `.glaze-light` |
| Pricing (Featured) | `.glaze` | `.impasto-gilded` | `.impasto-light-gilded` |

### 12.3 ステータス表示

```
Success  → アイコン: success-400, テキスト: success-500, 背景: success-900
Warning  → アイコン: warning-400, テキスト: warning-500, 背景: warning-900
Error    → アイコン: error-400,   テキスト: error-500,   背景: error-900
Info     → アイコン: info-400,    テキスト: info-500,    背景: info-900
```

## 13. Component Guidelines

UI コンポーネントの仕様をここで定義します。すべてのコンポーネントはデザイントークンから値を導出し、2 つのマテリアル（Impasto / Glaze）を用途に応じて適用します。

### 13.1 Button

#### Variants

| Variant | Background | Text | Border | 用途 |
|---------|-----------|------|--------|------|
| **Primary** | `cta` (accent-500) | neutral-1000 (#faf5ed) | gold-300 @ 15% | CTA・主要アクション |
| **Secondary** | transparent | `text-primary` | `stroke-sm` solid `border-default` | 補助アクション |
| **Ghost** | transparent | `text-secondary` | none | 最小限のアクション |
| **Danger** | error-500 | neutral-1000 (#faf5ed) | none | 破壊的アクション |

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
| Hover | Primary → `.btn-impasto` hover / Secondary → `.btn-glaze` hover |
| Active / Pressed | opacity: 0.85、transform: scale(0.98) |
| Focus | `glow-ring`（0 0 0 2px primary-600, 0 0 10px primary-500 @ 25%） |
| Disabled | opacity: 0.35、cursor: not-allowed |
| Loading | テキストを spinner に差し替え、pointer-events: none |

#### ライトモード差分

- Primary: background は同じ accent-500、text は neutral-1000
- Secondary: border-color → `border-default`（secondary-200）
- Ghost: text → `text-secondary`（neutral-600）

### 13.2 Card

| Property | Value |
|----------|-------|
| Background | `bg-surface` |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-lg` (10px) |
| Padding | `space-5` (16px) ～ `space-6` (24px) |
| Hover（optional） | border-color → gold-300 @ 18%、transition `duration-normal` |

#### Card Variants by Material

| Variant | Class | 用途 |
|---------|-------|------|
| **Glaze Card** | `.glaze` + `radius-lg` | 一般的なコンテンツカード |
| **Impasto Card** | `.card-impasto` | フィーチャーカード・ヒーロー内 |
| **Gilded Card** | `.impasto-gilded` | 推奨プラン・特別カード |

```css
/* Glaze Card */
.card-glaze {
  background: rgba(24, 21, 15, 0.65);
  backdrop-filter: blur(20px) saturate(1.1);
  -webkit-backdrop-filter: blur(20px) saturate(1.1);
  border: 1px solid rgba(236, 229, 216, 0.05);
  border-radius: 10px;
  padding: 24px;
}
```

#### ライトモード差分

- Background: `bg-surface`（secondary-50 → #faf6f3）
- Border: `border-default`（secondary-200 → #dcc8b5）
- Glaze Card → `.glaze-light-frosted` を使用

### 13.3 Input / Text Field

| Property | Value |
|----------|-------|
| Background | `bg-surface` |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-md` (6px) |
| Height | 40px（md）/ 32px（sm） |
| Padding | 0 `space-4` (12px) |
| Font | Sans `body-md` (14px) |
| Text Color | `text-primary` |
| Placeholder | `text-muted` |

#### States

| State | 変化 |
|-------|------|
| Default | 上記の通り |
| Hover | border-color → `border-hover` |
| Focus | border-color → `interactive`、`glow-ring` 適用 |
| Error | border-color → error-500、`glow-ring` を error-500 基調に差し替え |
| Disabled | background → neutral-200、opacity: 0.45 |

#### ライトモード差分

- Background: `bg-surface-raised`（#faf5ed）
- Border: `border-default`（secondary-200）
- Text: `text-primary`（neutral-200 → #211d16）

### 13.4 Badge / Tag

| Property | Value |
|----------|-------|
| Height | 22px |
| Padding | 0 `space-3` (8px) |
| Font | Sans `label-sm` (11px), medium |
| Radius | `radius-sm` (3px) |
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
| Material | `.glaze-frosted` |
| Background | `bg-surface-raised` or Glaze variant |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-xl` (14px) |
| Shadow | `shadow-lg` |
| Max Width | `container-sm` (640px) |
| Padding | `space-6` (24px) ～ `space-7` (32px) |
| Overlay | neutral-0 @ 65% opacity + `backdrop-filter: blur(8px)` |
| Entry Animation | `fadeIn` `duration-slow` `ease-brush` |

### 13.6 Toast / Notification

| Property | Value |
|----------|-------|
| Background | neutral-400 |
| Text Color | `text-primary` |
| Font | Sans `body-md` (14px) |
| Radius | `radius-md` (6px) |
| Padding | `space-3` (8px) `space-5` (16px) |
| Position | fixed、bottom: 24px、center |
| z-index | `z-toast` (400) |
| Animation | fadeIn + translateY(20px → 0)、`duration-normal` |
| Auto Dismiss | 3000ms default |

### 13.7 Navigation / Sidebar

| Property | Value |
|----------|-------|
| Material | `.glaze-frosted`（推奨）/ `bg-surface`（フォールバック） |
| Width | 240px ～ 280px |
| Border Right | `stroke-sm` solid `border-default` |
| Nav Item Height | 36px |
| Nav Item Padding | `space-3` (8px) `space-4` (12px) |
| Nav Item Font | Sans `body-md` (14px) |
| Nav Item Radius | `radius-md` (6px) |
| Active State | background → neutral-200、text → `text-primary`、font-weight: 600 |
| Hover State | background → neutral-200、text → `text-primary` |

サイドバーには `.glaze-frosted` を標準適用し、コンテンツ領域との境界を柔らかく表現します。
ヘッダーバーには `.impasto-subtle` を適用し、キャンバステクスチャのある存在感を与えます。

### 13.8 Table

| Property | Value |
|----------|-------|
| Header Font | Sans `label-md` (13px), semibold, uppercase |
| Header Color | `text-secondary` |
| Header Border Bottom | `stroke-sm` solid `border-default` |
| Cell Font | Sans `body-md` (14px) |
| Cell Padding | `space-5` (16px) |
| Row Border Bottom | `stroke-hairline` solid neutral-200 |
| Row Hover | background → neutral-100 |
| Mono Values | `mono-md` を使用（数値・コード） |

## 14. Paint

### 14.1 概要

Utopia デザインシステムでは、ルネサンス期の油絵の質感がすべてのビジュアル表現の基盤です。AI 画像生成（DALL-E, Midjourney, Stable Diffusion 等）でイラスト・背景・装飾画像を作成する際は、以下のプロンプトテンプレートを使用し、デザインシステム全体との視覚的一貫性を確保します。

### 14.2 Base Prompt Template

```
A classical Renaissance oil painting in the style of the reference image.
Muted, earthy color palette with deep greens, warm ivories, and cloudy blues.
Aged, rich texture with smooth, meticulous brushwork (sfumato) on fabric folds and foliage.
A detailed landscape background with tall pine trees, rolling hills, and a serene, cloudy sky.
[Insert description of subject here, e.g., A portrait of a young noblewoman in classical robes].
No modern elements or text.
```

### 14.3 プロンプト構成要素

| 要素 | 説明 | デザインシステムとの対応 |
|------|------|--------------------------|
| **Style** | `classical Renaissance oil painting` | Design Principle #1: Old Masters' Canvas |
| **Color palette** | `Muted, earthy color palette with deep greens, warm ivories, and cloudy blues` | Color System: Secondary (Burnt Sienna), Neutral (Raw Umber Canvas), Primary (Ultramarine) |
| **Texture** | `Aged, rich texture with smooth, meticulous brushwork (sfumato)` | Material: Impasto テクスチャ + Glaze の透明感 |
| **Background** | `detailed landscape background with tall pine trees, rolling hills, and a serene, cloudy sky` | Gradient: gradient-mesh の多層構造 |
| **Subject** | `[Insert description of subject here]` | 用途に応じて差し替え |
| **Constraint** | `No modern elements or text` | Design Principle #3: Chromatic Depth（彩度を抑えた重厚な色彩） |

### 14.4 Subject Variants

用途に応じた Subject の記述例です。

| 用途 | Subject 記述例 |
|------|---------------|
| ヒーロー背景 | `A sweeping Tuscan landscape at golden hour, rolling hills fading into mist` |
| ポートレート | `A portrait of a young noblewoman in classical robes, gazing serenely to the left` |
| 静物画 | `A still life with golden vessels, draped velvet fabric, and scattered autumn leaves on a marble table` |
| プロダクト紹介 | `An open leather-bound book resting on an ornate wooden desk, candlelight illuminating the pages` |
| チーム紹介 | `A gathering of scholars in a Renaissance studiolo, surrounded by globes and manuscripts` |

### 14.5 カラー調整ガイド

生成画像がデザインシステムのカラーパレットと調和するよう、以下を追加指示として使用します。

| 調整目的 | 追加プロンプト |
|----------|---------------|
| ダークモード適合 | `Dark, moody atmosphere with warm candlelight. Dominant tones: raw umber (#2a1e14), deep ivory (#ece5d8), gold ochre (#dfbc6e).` |
| ライトモード適合 | `Bright, airy atmosphere with soft natural light. Dominant tones: warm ivory (#faf5ed), soft sienna (#c4a78c), muted blue (#a9b5e1).` |
| アクセント強調 | `A focal point of deep vermillion red (#b83a24) in the subject's garment or accessory.` |
| ゴールド装飾 | `Gold leaf accents and gilded frame elements, warm gold tones (#dfbc6e, #cca044).` |

### 14.6 生成パラメータ推奨値

| パラメータ | 推奨値 | 備考 |
|-----------|--------|------|
| Aspect Ratio | 16:9（背景）, 3:4（ポートレート）, 1:1（アイコン） | 用途に合わせる |
| Style Strength | 高（70-90%） | 古典絵画らしさを維持 |
| Detail Level | 高 | sfumato の繊細な筆致を再現 |
| Color Temperature | Warm | デザインシステムの暖色基調に合わせる |

### 14.7 Samples

#### Sample 1 — Tuscan Landscape（ヒーロー背景）

```
Prompt:
A classical Renaissance oil painting in the style of the reference image.
Muted, earthy color palette with deep greens, warm ivories, and cloudy blues.
Aged, rich texture with smooth, meticulous brushwork (sfumato) on fabric folds and foliage.
A detailed landscape background with tall pine trees, rolling hills, and a serene, cloudy sky.
A sweeping Tuscan landscape at golden hour, rolling hills fading into mist.
No modern elements or text.
```

用途: ヒーローセクション背景、LP のキービジュアル

#### Sample 2 — Noblewoman Portrait（ポートレート）

```
Prompt:
A classical Renaissance oil painting in the style of the reference image.
Muted, earthy color palette with deep greens, warm ivories, and cloudy blues.
Aged, rich texture with smooth, meticulous brushwork (sfumato) on fabric folds and foliage.
A detailed landscape background with tall pine trees, rolling hills, and a serene, cloudy sky.
A portrait of a young noblewoman in classical robes, gazing serenely to the left.
No modern elements or text.
```

用途: About ページ、チーム紹介のビジュアル要素

#### Sample 3 — Scholar's Study（静物画）

```
Prompt:
A classical Renaissance oil painting in the style of the reference image.
Muted, earthy color palette with deep greens, warm ivories, and cloudy blues.
Aged, rich texture with smooth, meticulous brushwork (sfumato) on fabric folds and foliage.
A detailed landscape background with tall pine trees, rolling hills, and a serene, cloudy sky.
An open leather-bound book resting on an ornate wooden desk, candlelight illuminating the pages.
No modern elements or text.
```

用途: プロダクト紹介、ブログのアイキャッチ
