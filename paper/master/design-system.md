# Design System — Paper

## Design Philosophy

紙とインクで成立する Editorial / Magazine-inspired design。情報階層はセリフ体とサンセリフ体の対比、ウェイトとサイズの段階、余白の量と質で表現する。色は黒インクを主軸に、意味のある場面でのみ淡い色付きインクを添える。方眼紙のグリッド背景が「紙上の分析ノート」という世界観を演出する。

| # | Principle | 説明 |
|---|-----------|------|
| 1 | Paper-First | 紙とインクだけで成立するデザイン |
| 2 | Restrained Color | 黒インクが主役。色付きインクは意味のある場面で控えめに添える |
| 3 | Typographic Hierarchy | セリフ × サンセリフの対比で構造を表現 |
| 4 | Generous Whitespace | 余白の量と質で読みやすさと格調を生む |
| 5 | Ink Economy | すべての要素に「インクを使う価値があるか」を問う |

## Typography

### Font Family

| Role | Font | Fallback | Usage |
|------|------|----------|-------|
| Serif | Crimson Pro | Georgia, 'Times New Roman', serif | 見出し・タイトル・引用・メトリクス数値 |
| Sans | Instrument Sans | -apple-system, 'Segoe UI', sans-serif | 本文・UI全般 |
| Mono | JetBrains Mono | 'SF Mono', 'Fira Code', monospace | コード・数値 |

### Type Scale

| Token | Size | Weight | Line Height | Letter Spacing | Font | Usage |
|-------|------|--------|-------------|----------------|------|-------|
| `display-xl` | 56px / 3.5rem | 300 | 1.1 | -1.5px | Serif | ヒーロー見出し。italic を部分適用 |
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
| `label-sm` | 11px / 0.6875rem | 600 | 1.2 | 1.5px | Sans | タグ・バッジ（uppercase） |
| `mono-md` | 13px / 0.8125rem | 400 | 1.7 | 0 | Mono | コードブロック |
| `mono-sm` | 11px / 0.6875rem | 400 | 1.5 | 0 | Mono | インラインコード |

Font Weight: `300` (light) = display 見出し・メトリクス数値 / `400` (regular) = 本文 / `600` (semibold) = heading・ラベル・ボタン / `700` (bold) = セクションラベル・uppercase / `400 italic` = 引用・装飾アクセント

### Typographic Patterns

```
COMPANY-WIDE DX // Dashboard          February 2026  ← label-md, uppercase, bold, tracking: 2px
──────────────────────────────────────────────────    ← border-heavy (2px solid black)
DX Impact Dashboard                                   ← display-md, Serif, regular
全社DXの成果を可視化。                                  ← body-md, Sans, text-secondary

1. 全社成果                                            ← heading-lg, Serif, semibold
DX投資による全社レベルの利益インパクト                      ← body-sm, Sans, text-secondary

¥20.7M                                                ← display-md, Serif, light (300)
年間利益貢献額                                          ← body-sm, Sans, text-muted
```

## Color Tokens

### Ink Scale — テキスト・ボーダー・アイコン

| Token | Hex | Usage |
|-------|-----|-------|
| `ink-1000` | `#000000` | 見出し・最大強調 |
| `ink-900` | `#1a1a1a` | 本文テキスト |
| `ink-800` | `#2d2d2d` | 強調テキスト |
| `ink-700` | `#404040` | アクティブ要素・フォーカスリング |
| `ink-600` | `#525252` | セカンダリテキスト |
| `ink-500` | `#6b6b6b` | キャプション |
| `ink-400` | `#8a8a8a` | プレースホルダ |
| `ink-300` | `#a3a3a3` | 非活性テキスト |
| `ink-200` | `#c4c4c4` | 薄いボーダー |
| `ink-100` | `#e0e0e0` | セパレーター |
| `ink-50` | `#f0f0f0` | 微細な区切り線 |

### Paper Scale — 背景・サーフェス

| Token | Hex | Usage |
|-------|-----|-------|
| `paper-white` | `#fdfdfc` | ページ背景（上質紙） |
| `paper-cream` | `#faf9f7` | カード背景（生成り） |
| `paper-warm` | `#f5f4f0` | セクション背景（クラフト紙） |
| `paper-kraft` | `#eeedea` | サイドバー・ヘッダー背景 |
| `paper-aged` | `#e8e7e3` | ホバー・アクティブ背景 |
| `paper-shadow` | `#dddcd8` | 影の表現・押下状態 |

### Accent Ink — 色付きインク

紙に落とした色付きインクの滲みのような、控えめなアクセントカラー。彩度を落とし、温かみのあるトーンで Paper Scale と調和させる。

| Token | Hex | Usage |
|-------|-----|-------|
| `ink-blue` | `#4a6d8c` | リンク・アクティブ状態・選択・フォーカス |
| `ink-green` | `#4a7c5c` | 成功・利益・完了 |
| `ink-amber` | `#8c6d3f` | 注意・ハイライト・ROI |
| `ink-red` | `#8c4a4a` | エラー・危険・削除 |

| Token | Hex | Usage |
|-------|-----|-------|
| `wash-blue` | `#eef2f7` | 選択状態・アクティブ背景 |
| `wash-green` | `#edf4ef` | 成功背景・完了表示 |
| `wash-amber` | `#f5f1ea` | 注意背景・ハイライト |
| `wash-red` | `#f5eded` | エラー背景・警告 |

使用ルール: 色付きインクは意味を伴う場面（ステータス・インタラクション・データ可視化）にのみ使用する。装飾目的では使用しない。主軸はあくまで黒インク（Ink Scale）。

### Semantic Tokens

| Token | Maps To | Usage |
|-------|---------|-------|
| `bg-page` | paper-white `#fdfdfc` | ページ全体の背景 |
| `bg-surface` | paper-cream `#faf9f7` | カード・パネル背景 |
| `bg-surface-raised` | paper-white `#fdfdfc` | モーダル・浮上パネル |
| `bg-recessed` | paper-warm `#f5f4f0` | インプット背景 |
| `border-default` | ink-100 `#e0e0e0` | 通常のボーダー |
| `border-strong` | ink-200 `#c4c4c4` | 強調ボーダー |
| `border-heavy` | ink-1000 `#000000` | ヘッダー下線・重要な区切り |
| `text-primary` | ink-900 `#1a1a1a` | 本文テキスト |
| `text-heading` | ink-1000 `#000000` | 見出し |
| `text-secondary` | ink-600 `#525252` | 補助テキスト |
| `text-muted` | ink-400 `#8a8a8a` | ヒントテキスト |
| `text-caption` | ink-500 `#6b6b6b` | キャプション・注釈 |
| `interactive` | ink-900 `#1a1a1a` | ボタン・リンク |
| `interactive-hover` | ink-700 `#404040` | ホバー状態 |
| `focus-ring` | ink-700 `#404040` | フォーカスインジケーター |

### Status Indication

色に頼らず、テキストラベル・記号・ボーダー太さで状態を伝える。

| Status | Label | Symbol | Background | Border |
|--------|-------|--------|------------|--------|
| Success | "Complete" | ✓ | `paper-warm` | `ink-200` |
| Warning | "Attention" | ! | `paper-warm` | `ink-300` |
| Error | "Error" | × | `paper-warm` | `ink-700` 2px |
| Info | "Note" | i | `paper-cream` | `ink-100` |

データ可視化・ステータスドット（直径 6px 以下）に限り、Success `#16a34a` / Error `#dc2626` を使用可。

## Layout

### Page Structure

```
[Fixed Grid Background — 40px grid, opacity: 0.3]
  Header (paper-white, border-bottom: 2px solid black)
    [Left: label-md uppercase]               [Right: Date]
    [Page Title — display-md, Serif]
    [Description — body-md, text-secondary]
  Sticky Navigation (top: 0, backdrop-blur: 8px, z-index: 10)
    1. Section   2. Section   3. Section
    ──────────  (2px bottom-border on active)
  Main Content (max-w: 1120px, padding: 48px+, section-gap: 64px)
    Section 1–N
  Footer (max-w: 1120px, border-top: ink-100)
    [Left: Copyright]                        [Right: Confidentiality]
```

### Breakpoints

| Token | Width | Layout Changes |
|-------|-------|----------------|
| `bp-mobile` | 0–639px | 4col, gutter 16px, padding 16px, 単一カラム |
| `bp-tablet` | 640–1023px | 8col, gutter 24px, padding 32px |
| `bp-desktop` | 1024–1439px | 12col, gutter 24px, max-w 1120px |
| `bp-wide` | 1440px+ | 12col, gutter 32px, max-w 1280px |

### Container

```css
--container-sm:   640px;   /* 記事・フォーム */
--container-md:   840px;   /* 記事（本文幅） */
--container-lg:  1120px;   /* メインレイアウト */
--container-xl:  1280px;   /* ワイドレイアウト */
```

## Spacing

8px グリッドベース。`space-8` 以上の余白を多用し、紙面の「呼吸」を確保する。

| Token | Value | Usage |
|-------|-------|-------|
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

## Shape & Lines

### Border Radius

角丸を最小限に抑え、紙の直線的な質感を維持する。

| Token | Value | Usage |
|-------|-------|-------|
| `radius-none` | 0px | **カード・パネル・インプット（デフォルト）** |
| `radius-sm` | 2px | タグ・バッジ |
| `radius-md` | 4px | ボタン |
| `radius-full` | 9999px | ステータスドット |

### Stroke Width

| Token | Value | Usage |
|-------|-------|-------|
| `stroke-hairline` | 0.5px | グリッド線・微細なセパレーター |
| `stroke-sm` | 1px | **ボーダー default** |
| `stroke-md` | 1.5px | ナビゲーション下線 |
| `stroke-lg` | 2px | ヘッダー下線・フォーカスリング |
| `stroke-xl` | 3px | セクション区切り（黒線） |

### Separators

```css
--separator: 1px solid var(--ink-100);
--separator-strong: 1px solid var(--ink-1000);
--separator-dashed: 1px dashed var(--ink-200);

.separator-double { border-top: 3px double var(--ink-1000); }
.rule-editorial  { border-bottom: 2px solid var(--ink-1000); padding-bottom: var(--space-3); }
```

## Material System

Glassmorphism / Liquid Glass を使用しない。紙とインクの物理特性をデジタル上で再現する 2 つのマテリアルで構成する。

### Flat Paper — 罫線のみの基本マテリアル

```css
.paper-flat {
  background: var(--paper-cream);    /* #faf9f7 */
  border: 1px solid var(--ink-100);  /* #e0e0e0 */
  border-radius: 0;
}
.paper-flat:hover { border-color: var(--ink-900); }

.paper-recessed {
  background: var(--paper-warm);     /* #f5f4f0 — インプット・埋め込み領域 */
  border: 1px solid var(--ink-100);
  border-radius: 0;
}
```

### Layered Paper — 微細な影で浮かせるマテリアル

```css
.paper-layered {
  background: var(--paper-white);
  border: 1px solid var(--ink-100);
  border-radius: 0;
  box-shadow: 2px 2px 0 var(--ink-50);  /* フラットな紙の影 */
}

.paper-modal {
  background: var(--paper-white);
  border: 1px solid var(--ink-200);
  border-radius: 0;
  box-shadow: 4px 4px 0 var(--ink-100), 8px 8px 0 var(--ink-50);  /* 多層影 */
}

.paper-elevated {
  background: var(--paper-white);
  border: 1px solid var(--ink-100);
  border-radius: 0;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}
```

### Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-flat` | `2px 2px 0 #f0f0f0` | 紙片のフラットな影 |
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.06)` | 微小な浮き |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.08)` | ドロップダウン |
| `shadow-lg` | `0 8px 24px rgba(0,0,0,0.1)` | モーダル |

### Background Patterns

```css
/* Paper Grain — 紙のざらつき */
.paper-grain::after {
  content: ""; position: absolute; inset: 0; opacity: 0.03; pointer-events: none;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)'/%3E%3C/svg%3E");
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

## Elevation

| Token | z-index | Usage |
|-------|---------|-------|
| `z-base` | 0 | 通常コンテンツ |
| `z-raised` | 10 | スティッキーヘッダー |
| `z-dropdown` | 100 | ドロップダウン・ポップオーバー |
| `z-overlay` | 200 | オーバーレイ背景 |
| `z-modal` | 300 | モーダル・ダイアログ |
| `z-toast` | 400 | トースト通知 |
| `z-tooltip` | 500 | ツールチップ |

## Motion

紙は動かない。必要な状態遷移のみ短い duration で実行する。バウンス・スプリングは使用しない。

| Token | Value | Usage |
|-------|-------|-------|
| `duration-instant` | 80ms | ホバー・フォーカス |
| `duration-fast` | 150ms | ボタン押下・切り替え |
| `duration-normal` | 200ms | パネル展開・フェード |
| `duration-slow` | 300ms | モーダル表示・セクション展開 |
| `ease-default` | `ease` | 汎用 |
| `ease-in` | `ease-in` | 退出 |
| `ease-out` | `ease-out` | 出現 |

```css
@keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
```

## Components

### Card `.paper-flat`

| Property | Value |
|----------|-------|
| Background | `bg-surface` (paper-cream) |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-none` (0px) |
| Padding | `space-5` – `space-6` |

- **Hover** (clickable): `border-color: var(--ink-900)`, `translateY(-2px)`, `shadow-md`
- Variants: `.paper-flat`（罫線のみ）/ `.paper-layered`（フラット影）/ `.paper-elevated`（自然影）

### Button

| Variant | Background | Text | Border | Usage |
|---------|-----------|------|--------|-------|
| Primary | `ink-900` | `paper-white` | none | CTA・主要アクション |
| Secondary | transparent | `ink-900` | `stroke-sm` solid `ink-900` | 補助アクション |
| Ghost | transparent | `ink-600` | none | 最小限のアクション |
| Danger | transparent | `ink-900` | `stroke-lg` solid `ink-900` | 破壊的アクション（ラベルで区別） |

| Size | Height | Padding (h) | Font |
|------|--------|-------------|------|
| sm | 32px | 12px | `body-sm`, semibold |
| md | 40px | 16px | `body-md`, semibold |
| lg | 48px | 24px | `body-lg`, semibold |

Radius: 全サイズ `radius-md` (4px)

```css
/* Primary */
.btn-primary { background: var(--ink-900); color: var(--paper-white); transition: all 0.15s ease; }
.btn-primary:hover { background: var(--ink-700); }
.btn-primary:active { background: var(--ink-1000); }

/* Secondary */
.btn-secondary { background: transparent; color: var(--ink-900); border: 1px solid var(--ink-900); transition: all 0.15s ease; }
.btn-secondary:hover { background: var(--ink-900); color: var(--paper-white); }
```

- **Focus**: `outline: 2px solid var(--ink-700); outline-offset: 2px`
- **Disabled**: `opacity: 0.3; cursor: not-allowed`
- **Loading**: テキストを `...` に差し替え、`pointer-events: none`

### Input `.paper-recessed`

| Property | Value |
|----------|-------|
| Background | `bg-recessed` (paper-warm) |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-none` (0px) |
| Height | 40px (md) / 32px (sm) |
| Padding | 0 `space-4` |
| Font | `body-md`, Sans |
| Placeholder | `text-muted` (ink-400) |

- **Hover**: `border-color: var(--ink-200)`
- **Focus**: `border-color: var(--ink-900)`, `outline: 2px solid var(--ink-700)`, `outline-offset: 2px`
- **Error**: `border-color: var(--ink-900)`, `border-width: 2px`, エラーメッセージを下に表示
- **Disabled**: `background: paper-kraft`, `opacity: 0.5`

### Badge / Tag

```css
padding: 0 8px; height: 22px; border-radius: 2px;
font-size: 0.6875rem; font-weight: 600; text-transform: uppercase;
background: var(--paper-warm); color: var(--ink-900); border: 1px solid var(--ink-200);
```

| Status | Label | Border |
|--------|-------|--------|
| Active | "LIVE" | `ink-900` |
| In Progress | "PILOT" | `ink-300` |
| Planned | "PLANNING" | `ink-100` |

### Modal `.paper-modal`

| Property | Value |
|----------|-------|
| Background | `paper-white` |
| Border | `stroke-sm` solid `ink-200` |
| Shadow | `shadow-lg` or 多層フラット影 |
| Max Width | `container-sm` (640px) |
| Padding | `space-6` – `space-7` |
| Overlay | `paper-white` @ 80% opacity |
| z-index | `z-modal` (300) |
| Animation | fadeIn `duration-slow` |

### Toast

反転表示（画面上で最も目立つ要素）。

```css
background: var(--ink-900); color: var(--paper-white);
font-size: 0.75rem; padding: 8px 16px; border-radius: 0;
position: fixed; bottom: 24px; z-index: 400;
animation: fadeIn 0.2s ease;  /* auto-dismiss: 3000ms */
```

### Navigation / Sidebar

| Property | Value |
|----------|-------|
| Background | `paper-kraft` (#eeedea) |
| Width | 240–280px |
| Border Right | `stroke-sm` solid `border-default` |
| Nav Item | 36px height, `body-md`, `radius-none` |

- **Active**: `color: ink-900`, `font-weight: 600`, `border-left: 2px solid ink-900`
- **Hover**: `color: ink-900`, `background: paper-aged`

### Sticky Navigation `.section-nav`

```css
position: sticky; top: 0;
background: rgba(253, 253, 252, 0.95);
backdrop-filter: blur(8px);
z-index: 10;
border-bottom: 1px solid var(--border-default);
```

- **Nav Item**: `font-size: 0.85rem`, `color: var(--text-muted)`, `padding: 12px 16px`
- **Active / Hover**: `color: var(--text-primary)`, `border-bottom: 2px solid var(--ink-900)`
- IntersectionObserver によるスクロール連動ハイライト

### Table

| Property | Value |
|----------|-------|
| Header | `label-md`, bold, uppercase, `text-secondary` |
| Header Border | `stroke-sm` solid `ink-900` |
| Cell | `body-md`, Sans, padding `space-5` |
| Row Border | `stroke-hairline` solid `ink-100` |
| Row Hover | `background: paper-warm` |
| Mono Values | `mono-md`（数値・コード） |

### Progress Bar

```css
/* Track */  height: 4px; background: var(--ink-100); border-radius: 2px;
/* Fill */   background: var(--ink-900); border-radius: 2px; transition: width 0.5s ease-out;
```

### Metric Card

Card の拡張。中央揃え、`padding: space-6`。

```
[Value]     — display-md or larger, Serif, light (300), ink-900
[Label]     — body-sm, Sans, text-muted
[Divider]   — border-t ink-50, mt-4 pt-4
[Details]   — body-sm, Sans, flex justify-between
```

### Expandable / Accordion

| Property | Value |
|----------|-------|
| Toggle | `body-md`, semibold, `paper-warm` bg, `radius-none` |
| Arrow | `▶` (0.7rem)、展開時 `rotate(90deg)`, transition 0.2s |
| Tree Line | `border-left: 2px solid ink-100`, `margin-left: 12px`, `padding-left: 20px` |
| Content | `max-height: 0` → `.open` で `max-height: 2000px`, transition 0.3s ease-out |

## Interaction Patterns

### Drill-Down Navigation

多段階の情報階層を段階的に掘り下げる。

1. 概要カード群をグリッド表示（Section 1）
2. カードクリック → selected 状態（`border-color: ink-900`）
3. 詳細セクションにスムーズスクロール + コンテンツレンダリング
4. 詳細内の行クリック → アコーディオンで打ち手展開

### Expandable Tree

- ヘッダークリックで子要素の表示/非表示を切り替え
- 左辺のツリーラインで親子関係を視覚化
- 同時に複数ノードを展開可能

### Time Period Toggle

- タブボタンで期間を切り替え（例: 1年目 / 3年累計）
- メトリクス値を直接 DOM 書き換え

## Iconography

| Property | Value |
|----------|-------|
| Style | Outline（線幅 1.5px）、直線的 |
| Size | 16px（UI）/ 20px（ナビ）/ 24px（装飾） |
| Color | `ink-500`（通常）→ `ink-900`（アクティブ） |
| Set | Lucide（Outline、角丸最小設定） |

テキストラベルを優先し、アイコンの使用は最小限にする。

## Platform Guidelines

| Platform | 要点 |
|----------|------|
| **Web Page / LP** | ヒーロー `display-xl` light + italic。ヘッダー直下に `border-heavy`。セクション間 `space-9`+。CTA は `btn-primary`。背景にグリッドパターン |
| **Web App** | サーフェス階層: `bg-page` → `bg-surface` → `bg-surface-raised`。サイドバー `paper-kraft`。ヘッダー `backdrop-filter: blur(8px)`。本文 `body-md`、密度の高いUIは `body-sm` |
| **Mobile (iOS)** | iOS HIG 優先。カラートークンのみ適用。タッチターゲット 44×44pt 以上。SF Pro 基本、見出しのみ Crimson Pro 検討。Dynamic Type サポート |
| **Presentation** | 16:9 (1920×1080)。`paper-white` + グリッドパターン (opacity: 0.15)。タイトル `display-xl`、本文 `body-lg` 以上。セクション区切りに `separator-double`。余白 `space-8`+ |

## CSS Custom Properties Reference

```css
:root {
  /* Typography */
  --font-serif: 'Crimson Pro', Georgia, 'Times New Roman', serif;
  --font-sans: 'Instrument Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-mono: 'JetBrains Mono', 'SF Mono', 'Fira Code', monospace;

  /* Ink Scale */
  --ink-1000: #000000;  --ink-900: #1a1a1a;  --ink-800: #2d2d2d;
  --ink-700: #404040;   --ink-600: #525252;   --ink-500: #6b6b6b;
  --ink-400: #8a8a8a;   --ink-300: #a3a3a3;   --ink-200: #c4c4c4;
  --ink-100: #e0e0e0;   --ink-50:  #f0f0f0;

  /* Paper Scale */
  --paper-white: #fdfdfc;  --paper-cream: #faf9f7;  --paper-warm:   #f5f4f0;
  --paper-kraft: #eeedea;  --paper-aged:  #e8e7e3;  --paper-shadow: #dddcd8;

  /* Semantic */
  --bg-page: var(--paper-white);         --bg-surface: var(--paper-cream);
  --bg-surface-raised: var(--paper-white); --bg-recessed: var(--paper-warm);
  --border-default: var(--ink-100);      --border-strong: var(--ink-200);
  --border-heavy: var(--ink-1000);
  --text-primary: var(--ink-900);        --text-heading: var(--ink-1000);
  --text-secondary: var(--ink-600);      --text-muted: var(--ink-400);
  --text-caption: var(--ink-500);

  /* Spacing */
  --space-0: 0px;   --space-1: 2px;   --space-2: 4px;   --space-3: 8px;
  --space-4: 12px;  --space-5: 16px;  --space-6: 24px;  --space-7: 32px;
  --space-8: 48px;  --space-9: 64px;  --space-10: 96px; --space-11: 128px;

  /* Radius */
  --radius-none: 0px;  --radius-sm: 2px;  --radius-md: 4px;  --radius-full: 9999px;

  /* Shadows */
  --shadow-flat: 2px 2px 0 var(--ink-50);
  --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.06);
  --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.08);
  --shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.1);

  /* Motion */
  --duration-instant: 80ms;  --duration-fast: 150ms;
  --duration-normal: 200ms;  --duration-slow: 300ms;

  /* Lines */
  --separator: 1px solid var(--ink-100);
  --separator-strong: 1px solid var(--ink-1000);
  --separator-dashed: 1px dashed var(--ink-200);
}
```

## Dependencies

- **Tailwind CSS**: ユーティリティクラスベース。カスタムプロパティを `tailwind.config` で拡張
- **Google Fonts**: Crimson Pro (300, 400, 600, 400italic), Instrument Sans (400, 600)
- **JetBrains Mono**: Google Fonts or self-hosted
- **Lucide Icons**: Outline スタイル、角丸最小
- **JavaScript**: Vanilla JS（IntersectionObserver, accordion 制御）
