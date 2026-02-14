# Thumbnail / OGP Design Rules

このファイルは AI がサムネイル・OGP 画像用 HTML を生成する際に従うルールセットである。
template.html はこのルールで構築されたビジュアルリファレンスである。ブラウザで開いて見た目を確認できる。

## サイズ

| パターン | サイズ | 用途 |
|---------|--------|------|
| OGP | 1200×630px | og:image, Twitter Card, Slack preview |
| YouTube | 1280×720px | YouTube サムネイル |

## 基本設定

```css
body {
  font-family: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  -webkit-font-smoothing: antialiased;
}
```

## カラー

| 役割 | 値 |
|------|-----|
| 背景 | #000000 |
| タイトル | #ffffff |
| サブタイトル | #7e7e8c |
| タグテキスト | #6b84c0 |
| タグ背景 | rgba(80,104,164,0.15) |
| タグボーダー | rgba(107,132,192,0.3) |
| ロゴ | #7e7e8c |
| ボトムライン | #5068a4 → #8e7cb4 グラデーション |

## タイポグラフィ

| 要素 | OGP (1200×630) | YouTube (1280×720) | weight | color |
|------|----------------|---------------------|--------|-------|
| タイトル | 48px | 56px | 300 | #ffffff |
| サブタイトル | 20px | 24px | 400 | #7e7e8c |
| タグ | 13px | 13px | 600 | #6b84c0 |
| ロゴ | 14px | 14px | 600 | #7e7e8c |

letter-spacing: タイトルは -1.5px、タグは 1.5px (uppercase)、ロゴは 3px (uppercase)

## 背景

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

## 構成要素

すべて任意。タイトルのみ必須。全要素中央配置。

### タグ（上部ラベル）
```css
padding: 6px 16px; font-size: 13px; font-weight: 600;
letter-spacing: 1.5px; text-transform: uppercase; color: #6b84c0;
background: rgba(80,104,164,0.15); border: 1px solid rgba(107,132,192,0.3);
border-radius: 4px;
```

### タイトル
```css
/* OGP */ font-size: 48px;
/* YouTube */ font-size: 56px;
font-weight: 300; line-height: 1.1; letter-spacing: -1.5px; color: #ffffff;
max-width: 80%; /* 端に寄りすぎない */
```

### サブタイトル
```css
/* OGP */ font-size: 20px;
/* YouTube */ font-size: 24px;
font-weight: 400; color: #7e7e8c; max-width: 70%; line-height: 1.4;
```

### ロゴ
```css
font-size: 14px; font-weight: 600; letter-spacing: 3px;
text-transform: uppercase; color: #7e7e8c;
```

### ボトム装飾ライン
```css
position: absolute; bottom: 0; left: 0; right: 0; height: 3px;
background: linear-gradient(90deg, transparent 0%, #5068a4 30%, #8e7cb4 50%, #5068a4 70%, transparent 100%);
```

### テキストグラデーション（装飾用）
```css
background: linear-gradient(90deg, #e8e8ec 0%, #8f99b8 100%);
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
```

## HTML 構造

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

## 禁止事項

- 背景色を #000000 以外にしない
- タイトルを 40px 未満にしない
- font-weight: 700 は使わない
- テキストを 4行以上にしない（1〜2行推奨）
- コンテンツの max-width を 80% より広くしない
