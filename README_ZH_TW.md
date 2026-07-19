🌐 [English](README.md) | [简体中文](README_CN.md) | **繁體中文** | [日本語](README_JA.md) | [한국어](README_KO.md)

<div align="center">

# Wonderful Launcher for ComfyUI（Windows）

### 下載了 ComfyUI 工作流，下一步就是讓它真正跑起來。

[**下載 2.1.11**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11) · [**官方網站**](https://wonderfullauncher.com/) · [**文件**](https://wonderfullauncher.com/docs) · [**回報問題**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## 下載

- **建議下載**：[Wonderful Launcher 2.1.11 Setup](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)
- **安裝檔**：`WonderfulLauncher-Setup-v2.1.11.exe`
- **校驗檔**：同一個 Release 裡的 `SHA256SUMS.txt`
- **上一個穩定版本**：[2.1.10](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.10)

> [!WARNING]
> 請不要下載 GitHub 自動產生的 `Source code.zip` 或 `Source code.tar.gz`。那些是原始碼壓縮包，不是 Windows 安裝程式。

> [!TIP]
> 一般安裝包已包含桌面程式所需執行環境，不需要另外安裝 Microsoft .NET Desktop Runtime。

<p align="center">
  <img src="assets/screenshots/home-launch-surface.png" alt="Wonderful Launcher home screen" width="86%" />
</p>

---

## 這個工具解決什麼問題？

如果你下載了 ComfyUI 工作流，卻卡在缺模型、紅節點、缺依賴或啟動失敗，Wonderful Launcher 會把排查和修復集中在同一個桌面工作區裡：

| 你遇到的情況 | Wonderful Launcher 會協助你 |
|--------------|------------------------------|
| 已經有 ComfyUI | 匯入現有 ComfyUI 或便攜版資料夾 |
| 想要乾淨環境 | 部署新的 ComfyUI 套件 |
| ComfyUI 啟動失敗 | 顯示啟動日誌，並在你同意後執行修復 |
| 工作流缺模型 | 匹配模型名稱，下載或放到正確目錄 |
| 工作流缺節點 | 安裝缺失自訂節點和依賴 |
| 多個 ComfyUI 共用模型 | 設定共享模型目錄 |

## 2.1.11 更新重點

- ComfyUI 啟動時不再因 Torch 探測超時而彈出誤導性的修復提示。
- 缺失模型會在正在執行的 ComfyUI WebView 工作區內處理。
- 模型結果列表更精簡，聚焦模型名稱、目標目錄、匹配狀態和下載動作。
- 模型共享設定改成更清楚的 A → B 結構。
- 圖片生成對話中的 prompt 更容易選取和複製。

## 快速開始

1. 開啟 [最新版 Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)。
2. 下載 `WonderfulLauncher-Setup-v2.1.11.exe`。
3. 安裝後匯入現有 ComfyUI，或部署一個新的 ComfyUI 套件。
4. 如果工作流缺模型或節點，依照通知列提示進行匹配、下載或修復。

本倉庫是 Windows 安裝包、截圖與問題回報入口，不是完整桌面端原始碼鏡像。
