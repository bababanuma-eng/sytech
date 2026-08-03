# S&YTech 事業紹介サイト

Stripe の事業確認（Activate your account）に提出するための、S&YTech の事業紹介サイト。
静的 HTML/CSS のみ。ビルド不要。

## 構成

```
index.html        LP 本体（ヒーロー／導線図／課題／提供するもの／決済／料金／運営者／お問い合わせ）
tokushoho.html    特定商取引法に基づく表記
privacy.html      プライバシーポリシー
assets/style.css  スタイル一式
assets/favicon.svg
```

## ローカルで確認する

```
python3 -m http.server 8080
# → http://localhost:8080
```

## 公開

GitHub Pages（`main` ブランチのルート）で配信。push すれば自動で反映される。

## 注意

- **パスワード保護をかけないこと。** Stripe の要件（誰でも閲覧できること）。
- ページ内の表記「S&YTech」は Stripe 登録事業名と一致させること。変更しない。
- 料金は「個別見積り」表記。金額を決めたら `index.html` の `#price` セクションと
  `tokushoho.html` の「販売価格」を更新する。
- 導入事例（juju）はクライアント許諾が取れてから追加する。現状は未掲載。
