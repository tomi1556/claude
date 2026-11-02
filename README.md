# 作品置き場

Claude と作ったページを公開する場所。`main` に push すると Cloudflare が自動で公開します。

## 作品の足し方

1. `works/<名前>/index.html` に作品を置く（画像などは同じフォルダに。リンクは相対パスで書く）
2. `works.json` に1件足す

```json
{ "path": "works/<名前>/", "title": "題名", "desc": "ひとこと説明", "tag": "種類", "date": "2026-11-02" }
```

## ファイル

| ファイル | 役割 |
|---|---|
| `index.html` | 一覧（`works.json` を読んで並べる。探す・種類でしぼる） |
| `404.html` | 見つからないとき |
| `wrangler.jsonc` | Cloudflare の公開設定（ビルドなし） |
| `.assetsignore` | 公開しないファイル（設定ファイル・この説明など） |
