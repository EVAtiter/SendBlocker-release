# SendBlocker

指定したアプリでのみ **Return キーと Shift+Return キーの動作を入れ替える**、macOS メニューバー常駐ユーティリティです。

チャットツールで「Return を押したつもりが誤送信してしまう」のを防ぎます。Return が改行に、Shift+Return が送信になります。

---

## ダウンロード

最新版は [Releases](https://github.com/EVAtiter/SendBlocker-release/releases/latest) からダウンロードできます。

1. `SendBlocker-x.x.x.zip` を解凍し、`SendBlocker.app` を「アプリケーション」フォルダへ移動
2. 初回起動後、**システム設定 → プライバシーとセキュリティ → アクセシビリティ** で SendBlocker を許可
3. メニューバーの ↩ アイコンから「対象アプリ」を追加して利用開始

---

## 主な機能

- **キー入れ替え** — Return ↔ Shift+Return（Command / Option / Control との組み合わせは変換しません）
- **対象アプリの限定** — 指定したアプリでのみ動作（未設定時は変換しません）
- **ログイン時に開く** — システム設定のログイン項目と双方向同期
- **メニューを隠す** — メニューバーアイコンを一時的に非表示
- **日本語 / 英語対応** — OS の言語設定に追従

---

## 対応 OS

macOS 13.0 Ventura 以降 / Apple Silicon（arm64）専用 / Apple 公証済み

---

Copyright © 2026 EVA Titer. All rights reserved.
