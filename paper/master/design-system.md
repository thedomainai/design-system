# The Domain AI Company Design System — Paper

The Domain AI Company の紙質感デザインシステムです。
インクと紙だけで構成されたエディトリアルデザインを基盤に、色を極限まで排除したモノクロームの世界で情報階層を表現します。
Web Page / Web App / Mobile App / Visual Presentation の全アウトプットで統一的に使用します。

## 1. Design Principles

| # | 原則 | 説明 |
|---|------|------|
| 1 | **Paper-First** | 紙とインクだけで成立するデザイン。色に頼らず、書体・太さ・サイズ・余白で情報の重みを伝える |
| 2 | **Monochrome Discipline** | 使用色は黒・白・グレーのみ。色が必要な場面でも最小限のグレー濃淡で代替する |
| 3 | **Typographic Hierarchy** | 見出しのセリフ体と本文のサンセリフ体の対比、ウェイトとサイズの段階で構造を表現する |
| 4 | **Generous Whitespace** | 紙面の余白は情報そのもの。余白の量と質で読みやすさと格調を生み出す |
| 5 | **Ink Economy** | すべての要素に「本当にインクを使う価値があるか」を問う。装飾を排し、必要最小限の線と文字で構成する |


## 2. Color System

### 2.1 Color Palette

#### Ink — Black Scale

テキスト・ボーダー・アイコンを構成するインクスケールです。紙の上のインクの濃淡を表現します。

| Token | Hex | 用途 |
|-------|-----|------|
| `ink-1000` | `#000000` | 見出し・最大強調 |
| `ink-900` | `#1a1a1a` | 本文テキスト |
| `ink-800` | `#2d2d2d` | 強調テキスト |
| `ink-700` | `#404040` | アクティブ要素 |
| `ink-600` | `#525252` | セカンダリテキスト |
| `ink-500` | `#6b6b6b` | キャプション |
| `ink-400` | `#8a8a8a` | プレースホルダ |
| `ink-300` | `#a3a3a3` | 非活性テキスト |
| `ink-200` | `#c4c4c4` | 薄いボーダー |
| `ink-100` | `#e0e0e0` | セパレーター |
| `ink-50` | `#f0f0f0` | 微細な区切り線 |

#### Paper — White Scale

背景・サーフェスを構成する紙色スケールです。暖色系の白で自然な紙の質感を表現します。

| Token | Hex | 用途 |
|-------|-----|------|
| `paper-white` | `#fdfdfc` | ページ背景（上質紙） |
| `paper-cream` | `#faf9f7` | カード背景（生成り） |
| `paper-warm` | `#f5f4f0` | セクション背景（クラフト紙） |
| `paper-kraft` | `#eeedea` | サイドバー・ヘッダー背景 |
| `paper-aged` | `#e8e7e3` | ホバー状態・アクティブ背景 |
| `paper-shadow` | `#dddcd8` | 影の表現・押下状態 |

### 2.2 Semantic Tokens

用途に基づく意味的トークンです。実装時はこちらを優先して使用します。

| Semantic Token | Maps To | Hex | 用途 |
|----------------|---------|-----|------|
| `bg-page` | paper-white | `#fdfdfc` | ページ全体の背景 |
| `bg-surface` | paper-cream | `#faf9f7` | カード・パネル背景 |
| `bg-surface-raised` | paper-white | `#fdfdfc` | モーダル・浮上パネル |
| `bg-recessed` | paper-warm | `#f5f4f0` | 凹んだ領域・インプット背景 |
| `border-default` | ink-100 | `#e0e0e0` | 通常のボーダー |
| `border-strong` | ink-200 | `#c4c4c4` | 強調ボーダー |
| `border-heavy` | ink-1000 | `#000000` | ヘッダー下線・重要な区切り |
| `text-primary` | ink-900 | `#1a1a1a` | 本文テキスト |
| `text-heading` | ink-1000 | `#000000` | 見出し |
| `text-secondary` | ink-600 | `#525252` | 補助テキスト |
| `text-muted` | ink-400 | `#8a8a8a` | 非活性・ヒントテキスト |
| `text-caption` | ink-500 | `#6b6b6b` | キャプション・注釈 |
| `interactive` | ink-900 | `#1a1a1a` | ボタン・リンク |
| `interactive-hover` | ink-700 | `#404040` | ホバー状態 |
| `focus-ring` | ink-700 | `#404040` | フォーカスインジケーター |

### 2.3 Status Indication

Paper テーマではステータスも色に頼りません。テキストラベル・アイコン形状・パターンで状態を伝えます。

| Status | テキスト表現 | 記号 | 背景 | ボーダー |
|--------|------------|------|------|----------|
| **Success** | `ink-900` + ラベル「Complete」 | `[done]` ✓ | `paper-warm` | `ink-200` |
| **Warning** | `ink-900` + ラベル「Attention」 | `[!]` | `paper-warm` | `ink-300` |
| **Error** | `ink-900` + ラベル「Error」 | `[x]` | `paper-warm` | `ink-700` 2px |
| **Info** | `ink-600` + ラベル「Note」 | `[i]` | `paper-cream` | `ink-100` |

どうしても色が必要な場面（データ可視化・ステータスバッジの即座の識別）に限り、以下の抑制されたパレットを使用します。

| Status | Hex | 用途制限 |
|--------|-----|----------|
| **Success** | `#16a34a` | データチャート・ステータスドット（直径 6px 以下）のみ |
| **Error** | `#dc2626` | データチャート・ステータスドット（直径 6px 以下）のみ |


## 3. Typography

### 3.1 Font Family

| Role | Font | Fallback | 用途 |
|------|------|----------|------|
| **Serif** | Crimson Pro | Georgia, 'Times New Roman', serif | 見出し・タイトル・引用 |
| **Sans** | Instrument Sans | -apple-system, 'Segoe UI', sans-serif | 本文・UI全般 |
| **Mono** | JetBrains Mono | 'SF Mono', monospace | コード・数値 |

```
--font-serif: 'Crimson Pro', Georgia, 'Times New Roman', serif;
--font-sans: 'Instrument Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-mono: 'JetBrains Mono', 'SF Mono', 'Fira Code', monospace;
```

見出しにはセリフ体（Crimson Pro）、本文にはサンセリフ体（Instrument Sans）を使用します。この対比が Paper テーマの視覚的リズムの中核です。

### 3.2 Type Scale

| Token | Size | Weight | Line Height | Letter Spacing | Font | 用途 |
|-------|------|--------|-------------|----------------|------|------|
| `display-xl` | 56px / 3.5rem | 300 | 1.1 | -1.5px | Serif | ヒーロー見出し |
| `display-lg` | 44px / 2.75rem | 300 | 1.15 | -1px | Serif | セクション見出し |
| `display-md` | 36px / 2.25rem | 400 | 1.2 | -0.5px | Serif | ページタイトル |
| `heading-lg` | 28px / 1.75rem | 600 | 1.3 | -0.3px | Serif | カードタイトル |
| `heading-md` | 22px / 1.375rem | 600 | 1.35 | -0.2px | Serif | サブセクション |
| `heading-sm` | 18px / 1.125rem | 600 | 1.4 | 0 | Serif | 小見出し |
| `body-lg` | 16px / 1rem | 400 | 1.7 | 0 | Sans | 本文（大） |
| `body-md` | 14px / 0.875rem | 400 | 1.6 | 0 | Sans | **本文（基準）** |
| `body-sm` | 12px / 0.75rem | 400 | 1.5 | 0.1px | Sans | 注釈・キャプション |
| `label-lg` | 14px / 0.875rem | 600 | 1.2 | 0.5px | Sans | ボタンラベル |
| `label-md` | 13px / 0.8125rem | 700 | 1.2 | 2px | Sans | セクションラベル（uppercase） |
| `label-sm` | 11px / 0.6875rem | 600 | 1.2 | 1.5px | Sans | タグ・バッジ |
| `mono-md` | 13px / 0.8125rem | 400 | 1.7 | 0 | Mono | コードブロック |
| `mono-sm` | 11px / 0.6875rem | 400 | 1.5 | 0 | Mono | インラインコード |

### 3.3 Font Weight

| Token | Weight | 用途 |
|-------|--------|------|
| `light` | 300 | Display 見出し（ヒーロー・セクション見出しの軽やかさ） |
| `regular` | 400 | 本文・説明テキスト |
| `semibold` | 600 | ラベル・ボタン・見出し（heading-lg, heading-md, heading-sm） |
| `bold` | 700 | セクションラベル・ナビゲーションのアクティブ状態 |
| `italic` | 400 italic | 引用・強調・装飾的なアクセント |

#### Weight 選択ガイド

| ユースケース | 推奨 Weight | Font | 例 |
|-------------|------------|------|-----|
| ヒーロー見出し | 300 (light) | Serif | "Design *System*" |
| ヒーロー内の装飾語 | 400 italic | Serif | "Design *System*" |
| セクション見出し | 600 (semibold) | Serif | "Color System" |
| カードタイトル | 600 (semibold) | Serif | "Standard Card" |
| 本文中の強調 | 600 (semibold) | Sans | "すべての値は**トークン**から導出" |
| KPI・メトリクス数値 | 300 (light) | Serif | "¥20.7M" |
| ボタンラベル | 600 (semibold) | Sans | "Get Started" |
| セクションラベル | 700 (bold) + uppercase | Sans | "COMPANY-WIDE DX" |
| ナビゲーション（通常） | 400 (regular) | Sans | サイドバーリンク |
| ナビゲーション（アクティブ） | 600 (semibold) | Sans | 選択中のリンク |
| バッジ・タグ | 600 (semibold) + uppercase | Sans | "LIVE" "PILOT" |

### 3.4 Typographic Patterns

Paper テーマ特有の組版パターンです。

#### Editorial Header

ヘッダーラベルは `label-md`（uppercase, bold, letter-spacing: 2px）で、新聞の欄外見出しのように機能します。

```
COMPANY-WIDE DX // Dashboard          February 2026
──────────────────────────────────────────────────
DX Impact Dashboard
全社DXの成果を「利益インパクト」「投下リソース」
「ROI」で可視化。
```

#### Section Title

セクション番号 + セリフ体見出し + サンセリフ体の説明文の組み合わせです。

```
1. 全社成果                              ← heading-lg, Serif, semibold
DX投資による全社レベルの利益インパクト     ← body-sm, Sans, text-secondary
```

#### Metric Display

大きな数値はセリフ体 light (300) で、単位記号は小さく表示します。

```
¥20.7M        ← display-md, Serif, light
年間利益貢献額  ← body-sm, Sans, text-muted
```


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

Paper テーマでは `space-8` 以上の余白を多用し、紙面の「呼吸」を確保します。


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
| **Desktop** | 12 | 24px | auto | 1120px |
| **Wide** | 12 | 32px | auto | 1280px |
| **Presentation** | 自由 | — | 48px+ | 1920×1080 |

Paper テーマではコンテンツの最大幅を digital テーマより狭く設定し、書籍・雑誌の段組に近い読みやすさを追求します。

### 5.3 Container

```
--container-sm:   640px   /* 記事・フォーム */
--container-md:   840px   /* 記事（本文幅） */
--container-lg:  1120px   /* メインレイアウト */
--container-xl:  1280px   /* ワイドレイアウト */
```

### 5.4 Grid Background

Paper テーマの特徴的な装飾要素として、方眼紙のようなグリッド背景をページ全体に配置します。

```css
.grid-bg {
  background-image:
    linear-gradient(var(--border-default) 1px, transparent 1px),
    linear-gradient(90deg, var(--border-default) 1px, transparent 1px);
  background-size: 40px 40px;
  opacity: 0.3;
}
```

コンテンツの可読性を損なわないよう、opacity は 0.3 以下とします。


## 6. Shape & Radius

### 6.1 Border Radius

Paper テーマでは角丸を最小限に抑え、紙・印刷物の直線的な質感を維持します。

| Token | Value | 用途 |
|-------|-------|------|
| `radius-none` | 0px | **カード・パネル・インプット（デフォルト）** |
| `radius-sm` | 2px | タグ・バッジ（微細な角丸） |
| `radius-md` | 4px | ボタン |
| `radius-full` | 9999px | ステータスドット |

基本方針: **0px（`radius-none`）** をカードの標準とします。直角の端がカットされた紙のように、シャープなエッジで構成します。

### 6.2 Border & Stroke Width

| Token | Value | 用途 |
|-------|-------|------|
| `stroke-hairline` | 0.5px | 微細なセパレーター・グリッド線 |
| `stroke-sm` | 1px | **ボーダー default**・カード境界・セパレーター |
| `stroke-md` | 1.5px | ナビゲーション下線・強調ボーダー |
| `stroke-lg` | 2px | ヘッダー下線・フォーカスリング |
| `stroke-xl` | 3px | セクション区切り（黒線）・最大強調 |

基本方針: **1px（`stroke-sm`）** をデフォルトのボーダー幅とします。ヘッダー直下の区切り線には `stroke-lg` 以上を使用し、紙面の「天」を強調します。


## 7. Material System

Paper テーマでは Glassmorphism / Liquid Glass を使用しません。代わりに、紙とインクの物理的特性をデジタル上で再現する 2 つのマテリアルで構成します。

### 7.1 Material Philosophy

| Material | メタファー | 特性 | 主な用途 |
|----------|-----------|------|----------|
| **Flat Paper** | 上質紙 | 影なし、罫線のみで区画、平面的 | カード、パネル、テーブル |
| **Layered Paper** | 重ねた紙 | 微細な影、紙が浮いた物理感 | モーダル、ドロップダウン、ツールチップ |

```
情報階層: 地 ─── 浮上
          Flat Paper       Layered Paper
          ─────────────    ────────────
 影        なし             微細な落ち影
 境界      1px 罫線         1px 罫線 + 影
 背景      paper-cream      paper-white
 重なり    暗示的（線で区切る） 明示的（影で浮かせる）
```

### 7.2 Flat Paper

罫線だけで区画を作る基本マテリアルです。カード・パネル・テーブルに使用します。

```css
/* Flat Paper — 基本カード */
.paper-flat {
  background: var(--paper-cream);    /* #faf9f7 */
  border: 1px solid var(--ink-100);  /* #e0e0e0 */
  border-radius: 0;
}

/* Flat Paper — ホバー時 */
.paper-flat:hover {
  border-color: var(--ink-900);      /* #1a1a1a */
}

/* Flat Paper — 凹面（インプット・埋め込み領域） */
.paper-recessed {
  background: var(--paper-warm);     /* #f5f4f0 */
  border: 1px solid var(--ink-100);  /* #e0e0e0 */
  border-radius: 0;
}
```

### 7.3 Layered Paper

重ねた紙のように微細な影で浮かせるマテリアルです。モーダル・ドロップダウンに使用します。

```css
/* Layered Paper — 浮上カード */
.paper-layered {
  background: var(--paper-white);    /* #fdfdfc */
  border: 1px solid var(--ink-100);  /* #e0e0e0 */
  border-radius: 0;
  box-shadow: 2px 2px 0 var(--ink-50);  /* #f0f0f0 — フラットな紙の影 */
}

/* Layered Paper — モーダル */
.paper-modal {
  background: var(--paper-white);    /* #fdfdfc */
  border: 1px solid var(--ink-200);  /* #c4c4c4 */
  border-radius: 0;
  box-shadow:
    4px 4px 0 var(--ink-100),        /* #e0e0e0 — 1層目の影 */
    8px 8px 0 var(--ink-50);         /* #f0f0f0 — 2層目の影 */
}

/* Layered Paper — ドロップシャドウ（自然な影） */
.paper-elevated {
  background: var(--paper-white);
  border: 1px solid var(--ink-100);
  border-radius: 0;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}
```

### 7.4 Decorative Lines & Separators

```css
/* Standard Separator — 基本の罫線 */
--separator: 1px solid var(--ink-100);      /* #e0e0e0 */

/* Strong Separator — セクション区切り */
--separator-strong: 1px solid var(--ink-1000);  /* #000000 */

/* Double Line — 重要なセクション区切り */
.separator-double {
  border: none;
  border-top: 3px double var(--ink-1000);   /* #000000 */
}

/* Dashed Separator — 補助的な区切り */
--separator-dashed: 1px dashed var(--ink-200);  /* #c4c4c4 */

/* Editorial Rule — ヘッダー下の太い罫線 */
.rule-editorial {
  border: none;
  border-bottom: 2px solid var(--ink-1000);
  padding-bottom: var(--space-3);
}
```

### 7.5 Shadows (Elevation)

Paper テーマでは影を最小限に抑えます。影は「紙が物理的に浮いている」場面でのみ使用します。

| Token | Value | 用途 |
|-------|-------|------|
| `shadow-flat` | `2px 2px 0 #f0f0f0` | 紙片のフラットな影 |
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.06)` | 微小な浮き |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.08)` | ドロップダウン |
| `shadow-lg` | `0 8px 24px rgba(0,0,0,0.1)` | モーダル |

### 7.6 Background Patterns

紙の質感を強化するオプションのテクスチャパターンです。

```css
/* Paper Grain — 紙のざらつき（noise texture） */
.paper-grain {
  position: relative;
}
.paper-grain::after {
  content: "";
  position: absolute;
  inset: 0;
  opacity: 0.03;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)'/%3E%3C/svg%3E");
  pointer-events: none;
}

/* Grid Paper — 方眼紙 */
.grid-paper {
  background-image:
    linear-gradient(var(--ink-100) 1px, transparent 1px),
    linear-gradient(90deg, var(--ink-100) 1px, transparent 1px);
  background-size: 40px 40px;
  opacity: 0.3;
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

Paper テーマではアニメーションを最小限に抑えます。紙は動かないという物理特性に従い、必要な状態遷移のみ短い duration で実行します。

### 9.1 Duration

| Token | Value | 用途 |
|-------|-------|------|
| `duration-instant` | 80ms | ホバー・フォーカス |
| `duration-fast` | 150ms | ボタン押下・切り替え |
| `duration-normal` | 200ms | パネル展開・フェード |
| `duration-slow` | 300ms | モーダル表示・セクション展開 |

### 9.2 Easing

| Token | Value | 用途 |
|-------|-------|------|
| `ease-default` | `ease` | 汎用 |
| `ease-in` | `ease-in` | 退出 |
| `ease-out` | `ease-out` | 出現 |

バウンスやスプリングのイージングは使用しません。

### 9.3 Hover Patterns

Paper テーマのホバーは控えめです。色の変化ではなく、ボーダーの濃度変化と微細な移動で状態を伝えます。

#### Card Hover — ボーダー強調 + 微浮上

```css
.card-hover {
  border: 1px solid var(--ink-100);
  transition: all 0.2s ease;
}

.card-hover:hover {
  border-color: var(--ink-900);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}
```

#### Button Hover — 反転

```css
/* Primary Button — ink → paper 反転 */
.btn-primary {
  background: var(--ink-900);
  color: var(--paper-white);
  border: 1px solid var(--ink-900);
  transition: all 0.15s ease;
}

.btn-primary:hover {
  background: var(--ink-700);
  border-color: var(--ink-700);
}

/* Secondary Button — ボーダーのみ → 塗り */
.btn-secondary {
  background: transparent;
  color: var(--ink-900);
  border: 1px solid var(--ink-900);
  transition: all 0.15s ease;
}

.btn-secondary:hover {
  background: var(--ink-900);
  color: var(--paper-white);
}
```

#### Nav Item Hover — 下線

```css
.nav-item {
  color: var(--ink-500);
  border-bottom: 2px solid transparent;
  transition: all 0.2s ease;
}

.nav-item:hover,
.nav-item.active {
  color: var(--ink-900);
  border-bottom-color: var(--ink-900);
}
```

### 9.4 Animation Patterns

```css
/* Fade In — 唯一の出現アニメーション */
@keyframes fadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}

/* Expand — アコーディオン展開 */
.collapsible {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease-out;
}

.collapsible.open {
  max-height: 2000px;
}
```


## 10. Iconography

| Property | Value |
|----------|-------|
| Style | Outline（線幅 1.5px）、直線的 |
| Optical Size | 16×16px（UI）、20×20px（ナビ）、24×24px（装飾） |
| Color | `ink-500`（通常）、`ink-900`（アクティブ） |
| Recommended Set | Lucide（Outline、角丸最小設定） |

Paper テーマではアイコンの使用を最小限にし、テキストラベルを優先します。


## 11. Platform-Specific Guidelines

### 11.1 Web Page / LP

- ヒーローにはセリフ体 `display-xl` (light 300) + イタリックの組み合わせで印刷物のような格調を表現
- ヘッダー直下に `stroke-lg` の黒線（`border-heavy`）を配置し、紙面の「天」を定義
- セクション間は `space-9`（64px）以上の余白
- CTA ボタンは `ink-900` 背景の `btn-primary`。色は使わない
- 背景にグリッドパターン（opacity: 0.3）を敷き、方眼紙の質感を付与
- ヘッダーラベルに `label-md`（uppercase, bold, tracking-widest）で新聞風の欄外見出し

### 11.2 Web App

- サーフェス階層: `bg-page`（paper-white） → `bg-surface`（paper-cream） → `bg-surface-raised`（paper-white）
- サイドバーには `paper-kraft` 背景と右辺に `stroke-sm` ボーダーを配置
- ヘッダーには `paper-white` 背景 + `backdrop-filter: blur(8px)` + 下辺 `stroke-sm` ボーダー（スクロール時の半透明）
- インタラクティブ要素のフォーカスリングは `ink-700` の 2px solid outline + 2px offset
- 本文は `body-md`（14px）、密度の高いUIでは `body-sm`（12px）

### 11.3 Mobile App (iOS)

- iOS Human Interface Guidelines を優先し、カラートークンのみ本システムから適用
- タッチターゲット: 最小 44×44pt
- Spacing: `space-4`（12px）を最小パディング
- SF Pro を基本フォントとし、見出しのみ Crimson Pro を検討（読みやすさ優先で SF Pro Serif も可）
- Dynamic Type をサポートし、Type Scale は参考値として扱う
- ダークモードでは紙色を反転（`paper-white` → `ink-900`、`ink-900` → `paper-cream`）

### 11.4 Visual Presentation

- アスペクト比: **16:9**（1920×1080）
- 背景: `paper-white` + グリッドパターン（opacity: 0.15）
- タイトル: `display-xl`（56px）、Crimson Pro Light 300
- 本文: `body-lg`（16px）以上（視認性確保）
- コードブロック: `mono-md`、`paper-warm` 背景
- 数値強調はセリフ体 light + 大サイズで表現（色は使わない）
- セクション区切りに `separator-double`（3px double black）を使用
- 余白はデスクトップより大きく取る（`space-8` 以上）


## 12. Usage Quick Reference

### 12.1 Material Layer Map

```
┌─ Page: paper-white (#fdfdfc) + grid-paper ──────────────────────┐
│                                                                   │
│  ┌─ Header ▸ paper-white + border-heavy ─────────────────────┐  │
│  │  LABEL // Title          February 2026                     │  │
│  │  ════════════════════════════════════ (2px solid black)     │  │
│  └────────────────────────────────────────────────────────────┘  │
│                                                                   │
│  ┌─ Nav ▸ sticky + backdrop-blur ─────────────────────────────┐  │
│  │  1. Section   2. Section   3. Section                       │  │
│  │  ──────────  (2px bottom-border on active)                  │  │
│  └────────────────────────────────────────────────────────────┘  │
│                                                                   │
│  ┌─ Sidebar ▸ paper-kraft ──┐  ┌─ Content Area ──────────────┐  │
│  │  Nav items                │  │                              │  │
│  │  ─── underline on hover   │  │  ┌─ Card ▸ paper-flat ───┐  │  │
│  │                           │  │  │  Heading → ink-1000     │  │  │
│  │                           │  │  │  Body    → ink-900      │  │  │
│  │                           │  │  │  Sub     → ink-600      │  │  │
│  │                           │  │  └─────────────────────────┘  │  │
│  │                           │  │                              │  │
│  │                           │  │  ┌─ CTA ▸ btn-primary ────┐  │  │
│  │                           │  │  │  ink-900 bg, paper text  │  │  │
│  │                           │  │  └─────────────────────────┘  │  │
│  └───────────────────────────┘  └──────────────────────────────┘  │
│                                                                   │
│  ┌─ Hero ▸ generous whitespace ────────────────────────────────┐  │
│  │  display-xl title, Crimson Pro Light                         │  │
│  │  CTA: btn-primary (ink-900 background)                       │  │
│  └──────────────────────────────────────────────────────────────┘  │
└───────────────────────────────────────────────────────────────────┘
```

### 12.2 Material × Component 早見表

| Component | Default Material | Hover | 備考 |
|-----------|-----------------|-------|------|
| Card | `paper-flat` | border → `ink-900` | 角丸なし |
| Header | `paper-white` + `border-heavy` | — | 太い黒線で区切り |
| Sidebar | `paper-kraft` + right border | — | 控えめな紙色 |
| Button (Primary) | `ink-900` bg | `ink-700` bg | 黒背景・白文字 |
| Button (Secondary) | transparent + `ink-900` border | `ink-900` bg + white text | 黒枠 → 反転 |
| Button (Ghost) | transparent | `paper-aged` bg | テキストのみ |
| Modal | `paper-modal` | — | 多層影 |
| Tooltip | `paper-elevated` | — | 微細な自然影 |

### 12.3 ステータス表示

```
Success  → テキスト: ink-900, ラベル: "Complete",  記号: ✓, 背景: paper-warm
Warning  → テキスト: ink-900, ラベル: "Attention", 記号: !, 背景: paper-warm, border: ink-300
Error    → テキスト: ink-900, ラベル: "Error",     記号: ×, 背景: paper-warm, border: ink-700 2px
Info     → テキスト: ink-600, ラベル: "Note",      記号: i, 背景: paper-cream
```


## 13. Component Guidelines

UIコンポーネントの仕様をここで定義します。すべてのコンポーネントはデザイントークンから値を導出し、色を排したモノクロームで構成します。

### 13.1 Button

#### Variants

| Variant | Background | Text | Border | 用途 |
|---------|-----------|------|--------|------|
| **Primary** | `ink-900` (#1a1a1a) | `paper-white` (#fdfdfc) | none | CTA・主要アクション |
| **Secondary** | transparent | `ink-900` | `stroke-sm` solid `ink-900` | 補助アクション |
| **Ghost** | transparent | `ink-600` | none | 最小限のアクション |
| **Danger** | transparent | `ink-900` | `stroke-lg` solid `ink-900` | 破壊的アクション（ラベルで区別） |

Danger ボタンに赤色は使用しません。太いボーダー（2px）とラベルテキスト（「削除する」等）で破壊的操作であることを伝えます。

#### Sizes

| Size | Height | Padding (h) | Font | Radius |
|------|--------|-------------|------|--------|
| **sm** | 32px | 12px | `body-sm` (12px), semibold | `radius-md` (4px) |
| **md** | 40px | 16px | `body-md` (14px), semibold | `radius-md` (4px) |
| **lg** | 48px | 24px | `body-lg` (16px), semibold | `radius-md` (4px) |

#### States

| State | 変化 |
|-------|------|
| Default | 上記 Variants の通り |
| Hover | Primary → `ink-700` bg / Secondary → 反転（`ink-900` bg + white text） |
| Active / Pressed | Primary → `ink-1000` bg / Secondary → `ink-1000` bg |
| Focus | outline: 2px solid `ink-700`, outline-offset: 2px |
| Disabled | opacity: 0.3、cursor: not-allowed |
| Loading | テキストを `...` に差し替え、pointer-events: none |

### 13.2 Card

| Property | Value |
|----------|-------|
| Background | `bg-surface` (paper-cream) |
| Border | `stroke-sm` solid `border-default` (ink-100) |
| Radius | `radius-none` (0px) |
| Padding | `space-5` (16px) ～ `space-6` (24px) |
| Hover（clickable） | border-color → `ink-900`、translateY(-2px)、`shadow-md` |

#### Card Variants by Material

| Variant | Class | 用途 |
|---------|-------|------|
| **Flat Card** | `.paper-flat` | 罫線のみの基本カード |
| **Layered Card** | `.paper-layered` | 浮上したカード（フラット影付き） |
| **Elevated Card** | `.paper-elevated` | 自然な影で浮上したカード |

### 13.3 Input / Text Field

| Property | Value |
|----------|-------|
| Background | `bg-recessed` (paper-warm) |
| Border | `stroke-sm` solid `border-default` (ink-100) |
| Radius | `radius-none` (0px) |
| Height | 40px（md）/ 32px（sm） |
| Padding | 0 `space-4` (12px) |
| Font | `body-md` (14px), Sans |
| Text Color | `text-primary` (ink-900) |
| Placeholder | `text-muted` (ink-400) |

#### States

| State | 変化 |
|-------|------|
| Default | 上記の通り |
| Hover | border-color → `ink-200` |
| Focus | border-color → `ink-900`、outline: 2px solid `ink-700`、outline-offset: 2px |
| Error | border-color → `ink-900`、border-width: 2px、エラーメッセージを下に表示 |
| Disabled | background → `paper-kraft`、opacity: 0.5 |

### 13.4 Badge / Tag

| Property | Value |
|----------|-------|
| Height | 22px |
| Padding | 0 `space-3` (8px) |
| Font | `label-sm` (11px), semibold, uppercase |
| Radius | `radius-sm` (2px) |
| Background | `paper-warm` (ink が乗る台紙) |
| Text Color | `ink-900` |
| Border | `stroke-sm` solid `ink-200` |

ステータスバッジも色ではなくラベルテキストで区別します。

| Status | Label | Border | 備考 |
|--------|-------|--------|------|
| Active / Live | "LIVE" | `ink-900` | 太めのボーダー |
| In Progress | "PILOT" | `ink-300` | 標準ボーダー |
| Planned | "PLANNING" | `ink-100` | 薄いボーダー |

### 13.5 Modal / Dialog

| Property | Value |
|----------|-------|
| Material | `paper-modal` |
| Background | `paper-white` |
| Border | `stroke-sm` solid `ink-200` |
| Radius | `radius-none` (0px) |
| Shadow | `shadow-lg` or 多層フラット影 |
| Max Width | `container-sm` (640px) |
| Padding | `space-6` (24px) ～ `space-7` (32px) |
| Overlay | `paper-white` @ 80% opacity |
| Entry Animation | fadeIn `duration-slow` |

### 13.6 Toast / Notification

| Property | Value |
|----------|-------|
| Background | `ink-900` |
| Text Color | `paper-white` |
| Font | `body-sm` (12px) |
| Radius | `radius-none` (0px) |
| Padding | `space-3` (8px) `space-5` (16px) |
| Position | fixed、bottom: 24px、center |
| z-index | `z-toast` (400) |
| Animation | fadeIn、`duration-normal` |
| Auto Dismiss | 3000ms default |

Toast は画面上で最も目立つ要素であるため、例外的に `ink-900` 背景（黒）で反転表示します。

### 13.7 Navigation / Sidebar

| Property | Value |
|----------|-------|
| Background | `paper-kraft` (#eeedea) |
| Width | 240px ～ 280px |
| Border Right | `stroke-sm` solid `border-default` |
| Nav Item Height | 36px |
| Nav Item Padding | `space-3` (8px) `space-4` (12px) |
| Nav Item Font | `body-md` (14px), Sans |
| Nav Item Radius | `radius-none` (0px) |
| Active State | text → `ink-900`、font-weight: 600、border-left: 2px solid `ink-900` |
| Hover State | text → `ink-900`、background → `paper-aged` |

### 13.8 Sticky Navigation Bar

ページ内ナビゲーション用のスティッキーバーです。参考HTMLの section-nav パターンに準拠します。

| Property | Value |
|----------|-------|
| Background | `paper-white` @ 95% opacity |
| Backdrop Filter | blur(8px) |
| Border Bottom | `stroke-sm` solid `border-default` |
| z-index | `z-raised` (10) |
| Nav Item Font | `body-sm` (0.85rem), Sans |
| Nav Item Color | `text-muted` → `text-primary` on active |
| Active Indicator | border-bottom: 2px solid `ink-900` |

### 13.9 Table

| Property | Value |
|----------|-------|
| Header Font | `label-md` (13px), bold, uppercase |
| Header Color | `text-secondary` (ink-600) |
| Header Border Bottom | `stroke-sm` solid `ink-900` |
| Cell Font | `body-md` (14px), Sans |
| Cell Padding | `space-5` (16px) |
| Row Border Bottom | `stroke-hairline` solid `ink-100` |
| Row Hover | background → `paper-warm` |
| Mono Values | `mono-md` を使用（数値・コード） |

### 13.10 Progress Bar

| Property | Value |
|----------|-------|
| Track Height | 4px |
| Track Background | `ink-100` (#e0e0e0) |
| Track Radius | 2px |
| Fill Background | `ink-900` (#1a1a1a) |
| Fill Radius | 2px |

進捗バーも色を使わず、黒のフィルで進捗を表現します。

### 13.11 Metric Card

KPI・数値を大きく表示するカードです。参考HTMLの metric-card パターンに準拠します。

| Property | Value |
|----------|-------|
| Background | `paper-flat` |
| Padding | `space-6` (24px) |
| Text Align | center |
| Value Font | `display-md` (36px) or larger, Serif, light (300) |
| Value Color | `ink-900` |
| Label Font | `body-sm` (12px), Sans |
| Label Color | `text-muted` (ink-400) |
| Breakdown Border | `stroke-hairline` solid `ink-50` |
| Breakdown Font | `body-sm` (12px), Sans |

数値の強調は色ではなく、サイズとウェイトの対比で実現します。

### 13.12 Expandable / Accordion

ツリー構造やドリルダウン表示に使用する展開可能なセクションです。

| Property | Value |
|----------|-------|
| Toggle Font | `body-md` (14px), semibold, Sans |
| Toggle Padding | `space-4` (12px) |
| Toggle Background | `paper-warm` |
| Toggle Radius | `radius-none` |
| Arrow | `▶` (text, 0.7rem)、展開時 rotate(90deg) |
| Tree Line | border-left: 2px solid `ink-100`、margin-left: 12px、padding-left: 20px |
| Content Transition | max-height 0.3s ease-out |


## 14. CSS Custom Properties Reference

Paper テーマで使用する全 CSS Custom Properties の一覧です。

```css
:root {
  /* ── Typography ── */
  --font-serif: 'Crimson Pro', Georgia, 'Times New Roman', serif;
  --font-sans: 'Instrument Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-mono: 'JetBrains Mono', 'SF Mono', 'Fira Code', monospace;

  /* ── Ink Scale ── */
  --ink-1000: #000000;
  --ink-900: #1a1a1a;
  --ink-800: #2d2d2d;
  --ink-700: #404040;
  --ink-600: #525252;
  --ink-500: #6b6b6b;
  --ink-400: #8a8a8a;
  --ink-300: #a3a3a3;
  --ink-200: #c4c4c4;
  --ink-100: #e0e0e0;
  --ink-50:  #f0f0f0;

  /* ── Paper Scale ── */
  --paper-white:  #fdfdfc;
  --paper-cream:  #faf9f7;
  --paper-warm:   #f5f4f0;
  --paper-kraft:  #eeedea;
  --paper-aged:   #e8e7e3;
  --paper-shadow: #dddcd8;

  /* ── Semantic ── */
  --bg-page: var(--paper-white);
  --bg-surface: var(--paper-cream);
  --bg-surface-raised: var(--paper-white);
  --bg-recessed: var(--paper-warm);
  --border-default: var(--ink-100);
  --border-strong: var(--ink-200);
  --border-heavy: var(--ink-1000);
  --text-primary: var(--ink-900);
  --text-heading: var(--ink-1000);
  --text-secondary: var(--ink-600);
  --text-muted: var(--ink-400);
  --text-caption: var(--ink-500);

  /* ── Spacing ── */
  --space-0: 0px;
  --space-1: 2px;
  --space-2: 4px;
  --space-3: 8px;
  --space-4: 12px;
  --space-5: 16px;
  --space-6: 24px;
  --space-7: 32px;
  --space-8: 48px;
  --space-9: 64px;
  --space-10: 96px;
  --space-11: 128px;

  /* ── Radius ── */
  --radius-none: 0px;
  --radius-sm: 2px;
  --radius-md: 4px;
  --radius-full: 9999px;

  /* ── Shadows ── */
  --shadow-flat: 2px 2px 0 var(--ink-50);
  --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.06);
  --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.08);
  --shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.1);

  /* ── Motion ── */
  --duration-instant: 80ms;
  --duration-fast: 150ms;
  --duration-normal: 200ms;
  --duration-slow: 300ms;

  /* ── Lines ── */
  --separator: 1px solid var(--ink-100);
  --separator-strong: 1px solid var(--ink-1000);
  --separator-dashed: 1px dashed var(--ink-200);
}
```
