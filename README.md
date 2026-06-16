# Anchor

> 制御できることに、心を繋ぎ止める。

気になっていることを書き出し、**自分の領域（制御できる）／領域外（制御できない）**に仕分けて、領域外は手放し、自分の領域には小さな一手をひとつだけ置く。
古代ストア派エピクテトス『提要』の「制御の二分法」を、責めずに使える道具にしたものです。Ataraxia Works の「鎮める」軸——Still（身体から鎮める）の隣に、Anchor（論理から鎮める）。

## 思想（守るべき原則）

- 責めずに、ただ仕分ける。
- 鎮めるための道具であって、続けるための道具ではない。**ストリーク・連続日数・達成バッジは作らない。**
- TODOアプリにしない。動かせることに置く一手は **一件につき一つだけ。**
- 急かさない。通知なし。途中でやめてもいい。
- すべて端末の中だけ。広告・追跡・ログインなし。オフライン対応（PWA）。

## 構成

- ビルド不要・1ファイル完結（`index.html` + `manifest.json` + `sw.js`）
- localStorage キー `anchor_v1`
- ダーク基調（静かな水面）。「手放す」でカードが沈むモーション。

## アイコンの作り直し

```sh
convert -background none icons/icon.svg -resize 192x192 icons/icon-192.png
convert -background none icons/icon.svg -resize 512x512 icons/icon-512.png
```

## デプロイ（Cloudflare Pages）

1. このリポジトリを Cloudflare Pages に接続
2. ビルド設定：フレームワークなし／ビルドコマンド空欄／出力ディレクトリ `/`
3. カスタムドメイン（例：`anchor.xdcyw.net`）を割り当て

© 2026 田中志 / Ataraxia Works

## アップデート履歴

## 2026-06-16
- OGタグ追加（og:title / og:description / og:image / og:url / og:type / twitter:card）
- キーボードアクセシビリティ改善（:focus-visible スタイル追加）
- manifest.json 整備（scope・categories・orientation 修正）
