# Concept Master Guide

新しいデザインコンセプトを作成する際のガイドラインです。

## 使い方

### 1. ディレクトリのコピー

```bash
cp -r concept-master/ {new-concept}/
cd {new-concept}/
```

### 2. プレースホルダの置換

`design-system.md` 内の `{{PLACEHOLDER}}` 形式のプレースホルダを一括置換します。

**主要プレースホルダ一覧**:

| カテゴリ | プレースホルダ | 説明 | 例（digital） | 例（paper） | 例（utopia） |
|---------|---------------|------|---------------|------------|--------------|
| **Identity** | | | | | |
| | `{{CONCEPT_NAME}}` | コンセプト名 | Digital | Paper | Utopia |
| | `{{CONCEPT_SLUG}}` | URL/ディレクトリ名用 | digital | paper | utopia |
| | `{{CONCEPT_TAGLINE}}` | 1行の概要説明 | ダークファーストデザインシステム | Editorial / Magazine-inspired design | ルネサンス期の油絵に着想を得た |
| | `{{CONCEPT_DESCRIPTION}}` | 2-3文の概要 | Glassmorphism・Liquid Glass の... | 紙とインクで成立する... | 漆黒の Raw Umber キャンバスの上に... |
| **Color** | | | | | |
| | `{{BG_BASE}}` | ページ背景色 | `#000000` | `#fdfdfc` | `#0c0a08` |
| | `{{TEXT_PRIMARY_HEX}}` | プライマリテキスト色 | `#e8e8ec` | `#1a1a1a` | `#e8e7e3` |
| | `{{PRIMARY_NAME}}` | プライマリカラー名 | Steel Blue | Ink Scale | Ultramarine |
| | `{{PRIMARY_BASE_HEX}}` | プライマリ基準色 (500) | `#5068a4` | `#000000` | `#3d4f9e` |
| | `{{SECONDARY_NAME}}` | セカンダリカラー名 | Silver | Paper Scale | Burnt Sienna |
| | `{{ACCENT_NAME}}` | アクセントカラー名 | Violet Smoke | Accent Ink | Vermillion |
| **Typography** | | | | | |
| | `{{FONT_DISPLAY}}` | 見出し用フォント | DM Sans | Crimson Pro | Playfair Display |
| | `{{FONT_BODY}}` | 本文用フォント | DM Sans | Instrument Sans | Source Sans 3 |
| | `{{FONT_MONO}}` | モノスペースフォント | JetBrains Mono | JetBrains Mono | JetBrains Mono |
| | `{{FONT_DISPLAY_ROLE}}` | 見出しフォントの分類 | Sans | Serif | Serif |
| | `{{FONT_BODY_ROLE}}` | 本文フォントの分類 | Sans | Sans | Sans |
| **Material** | | | | | |
| | `{{MATERIAL_A_NAME}}` | マテリアルA名 | Glassmorphism | Flat Paper | Impasto |
| | `{{MATERIAL_A_METAPHOR}}` | マテリアルAのメタファー | ガラスの透過と反射 | 罫線のみの基本マテリアル | 厚塗りの存在感 |
| | `{{MATERIAL_B_NAME}}` | マテリアルB名 | Liquid Glass | Layered Paper | Glaze |
| | `{{MATERIAL_B_METAPHOR}}` | マテリアルBのメタファー | 液体ガラスの流動感 | 影のみで浮かせるマテリアル | 薄塗りの透明な奥行き |
| **Presentation** | | | | | |
| | `{{PPTX_PADDING}}` | スライド padding | `64px 80px` | `50px 72px 80px` | `64px 80px` |
| | `{{PPTX_CONTENT_WIDTH}}` | コンテンツ幅 | `1760px` | `1776px` | `1760px` |
| | `{{PPTX_HEADER_LEFT}}` | Header left 座標 (px) | `80` | `72` | `80` |
| | `{{PPTX_HEADER_TOP}}` | Header top 座標 (px) | `64` | `50` | `64` |
| | `{{PPTX_FOOTER_TOP}}` | Footer top 座標 (px) | `1032` | `1000` | `1032` |
| | `{{PPTX_MIN_FONT_SIZE}}` | 最小フォントサイズ | `10px` | `14px` | `10px` |

**一括置換コマンド例**:

```bash
# Identity
sed -i '' 's/{{CONCEPT_NAME}}/YourConcept/g' design-system.md
sed -i '' 's/{{CONCEPT_SLUG}}/your-concept/g' design-system.md
sed -i '' 's/{{CONCEPT_TAGLINE}}/Your tagline here/g' design-system.md

# Color
sed -i '' 's/{{BG_BASE}}/#yourcolor/g' design-system.md
sed -i '' 's/{{TEXT_PRIMARY_HEX}}/#yourcolor/g' design-system.md
sed -i '' 's/{{PRIMARY_NAME}}/Your Primary Name/g' design-system.md

# 以下同様にすべてのプレースホルダを置換...
```

### 3. ガイドコメントを参照しながら記述

`design-system.md` 内の `<!-- GUIDE: ... -->` コメントを読みながら、各セクションを記述します。

**ガイドコメントの種類**:
- `<!-- GUIDE: ... -->`: このセクションで何を定義すべきかの説明
- `<!-- GUIDE-CHOICE: ... -->`: 複数のパターンから選択する箇所（Color 構成、pptx grid 等）
- `<!-- GUIDE-REF: ... -->`: GUIDE.md の該当セクションへの参照

### 4. ガイドコメントの削除

新規コンセプトが完成したら、ガイドコメントを一括削除します。

**削除コマンド**:

```bash
# 単一行コメントの削除
sed -i '' '/<!-- GUIDE.*-->/d' design-system.md

# 複数行コメントの削除（必要な場合）
perl -0777 -i -pe 's/<!-- GUIDE.*?-->\n?//gs' design-system.md
```

### 5. GUIDE.md と references/ の削除

GUIDE.md は concept-master/ でのみ必要なため、新規コンセプトからは削除できます。

```bash
rm GUIDE.md
# references/ は必要に応じて残す（インスピレーション記録用）
```

### 6. HTML ファイルのプレースホルダ置換

`viewers/` と `templates/` 配下の HTML ファイルの `:root` ブロック内の `/* TODO: {{...}} */` コメントを参照し、CSS カスタムプロパティの値を置換します。

```html
<!-- 置換前 -->
:root {
  --bg-page:     #000000;  /* TODO: {{BG_BASE}} */
  --text-primary: #e8e8ec; /* TODO: {{TEXT_PRIMARY_HEX}} */
}

<!-- 置換後 -->
:root {
  --bg-page:     #yourcolor;
  --text-primary: #yourcolor;
}
```

## セクション別ガイド

### Design Principles の設計

5つの原則を定義します。

**構成パターン**:
1. **コンセプトの軸** — Dark-First, Paper-First, Old Masters' Canvas 等、コンセプトの核心的な方向性
2. **美的方針** — Minimal & Precise, Restrained Color, Chromatic Depth 等、美的判断の基準
3. **マテリアルの2軸** — Two Materials, Impasto & Glaze, 枠線と影の使い分け 等、マテリアル体系の哲学
4. **システムの一貫性** — Systematic Consistency（全テーマ共通）
5. **プラットフォーム適応性** — Platform Adaptive（全テーマ共通）

**既存コンセプトの原則比較**:

| # | digital | paper | utopia |
|---|---------|-------|--------|
| 1 | Dark-First | Paper-First | Old Masters' Canvas |
| 2 | Minimal & Precise | Restrained Color | Impasto & Glaze |
| 3 | Two Materials | Typographic Hierarchy | Chromatic Depth |
| 4 | Systematic Consistency | Generous Whitespace | Tactile Warmth |
| 5 | Platform Adaptive | Ink Economy | Modern Precision |

### Color System の設計

**Pattern A: 4色系統型**（digital/utopia）
- Primary（ブランドカラー）
- Secondary（補助色・テキスト用）
- Accent（強調・装飾用）
- Neutral（背景・ボーダー・テキスト）
- 各色系統を 50～950 の 11段階で定義（Neutral は 0～1000 の 13段階）

**Pattern B: Ink/Paper 2軸型**（paper）
- Ink Scale（テキスト・ボーダー・アイコン用、10段階）
- Paper Scale（背景・サーフェス用、6段階）
- Accent Ink（色付きインク、4色）
- Wash（淡い色付き背景、4色）

**セマンティックトークンの設計**:
- `bg-*`: 背景用（page, surface, surface-raised 等）
- `border-*`: ボーダー用（default, subtle, strong 等）
- `text-*`: テキスト用（primary, secondary, muted, disabled 等）
- `interactive-*`: インタラクティブ要素用（default, hover, active 等）
- `glow-*` / `cta-*`: グロウ・CTA 用（コンセプトに応じて）
- `focus-ring`: フォーカスリング用

**Status Colors**:
- Success, Warning, Error, Info の4種
- 各ステータスを 400/500/600/900 の4段階で定義

### Typography の設計

**フォント選定基準**:
1. **Display/Heading用**: コンセプトの世界観を体現するフォント（Serif or Sans）
2. **Body用**: 可読性の高いフォント（通常 Sans）
3. **Mono用**: コード・数値用（JetBrains Mono 推奨）

**Type Scale の設計**:
- 12～14トークンを定義
- 必須: display-xl/lg/md, heading-lg/md/sm, body-lg/md/sm, label-lg/md/sm, mono-md/sm
- size: 11px ～ 72px の範囲
- weight: コンセプトの tone に応じて選択（digital: 300-600, paper: 300-700, utopia: 400-900）
- line-height: 見出しは 1.1～1.4、本文は 1.5～1.7
- letter-spacing: 大きい見出しはマイナス、uppercase ラベルはプラス

**Weight Selection Guide**:
- Light (300): display 見出し・メトリクス数値
- Regular (400): 本文
- Medium (500): サブ見出し・強調
- Semibold (600): heading・ラベル・ボタン
- Bold (700): セクションラベル・uppercase
- Extrabold (800-900): 特殊な強調（utopia のみ）

### Material System の設計

**2マテリアル体系**:

すべてのコンセプトで「2つのマテリアル」を定義します。静/動、罫線/影、厚塗り/薄塗り等、対比する2つの表現軸を設定します。

**既存コンセプトの比較**:

| | Material A | Material B | 対比軸 |
|---|-----------|-----------|--------|
| digital | Glassmorphism | Liquid Glass | 静/動 |
| paper | Flat Paper | Layered Paper | 罫線/影 |
| utopia | Impasto | Glaze | 厚塗り/薄塗り |

**Material Selection Guide**:

| ユースケース | 推奨マテリアル | 理由 |
|-------------|--------------|------|
| ヒーローセクション | Material B | インパクト・動的表現 |
| CTA ボタン | Material B | 強調・視線誘導 |
| コンテンツカード | Material A | 静的・読みやすさ |
| サイドバー・ヘッダー | Material A | 控えめ・邪魔しない |

**枠線と中塗りの使い分けルール**:
- digital/utopia: 基本的に併用しない。例外: 薄い中塗り + 同系統の枠線
- paper: **排他使用** — Flat Paper（border使用、shadow禁止） / Layered Paper（shadow使用、border禁止）

**CSS 実装の粒度**:
- 各マテリアルを 3～4 バリアント定義（standard, frosted/subtle, tinted/gilded, deep 等）
- Dark Mode と Light Mode の両方を定義（paper は単一モードのため不要）

### Presentation (pptx) の設計

**grid 座標の選択**:

`<!-- GUIDE-CHOICE: ... -->` に従い、Pattern A（均等 padding 型）または Pattern B（非対称 padding 型）を選択します。

**Pattern A: 均等 padding 型**（digital / utopia）
- padding: `64px 80px`
- content width: `1760px`
- header-body gap: `40px`

**Pattern B: 非対称 padding 型**（paper）
- padding: `50px 72px 80px`（top/lr/bottom）
- content width: `1776px`
- header-body gap: `18px`（key-message の margin-bottom）

**最小フォントサイズ**:
- digital/utopia: `10px`（copyright 用）
- paper: `14px`（copyright・脚注含む全要素）

**スライドパターンの設計**:
- タイトルスライド（Cover）
- コンテンツスライド（カードグリッド 3列）
- 2カラムスライド（テキスト + ビジュアル）
- データスライド（数値ハイライト）

**禁止事項の定義**:
- 最小フォントサイズ違反
- font-weight の上限（800 or なし）
- タイポグラフィへのカラー固定
- 枠線と中塗りの併用
- 1スライドあたりの要素数上限
- padding の最小値

### Mobile App (iOS) の設計

iOS Human Interface Guidelines（HIG）と Material Design の要件を統合し、プラットフォームネイティブな体験を優先しながらデザインシステムのトークンを適用する。

**コアセクション（必須）**:

1. **基本方針** — iOS HIG 優先、SF Pro フォント、Dynamic Type サポート、マテリアルのパフォーマンス最適化

2. **Layout & Touch Targets**（レイアウトとタッチ領域）
   - Touch Target Size: 最小 44×44pt、推奨 48×48pt
   - Safe Area: 全コンテンツを Safe Area 内に配置
   - Spacing: 最小パディング `space-4`（12px）

3. **Navigation Patterns**（ナビゲーションパターン）
   - Tab Bar: 3～5タブ、常時表示、選択状態の明確化
   - Navigation Bar: Large Title、自動生成の戻るボタン
   - Modal/Sheet: スワイプ解除、`.sheet()` vs `.fullScreenCover()` の使い分け
   - Alert/Action Sheet: 破壊的アクションの赤表示、キャンセルボタン配置

4. **Interaction & Feedback**（インタラクションとフィードバック）
   - Response Time: 100ms以内の視覚フィードバック
   - Haptics: `UIImpactFeedbackGenerator` による触覚フィードバック
   - Loading Indicators: `.progressView` の適切な使用

5. **Typography Mapping** — SF Pro Text/Display の使い分け、Dynamic Type サイズクラスと Type Scale の対応

6. **Component Mapping** — iOS ネイティブコンポーネントとデザインシステムトークンの対応表

7. **Motion & Animation** — Spring animation パラメータ、Transition duration、Easing curve

**オプション要素（コンセプトの特性に応じて追加）**:
- Accessibility 詳細（Contrast Ratios, VoiceOver, Reduce Motion, Reduce Transparency）
- Dark Mode との統合方針
- Size Class 対応（iPhone/iPad）
- Android 対応（Material Design）
- ウィジェット・App Clips 等の拡張機能

**設計の粒度**:
- コアセクションで 80～100 行を目指す
- iOS HIG の必須要件（Touch Target, Safe Area, Navigation）はすべて網羅する
- コードサンプルは Swift + SwiftUI で記述する

### Component Guidelines の設計

**必須8コンポーネント**:
1. Button（Variants, Sizes, States）
2. Card
3. Input / Text Field
4. Badge / Tag
5. Modal / Dialog
6. Toast / Notification
7. Navigation / Sidebar
8. Table

**コンポーネント定義の粒度**:
- Variants: Primary, Secondary, Ghost, Danger 等
- Sizes: sm, md, lg 等
- States: Default, Hover, Active, Focus, Disabled, Loading, Error 等
- CSS: 簡潔なコードブロック
- Light Mode差分: Dark 優先コンセプトのみ

## 既存コンセプト比較表

### 主要パラメータ比較

| パラメータ | digital | paper | utopia |
|-----------|---------|-------|--------|
| **行数** | 1,712 | 822 | 1,596 |
| **セクション数** | 13 | 15 | 14 |
| **背景色** | `#000000` | `#fdfdfc` | `#0c0a08` |
| **テキスト色** | `#e8e8ec` | `#1a1a1a` | `#e8e7e3` |
| **フォント（Display）** | DM Sans | Crimson Pro | Playfair Display |
| **フォント（Body）** | DM Sans | Instrument Sans | Source Sans 3 |
| **マテリアルA** | Glassmorphism | Flat Paper | Impasto |
| **マテリアルB** | Liquid Glass | Layered Paper | Glaze |
| **pptx padding** | 64px 80px | 50px 72px 80px | 64px 80px |
| **pptx content width** | 1760px | 1776px | 1760px |
| **pptx 最小フォント** | 10px | 14px | 10px |
| **カラー構成** | 4色系統 | Ink/Paper 2軸 | 4色系統 |
| **Light Mode** | あり | なし | あり |

### タイポグラフィ比較

| 用途 | digital | paper | utopia |
|------|---------|-------|--------|
| **display-xl size** | 72px | 56px | 72px |
| **display-xl weight** | 300 | 300 | 700 |
| **heading-lg weight** | 500 | 600 | 700 |
| **body-md size** | 14px | 14px | 14px |
| **body-md weight** | 400 | 400 | 400 |

### Material 哲学比較

| | digital | paper | utopia |
|---|---------|-------|--------|
| **Material A** | ガラスの透過と反射 | 罫線のみの基本マテリアル | 厚塗りの存在感 |
| **Material B** | 液体ガラスの流動感 | 影のみで浮かせるマテリアル | 薄塗りの透明な奥行き |
| **排他ルール** | 枠線と中塗りの使い分け | 枠線と影の排他使用 | 枠線と中塗りの使い分け |

## チェックリスト

新規コンセプト作成時に以下をチェックしてください。

### Foundations

- [ ] Design Principles（5原則）
- [ ] Color Palette（4色系統 or Ink/Paper 2軸）× 11段階
- [ ] Semantic Tokens（bg-*, border-*, text-*, interactive-*, focus-ring）
- [ ] Light Mode Tokens（Dark 優先の場合）
- [ ] Status Colors（4種 × 4段階）
- [ ] Font Family（3 roles: Display/Body/Mono）
- [ ] Type Scale（12～14トークン）
- [ ] Font Weight（4～7段階）
- [ ] Weight Selection Guide
- [ ] Spacing（11段階: space-0 ～ space-11）
- [ ] Breakpoints（4段階: mobile/tablet/desktop/wide）
- [ ] Container（4サイズ: sm/md/lg/xl）
- [ ] Border Radius（7段階、コンセプト哲学に応じた標準値設定）
- [ ] Stroke Width（5段階: hairline/thin/default/thick/xl）

### Materials

- [ ] Material Philosophy（2マテリアルの定義表）
- [ ] Material Selection Guide
- [ ] Material A（3～4バリアント）
- [ ] Material B（3～4バリアント）
- [ ] Light Mode Material（Dark 優先の場合）
- [ ] 枠線と中塗りの使い分けルール
- [ ] Gradients（5～8種類）
- [ ] Glow Effects（box-shadow 3～5種、gradient 3～4種）
- [ ] Shadows（4段階: sm/md/lg/xl）
- [ ] Decorative Lines（3～4種類）

### Platform Guidelines

- [ ] Web Page / LP（タイポグラフィ表、マテリアル選択、レイアウト、ボタン、カード、バッジ、入力、アニメーション、レスポンシブ、禁止事項）
- [ ] Web App（簡潔な箇条書き: サーフェス階層、サイドバー/ヘッダー、フォーカスリング）
- [ ] Mobile App（基本方針、Accessibility、Layout & Touch Targets、Navigation Patterns、Interaction & Feedback）
- [ ] Presentation (pptx)
  - [ ] 基本設定（サイズ、フォント、背景）
  - [ ] タイポグラフィ表（最小サイズ宣言含む）
  - [ ] マテリアル使用ルール（テキスト配置、枠線と中塗り）
  - [ ] レイアウト（padding、header/body/footer grid 座標）
  - [ ] スライドパターン（4種: タイトル/コンテンツ/2カラム/データ）
  - [ ] 箇条書き、コードブロック、表、画像、ロゴ、トランジション
  - [ ] 禁止事項
- [ ] Thumbnail / OGP（サイズ、タイポグラフィ、背景、構成要素、禁止事項）

### Components

- [ ] Button（Variants, Sizes, States, CSS, Light差分）
- [ ] Card（基本CSS、ホバー、Light差分）
- [ ] Input（States, CSS, Light差分）
- [ ] Badge（サイズ、Status, CSS）
- [ ] Modal（CSS, Overlay, Animation）
- [ ] Toast（CSS、配置、Auto Dismiss）
- [ ] Navigation（CSS、Active/Hover）
- [ ] Table（Header、Cell、Row、CSS）

## よくある質問

### Q: プレースホルダの置換は必須ですか？

A: はい。`{{PLACEHOLDER}}` をそのまま残すと、design-system.md が完成しません。すべてのプレースホルダを新しいコンセプトの値に置換してください。

### Q: ガイドコメントを残したままでも動作しますか？

A: Markdown としては問題ありません（HTML コメントのため非表示）。ただし、新規コンセプトとして公開する場合は削除することを推奨します。

### Q: HTML ファイルは必ず全て作成する必要がありますか？

A: いいえ。必要なメディアに応じて選択的に作成できます。例えば、Presentation (pptx) が不要な場合は `templates/presentation.html` と `viewers/presentation.html` を削除できます。

### Q: digital/paper/utopia と異なる構造にできますか？

A: できます。concept-master はあくまでテンプレートであり、新しいコンセプトに必要なセクションを追加・削除することは自由です。ただし、3コンセプト間の一貫性を保つために、可能な限り同じ構造を維持することを推奨します。
