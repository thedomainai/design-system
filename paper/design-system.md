# Design System — Paper

## 1. Design Principles

紙とインクで成立する Editorial / Magazine-inspired design。情報階層はセリフ体とサンセリフ体の対比、ウェイトとサイズの段階、余白の量と質で表現する。色は黒インクを主軸に、意味のある場面では標準的な彩度のインクを使い、即座の識別を確保する。方眼紙のグリッド背景が「紙上の分析ノート」という世界観を演出する。

| # | Principle | 説明 |
|---|-----------|------|
| 1 | Paper-First | 紙とインクだけで成立するデザイン |
| 2 | Restrained Color | Slate（青みを帯びたグレー）が UI クロムの主役。コンテンツテキストは純粋な黒インク。色付きインクはステータス・インタラクション・データの場面で鮮やかに使い、即座の識別を確保する |
| 3 | Typographic Hierarchy | セリフ × サンセリフの対比で構造を表現 |
| 4 | Generous Whitespace | 余白の量と質で読みやすさと格調を生む |
| 5 | Ink Economy | すべての要素に「インクを使う価値があるか」を問う |

## 2. Color System

### 2.1 Ink Scale

コンテンツテキスト・アイコン用のピュアグレースケール。UI クロム（ボーダー・補助テキスト）には Slate Scale（2.2）を使用する。

| Token | Hex | Usage |
|-------|-----|-------|
| `ink-1000` | `#000000` | 見出し・最大強調 |
| `ink-900` | `#1a1a1a` | 本文テキスト |
| `ink-800` | `#2d2d2d` | 強調テキスト |
| `ink-700` | `#404040` | アクティブ要素・フォーカスリング |
| `ink-600` | `#525252` | 本文内補足 |
| `ink-500` | `#6b6b6b` | 本文内キャプション |
| `ink-400` | `#8a8a8a` | 本文内プレースホルダ |
| `ink-300` | `#a3a3a3` | 非活性テキスト |
| `ink-200` | `#c4c4c4` | コンテンツ内セパレーター |
| `ink-100` | `#e0e0e0` | 微細な区切り線 |
| `ink-50` | `#f0f0f0` | 最小区切り線 |

### 2.2 Slate Scale

UI クロム（ボーダー・補助テキスト・グリッド線）用のスケール。青みを帯びたグレーがデジタル画面での視認性と快適さを向上させる。コンテンツテキストには Ink Scale（2.1）を使用する。

| Token | Hex | Usage |
|-------|-----|-------|
| `slate-500` | `#64748b` | セカンダリテキスト・補助情報 |
| `slate-400` | `#94a3b8` | ミュートテキスト・ヒント |
| `slate-300` | `#cbd5e1` | 強調ボーダー |
| `slate-200` | `#e2e8f0` | ボーダー default・グリッド線 |
| `slate-100` | `#f1f5f9` | ホバー背景 |

### 2.3 Paper Scale

背景・サーフェス

| Token | Hex | Usage |
|-------|-----|-------|
| `paper-white` | `#fdfdfc` | ページ背景（上質紙） |
| `paper-cream` | `#faf9f7` | カード背景（生成り） |
| `paper-warm` | `#f5f4f0` | セクション背景（クラフト紙） |
| `paper-kraft` | `#eeedea` | サイドバー・ヘッダー背景 |
| `paper-aged` | `#e8e7e3` | ホバー・アクティブ背景 |
| `paper-shadow` | `#dddcd8` | 影の表現・押下状態 |

### 2.4 Accent Ink

ステータス・インタラクション・データ可視化で即座の識別を確保するカラー。主軸は黒インクだが、意味のある場面では標準的な彩度のインクを使用する。装飾目的では使用しない。

| Token | Hex | Usage |
|-------|-----|-------|
| `ink-blue` | `#2563eb` | リンク・アクティブ状態・選択・フォーカス |
| `ink-green` | `#16a34a` | 成功・利益・完了 |
| `ink-amber` | `#d97706` | 注意・ハイライト・ROI |
| `ink-red` | `#dc2626` | エラー・危険・削除 |

### 2.5 Wash

| Token | Hex | Usage |
|-------|-----|-------|
| `wash-blue` | `#dbeafe` | 選択状態・アクティブ背景 |
| `wash-green` | `#dcfce7` | 成功背景・完了表示 |
| `wash-amber` | `#fef3c7` | 注意背景・ハイライト |
| `wash-red` | `#fee2e2` | エラー背景・警告 |

使用ルール: 色付きインクは意味を伴う場面（ステータス・インタラクション・データ可視化）にのみ使用する。装飾目的では使用しない。主軸はあくまで黒インク（Ink Scale）。

### 2.6 Semantic Tokens

| Token | Maps To | Usage |
|-------|---------|-------|
| `bg-page` | paper-white `#fdfdfc` | ページ全体の背景 |
| `bg-surface` | paper-cream `#faf9f7` | カード・パネル背景 |
| `bg-surface-raised` | paper-white `#fdfdfc` | モーダル・浮上パネル |
| `bg-recessed` | paper-warm `#f5f4f0` | インプット背景 |
| `border-default` | slate-200 `#e2e8f0` | 通常のボーダー・カード枠 |
| `border-strong` | slate-300 `#cbd5e1` | 強調ボーダー |
| `border-heavy` | ink-1000 `#000000` | ヘッダー下線・重要な区切り |
| `text-primary` | ink-900 `#1a1a1a` | 本文テキスト |
| `text-heading` | ink-1000 `#000000` | 見出し |
| `text-secondary` | slate-500 `#64748b` | 補助テキスト・UI ラベル |
| `text-muted` | slate-400 `#94a3b8` | ヒントテキスト・メタデータ |
| `text-caption` | slate-500 `#64748b` | キャプション・注釈 |
| `interactive` | ink-blue `#2563eb` | リンク・選択状態 |
| `interactive-hover` | ink-900 `#1a1a1a` | ホバー状態 |
| `focus-ring` | ink-blue `#2563eb` | フォーカスインジケーター |

### 2.7 Status Colors

テキストラベル・記号で状態を伝えつつ、淡い色付きインクで即座の識別を補助する。

| Status | Label | Symbol | Text | Background | Border |
|--------|-------|--------|------|------------|--------|
| Success | "Complete" | ✓ | `ink-green` | `wash-green` | `ink-green` |
| Warning | "Attention" | ! | `ink-amber` | `wash-amber` | `ink-amber` |
| Error | "Error" | × | `ink-red` | `wash-red` | `ink-red` |
| Info | "Note" | i | `ink-blue` | `wash-blue` | `ink-blue` |

## 3. Typography

### 3.1 Font Family

| Role | Font | Fallback | Usage |
|------|------|----------|-------|
| Serif | Crimson Pro | Georgia, 'Times New Roman', serif | 見出し・タイトル・引用・メトリクス数値 |
| Sans | Instrument Sans | -apple-system, 'Segoe UI', sans-serif | 本文・UI全般 |
| Mono | JetBrains Mono | 'SF Mono', 'Fira Code', monospace | コード・数値 |

### 3.2 Type Scale

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

### 3.3 Typographic Patterns

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

## 4. Spacing

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

## 5. Grid & Layout

### 5.1 Page Structure

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
  Footer (max-w: 1120px, border-top: border-default)
    [Left: Copyright]                        [Right: Confidentiality]
```

### 5.2 Breakpoints

| Token | Width | Layout Changes |
|-------|-------|----------------|
| `bp-mobile` | 0–639px | 4col, gutter 16px, padding 16px, 単一カラム |
| `bp-tablet` | 640–1023px | 8col, gutter 24px, padding 32px |
| `bp-desktop` | 1024–1439px | 12col, gutter 24px, max-w 1120px |
| `bp-wide` | 1440px+ | 12col, gutter 32px, max-w 1280px |

### 5.3 Container

```css
--container-sm:   640px;   /* 記事・フォーム */
--container-md:   840px;   /* 記事（本文幅） */
--container-lg:  1120px;   /* メインレイアウト */
--container-xl:  1280px;   /* ワイドレイアウト */
```

## 6. Shape & Radius

### 6.1 Border Radius

角丸を最小限に抑え、紙の直線的な質感を維持する。

| Token | Value | Usage |
|-------|-------|-------|
| `radius-none` | 0px | **カード・パネル・インプット（デフォルト）** |
| `radius-sm` | 2px | タグ・バッジ |
| `radius-md` | 4px | ボタン |
| `radius-full` | 9999px | ステータスドット |

### 6.2 Stroke Width

| Token | Value | Usage |
|-------|-------|-------|
| `stroke-hairline` | 0.5px | グリッド線・微細なセパレーター |
| `stroke-sm` | 1px | **ボーダー default** |
| `stroke-md` | 1.5px | ナビゲーション下線 |
| `stroke-lg` | 2px | ヘッダー下線・フォーカスリング |
| `stroke-xl` | 3px | セクション区切り（黒線） |

### 6.3 Separators

```css
--separator: 1px solid var(--border-default);   /* slate-200 */
--separator-strong: 1px solid var(--ink-1000);
--separator-dashed: 1px dashed var(--border-strong); /* slate-300 */

.separator-double { border-top: 3px double var(--ink-1000); }
.rule-editorial  { border-bottom: 2px solid var(--ink-1000); padding-bottom: var(--space-3); }
```

## 7. Material System

Glassmorphism / Liquid Glass を使用しない。紙とインクの物理特性をデジタル上で再現する 2 つのマテリアルで構成する。

### 7.1 Material Philosophy

`border` と `box-shadow` は静的な表示状態では同一要素に併用しない。輪郭の定義手段を 1 つに絞ることで、Flat Paper（罫線）と Layered Paper（影）の視覚的差異を明確にする。

| マテリアル | 輪郭の定義 | 禁止（静的状態） |
|---|---|---|
| Flat Paper | `border` | `box-shadow` |
| Layered Paper | `box-shadow` | `border` |

**例外**: ホバー・選択などのインタラクティブ状態では、Flat Paper に一時的な `box-shadow` を追加できる（選択リング: `box-shadow: 0 0 0 2px rgba(37,99,235,0.2)`）。

### 7.2 Flat Paper

罫線のみの基本マテリアル

```css
.paper-flat {
  background: var(--paper-cream);         /* #faf9f7 */
  border: 1px solid var(--border-default); /* slate-200 #e2e8f0 */
  border-radius: 0;
}
.paper-flat:hover { border-color: var(--ink-blue); }

.paper-recessed {
  background: var(--paper-warm);          /* #f5f4f0 — インプット・埋め込み領域 */
  border: 1px solid var(--border-default);
  border-radius: 0;
}
```

### 7.3 Layered Paper

影のみで浮かせるマテリアル。枠線は使用しない。影だけで紙の境界と奥行きを表現する。

```css
.paper-layered {
  background: var(--paper-white);
  border: none;
  border-radius: 0;
  box-shadow: 2px 2px 0 var(--ink-50);  /* フラットな紙の影 */
}

.paper-modal {
  background: var(--paper-white);
  border: none;
  border-radius: 0;
  box-shadow: 4px 4px 0 var(--ink-100), 8px 8px 0 var(--ink-50);  /* 多層影 */
}

.paper-elevated {
  background: var(--paper-white);
  border: none;
  border-radius: 0;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}
```

### 7.4 Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-flat` | `2px 2px 0 #f0f0f0` | 紙片のフラットな影 |
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.06)` | 微小な浮き |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.08)` | ドロップダウン |
| `shadow-lg` | `0 8px 24px rgba(0,0,0,0.1)` | モーダル |

### 7.5 Background Patterns

```css
/* Paper Grain — 紙のざらつき */
.paper-grain::after {
  content: ""; position: absolute; inset: 0; opacity: 0.03; pointer-events: none;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)'/%3E%3C/svg%3E");
}

/* Grid Paper — 方眼紙（Slate 200 の青みがかった罫線） */
.grid-paper {
  background-image:
    linear-gradient(var(--slate-200) 1px, transparent 1px),
    linear-gradient(90deg, var(--slate-200) 1px, transparent 1px);
  background-size: 40px 40px;
  opacity: 0.3;
}
```

## 8. Elevation & Layers

| Token | z-index | Usage |
|-------|---------|-------|
| `z-base` | 0 | 通常コンテンツ |
| `z-raised` | 10 | スティッキーヘッダー |
| `z-dropdown` | 100 | ドロップダウン・ポップオーバー |
| `z-overlay` | 200 | オーバーレイ背景 |
| `z-modal` | 300 | モーダル・ダイアログ |
| `z-toast` | 400 | トースト通知 |
| `z-tooltip` | 500 | ツールチップ |

## 9. Motion & Animation

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

## 10. Iconography

| Property | Value |
|----------|-------|
| Style | Outline（線幅 1.5px）、直線的 |
| Size | 16px（UI）/ 20px（ナビ）/ 24px（装飾） |
| Color | `ink-500`（通常）→ `ink-900`（アクティブ） |
| Set | Lucide（Outline、角丸最小設定） |

テキストラベルを優先し、アイコンの使用は最小限にする。

## 11. Platform-Specific Guidelines

| Platform | 要点 |
|----------|------|
| **Web Page / LP** | 下記「セクション 11.1（Web Page / LP）」に展開 |
| **Web App** | サーフェス階層: `bg-page` → `bg-surface` → `bg-surface-raised`。サイドバー `paper-kraft`。ヘッダー `backdrop-filter: blur(8px)`。本文 `body-md`、密度の高いUIは `body-sm`。**フォント: `--font-sans` のみ使用。Crimson Pro (serif) 不使用。** |
| **Mobile (iOS)** | 下記「セクション 11.3（Mobile App (iOS)）」に展開 |
| **Presentation** | 下記「セクション 11.4（Presentation (pptx)）」に展開 |

### 11.1 Web Page / LP

- ヒーロー `display-xl` light + italic。ヘッダー直下に `border-heavy`。セクション間 `space-9`+。CTA は `btn-primary`。背景にグリッドパターン
- セクション見出し（`.section-header`）の横幅はコンテナ幅（1120px）に統一する。内部の `p` のみ行長制御のため `max-width: 720px; margin: 0 auto` を適用（単一列レイアウトでセクション間の幅が揃う）
- ヒーローサブタイトル等の本文テキストも `max-width: 720px; margin: 0 auto` で行長を統一する

### 11.3 Mobile App (iOS)

#### 基本方針

- iOS Human Interface Guidelines / Layered Paper ガイドラインを優先し、トークンで色・タイポを上書き
- `Layered Paper` は iOS ネイティブの `.glass` modifier と対応させて実装
- SF Pro を基本フォントとし（サンセリフ系のみ使用）、カラートークンのみ本システムから適用。Crimson Pro (serif) は使用しない
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
| Card | `List` with `.listStyle(.insetGrouped)` | `bg`: `bg-surface-raised`, Flat Paper 適用 |
| Input | `TextField` with `.textFieldStyle(.roundedBorder)` | `border`: `border-default`, `bg`: `bg-surface` |
| Badge | `.badge()` modifier | `bg`: Status Colors（Success/Warning/Error） |
| Modal | `.sheet()` / `.fullScreenCover()` | `bg`: `bg-page`, Layered Paper 適用（Hero 背景） |

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

AI がスライドデッキ（pptx / HTML）を生成する際に従うルールセット。カラーパレット・セマンティックトークンはセクション 2（Color System）を参照。マテリアル定義はセクション 7（Material System）を参照。

#### 基本設定

- 出力形式: pptx（PowerPoint）または HTML
- サイズ: 1920×1080px（16:9） — pptx 換算 13.333" × 7.5"
- フォント: Crimson Pro (300,400,600) + Instrument Sans (400,600,700) + JetBrains Mono (400)
- 背景: `paper-white` (#fdfdfc) + グリッドパターン（40px grid, opacity: 0.15）+ Paper Grain（opacity: 0.03）

#### タイポグラフィ

**注意: スライドでは 14px 未満を使わない（copyright・脚注含む）。**

テキストカラーはタイポグラフィでは固定しない。セマンティックトークン（text-heading, text-primary, text-secondary, text-muted 等）を背景色との組み合わせで選択する。

| 用途 | size | weight | line-height | letter-spacing | font |
|------|------|--------|-------------|----------------|------|
| タイトルスライド見出し | 72px | 300 | 1.1 | -1px | Serif |
| スライド見出し（key-message） | 32px | 600 | 1.3 | 0 | Serif |
| カードタイトル | 22px | 600 | 1.3 | 0 | Serif |
| 本文（スライド基準） | 18px | 400 | 1.5 | 0 | Sans |
| カード本文 | 16px | 400 | 1.5 | 0 | Sans |
| セクションラベル（uppercase） | 16px | 700 | 1.2 | 2.5px | Sans |
| サブヘッダー | 16px | 400 | 1.4 | 0 | Sans |
| 数値ハイライト（大） | 44px | 600 | 1.0 | 0 | Serif |
| 数値ハイライト（小） | 32px | 600 | 1.0 | 0 | Serif |
| サブタイトル | 18px | 400 | 1.5 | 0.5px | Sans |
| スライド番号 | 14px | 400 | 1.0 | 0 | Sans |
| copyright | 14px | 400 | 1.0 | 0 | Sans |
| 脚注 | 14px | 400 | 1.4 | 0 | Sans |

#### マテリアル使用ルール

##### マテリアル内テキスト配置

マテリアルグループ（同一種類のマテリアルが横に並ぶ集合）では、代表となる1つのマテリアルについてテキスト配置を決定し、グループ内の全マテリアルに同一ルールを適用する。個別のマテリアルごとに配置を変えない。

| マテリアル | 水平方向 | 垂直方向 | 備考 |
|-----------|---------|---------|------|
| Flat Paper カード | left | top | コンテンツは上から下へ流す |
| Metric カード | center | center | 数値を中央に大きく配置 |
| コードブロック | left | top | コードは左上起点 |

##### 枠線と影の排他使用

`border` と `box-shadow` は同一要素に併用しない。Flat Paper（罫線）と Layered Paper（影）の視覚的差異を維持する。

#### レイアウト

##### スライド共通

```
slide: 1920 × 1080px
slide-inner padding: 50px 72px 80px
  → コンテンツ幅: 1776px (1920 - 72×2)
  → コンテンツ上端: 50px
  → コンテンツ下端: 1000px (1080 - 80)
```

##### スライドコンポーネント

スライドは header / body / footer の3コンポーネントで構成する。各コンポーネントを組み合わせてスライドパターンを作成する。

**Header** — スライド上部の見出し領域。

| サブ要素 | 内容 | タイポグラフィ |
|---------|------|--------------|
| section-label | セクションラベル（例: 「EXECUTIVE SUMMARY」） | 16px / 700 / uppercase / letter-spacing: 2.5px / `text-secondary` |
| key-message | スライド見出し | Serif 32px / 600 / `text-heading` / border-bottom: 2px solid `ink-1000` |
| sub-header（任意） | 補足メッセージ | 16px / 400 / `text-secondary` |

Grid（pptx 座標）:

| プロパティ | px | inch |
|-----------|-----|------|
| left | 72 | 0.50" |
| top | 50 | 0.35" |
| width | 1776 | 12.33" |
| height（section-label + key-message） | 80 | 0.56" |
| height（+ sub-header） | 100 | 0.69" |

**Body** — メインコンテンツ領域。カード・テキスト・図表等を配置する。

Grid（pptx 座標）:

| プロパティ | px | inch |
|-----------|-----|------|
| left | 72 | 0.50" |
| top | header 下端 + 18 | header 下端 + 0.13" |
| width | 1776 | 12.33" |
| height | footer 上端まで（auto） | — |

header→body 間距離は key-message の `margin-bottom: 18px` で制御する。

**Footer** — スライド下部の固定領域。

| サブ要素 | 内容 | タイポグラフィ | 配置 |
|---------|------|--------------|------|
| footer-line | 水平線（セパレーター） | 1px solid `ink-100` | 左右全幅 |
| slide-number | スライド番号 | 14px / 400 / Sans / `text-muted` | 右寄せ |

Grid（pptx 座標）:

| プロパティ | px | inch |
|-----------|-----|------|
| left | 72 | 0.50" |
| top（footer-line） | 1000 | 6.94" |
| top（slide-number） | 1018 | 7.07" |
| width | 1776 | 12.33" |
| height（footer 領域全体） | 80 | 0.56" |

body→footer 間距離は `slide-inner` の `padding-bottom: 80px` で確保する。footer-line は `bottom: 80px`、slide-number は `bottom: 62px` の absolute 配置とする。

##### 距離の制御まとめ

| 距離 | 制御元 | 値 |
|------|--------|-----|
| slide-inner 上余白 | `padding-top` | 50px |
| slide-inner 左右余白 | `padding-left/right` | 72px |
| header → body | `key-message { margin-bottom }` | 18px |
| body → footer-line | `slide-inner { padding-bottom }` | 80px |
| footer-line → slide-number | 配置差分 | 18px |
| slide-inner 下余白（= footer 領域） | `padding-bottom` | 80px |

#### スライドパターン

**1. タイトルスライド（Cover）**
- Header: 使用しない
- Body: 全要素中央配置 — 宛名（border 枠付き）→ タイトル（Serif 72px / 300）→ サブタイトル（18px / 400）
- Footer: 左に会社名、右に日付。上下に `border-top/bottom: 1px solid ink-300`

**2. コンテンツスライド** — 見出し + カードグリッド
- Header: section-label + key-message
- Body: カード配置（flex / grid）
- Footer: footer-line + slide-number

**3. 2カラムスライド** — テキスト + ビジュアル
- Header: section-label + key-message
- Body: `display: flex; gap: 16px`
- Footer: footer-line + slide-number

**4. データスライド** — 数値ハイライト
- Header: section-label + key-message
- Body: Metric カード（center 配置、Serif 44px / 600 + ラベル 18px / `text-muted`）
- Footer: footer-line + slide-number

#### 箇条書き

```css
li { font-size: 18px; color: var(--ink-900); line-height: 1.5; padding-left: 16px; }
li::before { width: 5px; height: 5px; border-radius: 50%; background: var(--ink-400); }
/* sm variant */
li.sm { font-size: 16px; }
```

#### 表（テーブル）

| プロパティ | 値 |
|-----------|-----|
| ヘッダーフォント | 17px / 700 / uppercase / letter-spacing: 1px |
| ヘッダーカラー | `text-secondary` |
| ヘッダー背景 | `paper-warm` |
| ヘッダー下ボーダー | 1.5px solid `ink-900` |
| セルフォント | 18px / 400 |
| セルカラー | `text-primary` |
| セルパディング | 10px 12px |
| セル line-height | 1.5 |
| 行ボーダー | 0.5px solid `ink-100` |
| 数値セル | mono / 17px |

#### 画像・図表

| プロパティ | ルール |
|-----------|-------|
| 最大幅 | body 幅（1776px / 12.33"） |
| アスペクト比 | 元画像の比率を維持 |
| 配置 | body 領域内で水平中央 |
| キャプション | 画像下部、`text-muted`、14px / 400、margin-top: 10px |
| スクリーンショット枠 | 1px solid `ink-200` + `paper-warm` 背景 |
| チャート内テキスト | 14px 以上（視認性確保） |
| 背景透過 | 図表の背景は透過させスライド背景と一体化する |

#### トランジション

| 項目 | ルール |
|------|-------|
| スライド切替 | カット（瞬時切替）をデフォルトとする |
| セクション間切替 | フェード（0.3s）を許可 |
| オブジェクトアニメーション | 使用しない |

#### 禁止事項

- 14px 未満のフォントサイズを使用しない（copyright・脚注含む）
- font-weight: 800 以上は使わない
- `border` と `box-shadow` を同一要素に併用しない
- 1スライドにカード 4枚 or 箇条書き 6項目が上限目安
- スライドの padding を `50px 72px` 未満にしない
- Glassmorphism / Liquid Glass を使用しない
- 装飾目的で色付きインク（Accent Ink）を使用しない

## 12. Usage Quick Reference

<!-- paper コンセプトでは Usage Quick Reference は省略されています。
     必要に応じて、Material Layer Map や Component 早見表を追加してください。 -->

## 13. Component Guidelines

### 13.1 Card `.paper-flat`

| Property | Value |
|----------|-------|
| Background | `bg-surface` (paper-cream) |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-none` (0px) |
| Padding | `space-5` – `space-6` |

- **Hover** (clickable): `border-color: var(--ink-blue)`, `translateY(-2px)`, `box-shadow: var(--shadow-md)`（インタラクティブ状態のみ border + shadow 併用許容）
- **Selected**: `border-color: var(--ink-blue)`, `box-shadow: 0 0 0 2px rgba(37, 99, 235, 0.2)`（選択リング）
- Variants: `.paper-flat`（罫線のみ）/ `.paper-layered`（フラット影）/ `.paper-elevated`（自然影）

### 13.2 Button

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

- **Focus**: `outline: 2px solid var(--ink-blue); outline-offset: 2px`
- **Disabled**: `opacity: 0.3; cursor: not-allowed`
- **Loading**: テキストを `...` に差し替え、`pointer-events: none`

### 13.3 Input `.paper-recessed`

| Property | Value |
|----------|-------|
| Background | `bg-recessed` (paper-warm) |
| Border | `stroke-sm` solid `border-default` |
| Radius | `radius-none` (0px) |
| Height | 40px (md) / 32px (sm) |
| Padding | 0 `space-4` |
| Font | `body-md`, Sans |
| Placeholder | `text-muted` (ink-400) |

- **Hover**: `border-color: var(--border-strong)`
- **Focus**: `border-color: var(--ink-blue)`, `outline: 2px solid var(--ink-blue)`, `outline-offset: 2px`
- **Error**: `border-color: var(--ink-red)`, `border-width: 2px`, エラーメッセージを `ink-red` で表示
- **Disabled**: `background: paper-kraft`, `opacity: 0.5`

### 13.4 Badge / Tag

```css
padding: 0 8px; height: 22px; border-radius: 2px;
font-size: 0.6875rem; font-weight: 600; text-transform: uppercase;
background: var(--paper-warm); color: var(--ink-900); border: 1px solid var(--border-strong);
```

| Status | Label | Background | Text | Border |
|--------|-------|------------|------|--------|
| Active | "LIVE" | `wash-green` | `ink-green` | `ink-green` |
| In Progress | "PILOT" | `wash-blue` | `ink-blue` | `ink-blue` |
| Planned | "PLANNING" | `wash-amber` | `ink-amber` | `ink-amber` |

### 13.5 Modal `.paper-modal`

| Property | Value |
|----------|-------|
| Background | `paper-white` |
| Border | `stroke-sm` solid `border-default` |
| Shadow | `shadow-lg` or 多層フラット影 |
| Max Width | `container-sm` (640px) |
| Padding | `space-6` – `space-7` |
| Overlay | `paper-white` @ 80% opacity |
| z-index | `z-modal` (300) |
| Animation | fadeIn `duration-slow` |

### 13.6 Toast

反転表示（画面上で最も目立つ要素）。

```css
background: var(--ink-900); color: var(--paper-white);
font-size: 0.75rem; padding: 8px 16px; border-radius: 0;
position: fixed; bottom: 24px; z-index: 400;
animation: fadeIn 0.2s ease;  /* auto-dismiss: 3000ms */
```

### 13.7 Navigation / Sidebar

| Property | Value |
|----------|-------|
| Background | `paper-kraft` (#eeedea) |
| Width | 240–280px |
| Border Right | `stroke-sm` solid `border-default` |
| Nav Item | 36px height, `body-md`, `radius-none` |

- **Active**: `color: ink-900`, `font-weight: 600`, `border-left: 2px solid ink-900`
- **Hover**: `color: ink-900`, `background: paper-aged`

### 13.8 Sticky Navigation `.section-nav`

```css
position: sticky; top: 0;
background: rgba(253, 253, 252, 0.95);
backdrop-filter: blur(8px);
z-index: 10;
border-bottom: 1px solid var(--border-default);
```

- **Nav Item**: `font-size: 0.85rem`, `color: var(--text-muted)`, `padding: 12px 16px`
- **Active / Hover**: `color: var(--text-primary)`, `border-bottom: 2px solid var(--ink-blue)`
- IntersectionObserver によるスクロール連動ハイライト

### 13.9 Table

| Property | Value |
|----------|-------|
| Header | `label-md`, bold, uppercase, `text-secondary` |
| Header Border | `stroke-sm` solid `ink-900` |
| Cell | `body-md`, Sans, padding `space-5` |
| Row Border | `stroke-hairline` solid `border-default` |
| Row Hover | `background: paper-warm` |
| Mono Values | `mono-md`（数値・コード） |

### 13.10 Progress Bar

```css
/* Track */  height: 4px; background: var(--border-default); border-radius: 2px;  /* slate-200 */
/* Fill */   background: var(--ink-900); border-radius: 2px; transition: width 0.5s ease-out;
```

### 13.11 Metric Card

Card の拡張。中央揃え、`padding: space-6`。

```
[Value]     — display-md or larger, Serif, light (300), ink-900
[Label]     — body-sm, Sans, text-muted
[Divider]   — border-t ink-50, mt-4 pt-4
[Details]   — body-sm, Sans, flex justify-between
```

### 13.12 Expandable / Accordion

| Property | Value |
|----------|-------|
| Toggle | `body-md`, semibold, `paper-warm` bg, `radius-none` |
| Arrow | `▶` (0.7rem)、展開時 `rotate(90deg)`, transition 0.2s |
| Tree Line | `border-left: 2px solid var(--border-default)`, `margin-left: 12px`, `padding-left: 20px` |
| Content | `max-height: 0` → `.open` で `max-height: 2000px`, transition 0.3s ease-out |

### 13.13 Interaction Patterns

#### Drill-Down Navigation

多段階の情報階層を段階的に掘り下げる。

1. 概要カード群をグリッド表示（Section 1）
2. カードクリック → selected 状態（`border-color: ink-900`）
3. 詳細セクションにスムーズスクロール + コンテンツレンダリング
4. 詳細内の行クリック → アコーディオンで打ち手展開

#### Expandable Tree

- ヘッダークリックで子要素の表示/非表示を切り替え
- 左辺のツリーラインで親子関係を視覚化
- 同時に複数ノードを展開可能

#### Time Period Toggle

- タブボタンで期間を切り替え（例: 1年目 / 3年累計）
- メトリクス値を直接 DOM 書き換え

## 14. CSS Custom Properties Reference

```css
:root {
  /* Typography */
  --font-serif: 'Crimson Pro', Georgia, 'Times New Roman', serif;
  --font-sans: 'Instrument Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-mono: 'JetBrains Mono', 'SF Mono', 'Fira Code', monospace;

  /* Ink Scale — コンテンツテキスト用ピュアグレー */
  --ink-1000: #000000;  --ink-900: #1a1a1a;  --ink-800: #2d2d2d;
  --ink-700: #404040;   --ink-600: #525252;   --ink-500: #6b6b6b;
  --ink-400: #8a8a8a;   --ink-300: #a3a3a3;   --ink-200: #c4c4c4;
  --ink-100: #e0e0e0;   --ink-50:  #f0f0f0;

  /* Slate Scale — UI クロム用（ボーダー・補助テキスト）青みがかったグレー */
  --slate-500: #64748b;  --slate-400: #94a3b8;
  --slate-300: #cbd5e1;  --slate-200: #e2e8f0;  --slate-100: #f1f5f9;

  /* Paper Scale */
  --paper-white: #fdfdfc;  --paper-cream: #faf9f7;  --paper-warm:   #f5f4f0;
  --paper-kraft: #eeedea;  --paper-aged:  #e8e7e3;  --paper-shadow: #dddcd8;

  /* Accent Ink */
  --ink-blue: #2563eb;    --ink-green: #16a34a;
  --ink-amber: #d97706;   --ink-red: #dc2626;

  /* Accent Wash (backgrounds) */
  --wash-blue: #dbeafe;   --wash-green: #dcfce7;
  --wash-amber: #fef3c7;  --wash-red: #fee2e2;

  /* Semantic */
  --bg-page: var(--paper-white);         --bg-surface: var(--paper-cream);
  --bg-surface-raised: var(--paper-white); --bg-recessed: var(--paper-warm);
  --border-default: var(--slate-200);    --border-strong: var(--slate-300);
  --border-heavy: var(--ink-1000);
  --text-primary: var(--ink-900);        --text-heading: var(--ink-1000);
  --text-secondary: var(--slate-500);    --text-muted: var(--slate-400);
  --text-caption: var(--slate-500);

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
  --separator: 1px solid var(--border-default);      /* slate-200 */
  --separator-strong: 1px solid var(--ink-1000);
  --separator-dashed: 1px dashed var(--border-strong); /* slate-300 */
}
```

## 15. Dependencies

- **Tailwind CSS**: ユーティリティクラスベース。カスタムプロパティを `tailwind.config` で拡張
- **Google Fonts**: Crimson Pro (300, 400, 600, 400italic), Instrument Sans (400, 600)
- **JetBrains Mono**: Google Fonts or self-hosted
- **Lucide Icons**: Outline スタイル、角丸最小
- **JavaScript**: Vanilla JS（IntersectionObserver, accordion 制御）
