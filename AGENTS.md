# AGENTS.md — iniestabluu-website

このファイルのスコープはリポジトリ全体です。

## 目的
UI/UX とフロントエンド改善を一貫した品質で進める。

## 優先ルール
1. まず既存ページ4枚（`index.html` / `corporate.html` / `lp.html` / `ec.html`）の構造整合性を保つ。
2. 変更はアクセシビリティを最優先（コントラスト、フォーカス可視性、代替テキスト）。
3. 文言・導線変更はモバイル（375px）とPC（1440px）の両方を前提に検討する。
4. UI変更時は「目的」「対象ユーザー」「期待する行動」を短く明記してから実装する。
5. フォント・カラー規約は `/CLAUDE.md` と `/company-website/CLAUDE.md` に従う（和文: Zen Kaku Gothic New / 英字: Inter / モノクロ）。勝手に変更しない。

## 実装ガイド
- セマンティックHTMLを優先（`header` `main` `section` `footer`）。
- ボタン/リンクは目的が伝わるラベルを使う（例: 「お問い合わせ」）。
- 余白・タイポ・色はページ間で揃える。
- 画像には `alt` を付与し、装飾画像は空altを使う。
- 背景画像divには `role="img"` + `aria-label`、装飾divには `aria-hidden="true"` を付与する。

## 作業フロー
1. 要件を1文で定義。
2. 最小変更で実装。
3. 4ページの共通UI差分チェック。
4. 表示確認（モバイル/PC）。
5. 変更点サマリと確認コマンドを提示。

## 追加スキル
UI/UX 専用の実行手順は `skills/uiux-frontend/SKILL.md` を参照。
