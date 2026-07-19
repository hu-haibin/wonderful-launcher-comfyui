🌐 [English](README.md) | **简体中文** | [其他语言](README_I18N.md)

<div align="center">

# Wonderful Launcher for ComfyUI（Windows 版）

### 你下载了一个 ComfyUI 工作流，现在把它真正跑起来。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/wonderful-launcher-comfyui?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
[![产品下载量](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2Fwonderful-launcher-comfyui%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=%E4%BA%A7%E5%93%81%E4%B8%8B%E8%BD%BD%E9%87%8F)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)

[**下载 2.1.11**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11) · [**官网**](https://wonderfullauncher.com/) · [**文档**](https://wonderfullauncher.com/docs) · [**反馈问题**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## 下载

- **普通用户推荐**：[Wonderful Launcher 2.1.11 Setup 安装包](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)
- **安装包文件**：`WonderfulLauncher-Setup-v2.1.11.exe`
- **校验文件**：同一个 release 里的 `SHA256SUMS.txt`
- **备用版本**：[2.1.10](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.10) 会保留为上一个稳定 fallback

> [!WARNING]
> 不要下载 GitHub 自动生成的 `Source code.zip` 或 `Source code.tar.gz`。那些是源码压缩包，不是 Windows 安装包。

> [!TIP]
> 正常安装包已经自带桌面运行所需组件，不需要额外安装 Microsoft .NET Desktop Runtime。

> [!IMPORTANT]
> 如果旧版本下载了更新，但重启后又打开旧应用，请直接运行上面的最新 **Setup 安装包**。它会保留启动器数据，把旧 `ModelFinder` / `Wonderful Launcher` 数据收敛到 `WonderfulLauncher`，清理旧更新状态，并启动最新版。

<p align="center">
  <img src="assets/screenshots/home-launch-surface.png" alt="Wonderful Launcher 首页" width="86%" />
</p>

---

## 如果你也遇到过这种情况

你看到一个想试的工作流，下载下来，打开 ComfyUI，然后发现一堆红节点、缺模型、缺依赖，或者启动日志里只告诉你“坏了”，但没告诉你下一步该怎么做。

Wonderful Launcher 主要就是为这段折腾做的。它把这些实际维护动作放到你正在使用的 ComfyUI 包旁边：

| 你想做什么 | 启动器帮你做什么 |
|------------|--------------------|
| “我电脑里已经有 ComfyUI。” | 导入 ComfyUI Desktop 或便携版 ComfyUI。 |
| “这个环境太乱了，我想重新来。” | 下载并部署一个干净的 ComfyUI 包。 |
| “ComfyUI 启动不了。” | 显示启动日志，并执行你批准的依赖修复任务。 |
| “这个工作流说缺模型。” | 匹配模型名称，并下载或放到预期目录。 |
| “工作流缺节点。” | 安装自定义节点和依赖，不用手动翻文件夹。 |
| “我有几个 ComfyUI 包，但模型想共用一份。” | 在不同 ComfyUI 包之间共享模型目录。 |
| “我想出图，也想保留历史和参考图。” | 把图片生成、参考图、历史记录和 Photoshop 发送放在同一个工作区。 |

它不是要替代 ComfyUI，而是帮你少做那些“为什么这个工作流在我电脑上跑不起来”的杂活。

---

## 2.1.11 更新了什么

发布于 2026 年 7 月 20 日。[查看完整 GitHub Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)。

- **ComfyUI 启动更干净**：移除了容易误导用户的 Torch 启动前探测链路，不再因为探测超时就弹修复框。
- **缺失模型回到运行中的工作区处理**：移除了工具箱里独立的模型查找入口。WebView 通知条会直接打开当前工作流的缺失模型结果。
- **模型结果更清楚**：列表聚焦工作流模型名、目标模型目录、匹配状态和下载动作；批量操作改成“复制模型名称”和“下载全部”。
- **共享模型目录更紧凑**：ComfyUI 设置页用更清晰的 A → B 结构展示模型共享，并显示当前包是否正在使用全局共享模型路径。
- **图片 prompt 复制更顺手**：图片生成对话里的 prompt 文本可以更自然地选择和复制。

本次发版已通过完整 Release 测试、官方发布脚本打包，以及发布根目录隔离启动 smoke。

---

## 快速开始

### 1. 安装

1. 打开 [最新版安装包 release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)。
2. 下载 `WonderfulLauncher-Setup-v2.1.11.exe`。
3. 运行安装包并打开 Wonderful Launcher。

这个仓库是公开下载、截图和 issue 跟踪入口，不是桌面应用的公开源码镜像。

### 2. 告诉启动器你的 ComfyUI 在哪里

- 已经有 ComfyUI：选择 **导入 ComfyUI**，选择包含 `main.py` 的目录，或包含 `ComfyUI` 子文件夹的便携包上层目录。
- 想要干净环境：打开 ComfyUI 设置，选择磁盘和运行包，部署完成后从首页启动。

不要误选 `models`、`custom_nodes`、`output`、`python_embeded`，也不要选择只放工作流文件的目录。

### 3. 让工作流告诉你缺什么

如果工作流打开后出现红节点、缺模型或缺依赖，可以按这个循环处理：

1. 检查缺失模型或节点
2. 下载或放置缺失文件
3. 安装缺失节点或依赖
4. 重启或重新运行 ComfyUI
5. 验证工作流是否可以正常出图

---

## 功能截图

<p align="center">
  <img src="assets/screenshots/feature-environment.png" alt="环境管理" width="32%" />
  <img src="assets/screenshots/feature-model-manager.png" alt="模型管理" width="32%" />
  <img src="assets/screenshots/feature-plugin-manager.png" alt="插件管理" width="32%" />
</p>

<p align="center">
  <img src="assets/screenshots/home-live-startup-logs.png" alt="启动日志与启动状态" width="32%" />
  <img src="assets/screenshots/feature-image-workspace.png" alt="图片工作区" width="32%" />
  <img src="assets/screenshots/feature-image-photoshop-send.png" alt="发送到 Photoshop" width="32%" />
</p>

---

## 常见问题

<details>
<summary><b>为什么有些 Windows 位置里还是会看到 ModelFinder 或 mf？</b></summary>

Wonderful Launcher 是对外产品名。部分内部标识会继续保留 `ModelFinder` 或 `mf`，用于兼容已有安装目录、更新链、日志和 Windows 身份。

</details>

<details>
<summary><b>需要先安装 Python 吗？</b></summary>

不需要。正常路径下，Wonderful Launcher 会帮你管理 ComfyUI 的 Python 环境。

</details>

<details>
<summary><b>可以接管我现有的 ComfyUI 吗？</b></summary>

可以。使用 **导入 ComfyUI**，选择包含 `main.py` 的目录，或包含 `ComfyUI` 子文件夹的便携包上层目录即可。

</details>

<details>
<summary><b>Agent 会自动执行修复动作吗？</b></summary>

不会。涉及写入或修复的动作需要你授权。Agent 负责辅助诊断，并在你同意后调用受支持的启动器工具。

</details>

<details>
<summary><b>支持 macOS 或 Linux 吗？</b></summary>

目前不支持。这个仓库发布的是 Windows 桌面构建。

</details>

---

## Release 和仓库范围

GitHub Releases 页面会保持精简：最新版安装包 + 上一个稳定 fallback。旧 tag 会保留作为历史记录，但旧 release 页面可能会被清理，避免新用户下载过期构建。

- [最新版本](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
- [Wonderful Launcher 2.1.11](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)
- [Wonderful Launcher 2.1.10 fallback](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.10)

这个仓库不会公开完整桌面端源码。公开 release 资产是 GitHub Releases 中附带的 Windows 安装包和校验文件。
