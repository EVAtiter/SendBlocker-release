[English](README.md) | [日本語](README.ja.md)

# SendBlocker

指定したアプリでだけ **Return キーと Shift+Return キーの動作を入れ替える**、macOS メニューバー常駐のユーティリティです。

チャットツールで「改行のつもりで Return を押して、送信してしまう」のを防ぎます。Return が改行に、Shift+Return が送信になります。

**➡️ [最新版をダウンロード](https://github.com/EVAtiter/SendBlocker-release/releases/latest)**

---

## 変換のしかた

| 押したキー | 対象アプリに届くキー |
| --- | --- |
| Return | Shift+Return（改行） |
| Shift+Return | Return（送信） |
| Command / Option / Control ＋ Return | そのまま（変換しない） |

対象に登録したアプリが前面にあるときだけ変換します。それ以外のアプリでは、Return はいつもどおりに動きます。

---

## インストール

### Homebrew

```bash
brew install --cask EVAtiter/tap/sendblocker
```

Homebrew 7 以降で「untrusted tap」と表示されたら、先に次のコマンドで sendblocker を信頼してから、もう一度インストールしてください。

```bash
brew trust --cask evatiter/tap/sendblocker
```

### 手動

1. [Releases](https://github.com/EVAtiter/SendBlocker-release/releases/latest) から `SendBlocker-x.x.x.zip` をダウンロード
2. 解凍して `SendBlocker.app` を「アプリケーション」フォルダへ移動
3. 起動するとメニューバーに ↩ アイコンが出ます（Dock には表示されません）

---

## 使い方

1. メニューバーの ↩ アイコン → **「対象アプリ」→「実行中のアプリから追加…」** を開き、一覧から追加したいアプリを**ダブルクリック**します（一覧に出るのは起動中のアプリだけです）
2. メニューの **「有効」** を選びます
3. 初めて有効にするときは、アクセシビリティの許可を求める案内が出ます。「システム設定を開く」から、**システム設定 → プライバシーとセキュリティ → アクセシビリティ** で SendBlocker を ON にし、もう一度 **「有効」** を選びます

対象アプリを外すには、「対象アプリ」の一覧でアプリ名の右の **✕** の項目を選びます。

---

## 主な機能

- **キーの入れ替え** — Return ↔ Shift+Return（Command / Option / Control との組み合わせは変換しません）
- **対象アプリの限定** — 登録したアプリでだけ動作します（1 つも登録していなければ変換しません）
- **有効 / 無効の切り替え** — メニューの「有効」から。対象アプリを登録してあれば、起動時に自動で有効になります
- **ログイン時に開く** — システム設定の「ログイン項目」と連動します
- **メニューを隠す** — メニューバーのアイコンを隠します。隠しても動作し続けます。戻すには Finder から SendBlocker をもう一度起動します
- **日本語 / 英語対応** — システムの言語に従います

---

## ご注意

- SendBlocker が動いている最中にアクセシビリティの許可を外すと、数秒〜10 秒ほど、キー入力が反応しなくなることがあります（その後は戻り、メニューの「有効」のチェックが外れます）。許可を外すときは、先に SendBlocker を終了してください
- 許可を戻しても自動では再開しません。メニューの「有効」を選び直してください

---

## プライバシー

ネットワーク通信をしません。入力したキーの内容を記録・保存しません。保存するのは対象アプリの一覧だけで、
`~/Library/Application Support/SendBlocker/settings.json` に置きます。

---

## アンインストール

- Homebrew で入れた場合: `brew uninstall --cask sendblocker`（設定も消すときは `brew uninstall --zap --cask sendblocker`）
- 手動で入れた場合: SendBlocker を終了し、`SendBlocker.app` をゴミ箱へ移動します。設定も消すときは `~/Library/Application Support/SendBlocker/` を削除します

---

## 対応 OS

macOS 13.0 Ventura 以降 / Apple Silicon（arm64）専用 / Apple 公証済み

---

Copyright © 2026 EVA Titer. All rights reserved.
