# company-website（iniestabluu 公式サイト）

稼働中の会社サイト本体。ルートの `CLAUDE.md` に加え、このフォルダ固有のルール。

## ページ構成

- `index.html` トップ（ヒーロー＋サービス概要＋お問い合わせ）
- `corporate.html` コーポレートサイト制作ページ
- `lp.html` LP制作ページ
- `ec.html` ECサイト制作ページ

4ページとも同じヘッダー・フッター構造。どれか1つ更新したら他3つも整合性チェックする。

## セクション順（ランディング系ページ共通）

1. ヒーロー（canvas mockup）
2. サービス内容
3. 料金表
4. 制作実績（ポートフォリオ）
5. 制作フロー
6. FAQ
7. お問い合わせ

## canvas mockupのルール

- DPR scaling（`ctx.scale(dpr, dpr)`）必須
- フォントサイズはclampで動的計算：`Math.min(Math.max(Math.round(w*0.055), 14), 22)`
- 縦位置はフォントサイズから算出：`const aY1 = 70 + aFS; const aY2 = aY1 + aFS + 4;`
- テキスト重なり防止のため、固定px値は使わない

## 料金表記

サイト内の料金表記は `README.md`（リポジトリルート）と必ず一致させる。変更時は両方更新。

## 変更時チェックリスト

- [ ] 4ページ間でヘッダー・フッター一致
- [ ] モバイル表示（375px）・PC表示（1440px）両方で確認
- [ ] canvas mockupのテキスト重なりチェック
- [ ] デプロイ → Vercel URLで実機確認
