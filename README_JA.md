🌐 [English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH_TW.md) | **日本語** | [한국어](README_KO.md)

<div align="center">

# Wonderful Launcher for ComfyUI on Windows

### ComfyUI ワークフローをダウンロードしたら、次は実際に動かせる状態にしましょう。

[**2.1.11 をダウンロード**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11) · [**公式サイト**](https://wonderfullauncher.com/) · [**ドキュメント**](https://wonderfullauncher.com/docs) · [**問題を報告**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## ダウンロード

- **推奨**：[Wonderful Launcher 2.1.11 Setup](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)
- **インストーラー**：`WonderfulLauncher-Setup-v2.1.11.exe`
- **チェックサム**：同じ Release にある `SHA256SUMS.txt`
- **前の安定版**：[2.1.10](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.10)

> [!WARNING]
> GitHub が自動生成する `Source code.zip` や `Source code.tar.gz` はダウンロードしないでください。これらはソースアーカイブであり、Windows インストーラーではありません。

> [!TIP]
> 通常のインストーラーには必要なデスクトップ実行環境が含まれています。Microsoft .NET Desktop Runtime を別途インストールする必要はありません。

<p align="center">
  <img src="assets/screenshots/home-launch-surface.png" alt="Wonderful Launcher home screen" width="86%" />
</p>

---

## 何を解決するツールですか？

ComfyUI ワークフローが、モデル不足、赤いノード、依存関係不足、起動エラーで止まることがあります。Wonderful Launcher は、その復旧作業を現在使っている ComfyUI パッケージの近くにまとめます。

| 状況 | Wonderful Launcher が手伝うこと |
|------|----------------------------------|
| すでに ComfyUI がある | 既存の ComfyUI または portable ComfyUI フォルダーをインポート |
| クリーンな環境がほしい | 新しい ComfyUI パッケージをデプロイ |
| ComfyUI が起動しない | 起動ログを表示し、承認した修復タスクを実行 |
| ワークフローにモデルが足りない | モデル名を照合し、必要なフォルダーへダウンロードまたは配置 |
| ワークフローにノードが足りない | 不足している custom node と依存関係をインストール |
| 複数の ComfyUI で同じモデルライブラリを使いたい | 共有モデルディレクトリを設定 |

## 2.1.11 の主な変更

- Torch の事前検出がタイムアウトしただけで、誤解を招く修復ダイアログを出さないようにしました。
- 不足モデルの処理は、実行中の ComfyUI WebView ワークスペース内で行います。
- モデル結果一覧は、モデル名、配置先フォルダー、照合状態、ダウンロード操作に集中しました。
- 共有モデルフォルダー設定を、より分かりやすい A → B レイアウトにしました。
- 画像生成ダイアログ内の prompt を選択・コピーしやすくしました。

## クイックスタート

1. [最新 Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11) を開きます。
2. `WonderfulLauncher-Setup-v2.1.11.exe` をダウンロードします。
3. インストール後、既存の ComfyUI をインポートするか、新しい ComfyUI パッケージをデプロイします。
4. ワークフローに不足モデルや不足ノードがある場合は、通知バーの案内に従って照合、ダウンロード、修復を行います。

このリポジトリは、Windows インストーラー、スクリーンショット、Issue 受付のための公開ページです。デスクトップアプリ本体の完全な公開ソースコードミラーではありません。
