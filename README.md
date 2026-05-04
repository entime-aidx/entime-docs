# entime-docs

株式会社Entime 社内ドキュメント公開リポジトリ。

公開URL: https://docs.entime.jp

## 目的

- 関係先（税理士・パートナー等）向けの説明資料をHTMLで公開
- 修正後 git push で同URLに即反映できる運用

## 公開中ドキュメント

| ドキュメント | URL |
|---|---|
| 経理フロー変更案内（税理士向け） | https://docs.entime.jp/keiri-flow-tax-accountant.html |

## 更新フロー

```bash
# 1. ローカルで編集
vim keiri-flow-tax-accountant.html

# 2. コミット＆プッシュ
git add .
git commit -m "経理フロー資料の修正"
git push origin main

# 3. 数十秒後、同URLに反映
```

## デプロイ構成

- ホスティング: GitHub Pages (entime-aidx/entime-docs)
- DNS: Cloudflare
- 独自ドメイン: docs.entime.jp

## ディレクトリ

```
entime-docs/
├── CNAME                              # 独自ドメイン設定
├── index.html                         # 目次ページ
├── keiri-flow-tax-accountant.html     # 経理フロー資料
└── README.md
```

## 備考

- robots: noindex（検索エンジンには載せない）
- 直接URLを知っている人のみアクセス可能（security by obscurity）
- 機微情報は載せない方針
