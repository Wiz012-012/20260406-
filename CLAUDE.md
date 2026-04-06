# CLAUDE.md

## プロジェクト概要
株式会社Wiz（ワイズ）のBtoB営業用ランディングページ（LP）プロジェクト。
初回商談前に送付し、「この会社と話したい」と思わせることを目的とした営業資料。

## ファイル構成
- `wiz-lp.html` — メインLP（1ファイル完結、Tailwind CSS使用）
- `tabelog_toshima_restaurants.json` — 食べログ豊島区エリア店舗データ（400件、メタデータ付き）
- `tabelog_data_only.json` — 店舗データのみ（LP埋め込み用）

## LP構成
1. ファーストビュー — キャッチコピー + CTA
2. 課題提示 — 中小企業DXの3大つまずき
3. 解決策 — Wizの総合DX支援モデル
4. ベネフィット — 導入効果（数値比較）
5. 信頼要素 — 実績数値 + Wiz cloudリンク
6. 食べログ豊島区店舗一覧 — 検索・フィルタ・ソート・ページネーション付き（400件）
7. Why Now — 今やるべき理由
8. 導入フロー — 4ステップ
9. CTA — 無料相談予約フォーム

## 技術スタック
- HTML（1ファイル完結）
- Tailwind CSS（CDN）
- Vanilla JavaScript（フィルタ・ページネーション・スクロールアニメーション）
- Google Fonts（Noto Sans JP）

## 外部連携
LP内の各要素は https://012cloud.jp/ の以下ページにリンク:
- ヘッダーロゴ → トップページ
- ヘッダーナビ → サービス一覧 / 導入事例
- FV「300」→ サービス一覧
- FV「ITの総合商社」→ Wiz cloudとは？
- 対応領域カード → 業種別・カテゴリ別ページ
- 信頼セクション → サービス一覧 / 導入事例 / 資料DL
- CTAフォーム下 → Webフォーム / 経営相談フォーム
- フッター → 7つの主要ページリンク

## GitHub
- リポジトリ: https://github.com/Wiz012-012/20260406-
- ブランチ: main

## ローカル確認方法
```bash
cd "/Users/012-grp/AI研修20260406 ②"
python3 -m http.server 8080
# ブラウザで http://127.0.0.1:8080/wiz-lp.html を開く
```

## コーディング規約
- 1ファイル完結（HTMLにCSS/JSを内包）
- Tailwind CSSのユーティリティクラスを使用
- カスタムカラーはtailwind.configで定義（primary, accent, dark等）
- モバイルファースト設計（md:プレフィックスでデスクトップ対応）
