# S&YTech 事業紹介サイト

Stripe の事業確認（Activate your account）に提出するための、S&YTech の事業紹介サイト。
静的 HTML/CSS のみ。ビルド不要、JavaScript なし。

## 構成

```
index.html        LP 本体
                  ヒーロー＋事業サマリー → 01 提供するもの → 02 導線
                  → 03 お金の流れ → 04 料金 → 05 運営者情報 → 06 お問い合わせ
tokushoho.html    特定商取引法に基づく表記
privacy.html      プライバシーポリシー
assets/style.css  スタイル一式
assets/favicon.svg
```

## デザインの決めごと

- 純白（`#FFFFFF`）基調。面・影・カードは使わず、余白と細い罫で構造をつくる
- 全セクションが「左＝番号ラベル（スクロール追従）／右＝本文」の台帳レイアウト
- 色面はパイングリーン（`#0E5C4A`）1 色。塗りを使うのは「お金の流れ」の 1 ブロックのみ
  （ヘッダーの公式LINE ボタンと `#contact` の `.line-cta` は黒地／ホバーで緑）
- 書体：Murecho（和文・見出し）／ Space Grotesk（番号・欧文ラベル・メールアドレス）

## ローカルで確認する

```
python3 -m http.server 8080
# → http://localhost:8080
```

## 公開

GitHub Pages（`main` ブランチのルート）で配信。push すれば自動で反映される。
https://bababanuma-eng.github.io/sytech/

## 注意

- **パスワード保護をかけないこと。** Stripe の要件（誰でも閲覧できること）。
- ページ内の表記「S&YTech」は Stripe 登録事業名と一致させること。変更しない。
- 料金は「個別見積り」表記。金額を決めたら `index.html` の `#price` セクションと
  `tokushoho.html` の「販売価格」を更新する。
- 導入事例（juju）はクライアント許諾が取れてから追加する。現状は未掲載。
- 想定読者は「個人事業主・小規模事業者」。特定の業種（ネイル等）に限定する表現は
  使わない。業種を挙げる場合は例示にとどめる。
- 公式LINE の URL は `https://lin.ee/tbjOB0D`。掲載箇所は `index.html`（ヘッダー CTA・
  05 連絡先・06 お問い合わせ・フッター）、`tokushoho.html`（公式LINEアカウント欄・
  フッター）、`privacy.html`（1. 取得する情報・9. お問い合わせ窓口・フッター）。
  変更時はこの 3 ファイルをまとめて更新する。
- 代表者名はローマ字表記。漢字に差し替える場合は `index.html`（サマリー・05）と
  `tokushoho.html`・`privacy.html` の 3 ファイルを更新する。
