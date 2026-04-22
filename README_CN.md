🌐 [English](README.md) | **简体中文**

<div align="center">

# ComfyUI 安装 下载教程

### 一款 Windows 上的 ComfyUI 启动器，让你从工作流到出图，更快一步。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.cumulative_downloads&style=for-the-badge&logo=github&label=下载量)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**下载稳定版**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**Beta / 抢先体验**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**更新日志**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**反馈问题**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

</div>

---

## 为什么需要 ModelFinder

每个新的 ComfyUI 工作流都可能意味着缺模型、缺插件、依赖报错。你还没点"Queue Prompt"，就已经在 HuggingFace、Civitai 和 GitHub 之间来回跳了。

ModelFinder 把**工作流分析、资源下载、环境管理和启动运行**集中在一个地方 — 让你把时间花在出图上，而不是折腾环境。

<div align="center">
<img src="screenshots/home.png" width="80%" alt="首页 — 启动并监控 ComfyUI，内置终端实时输出">
</div>

---

## 快速开始

### 首次使用

1. 从 [Releases](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) 下载 **Setup 安装包** 或 **免安装 ZIP**
2. 启动 ModelFinder — 部署向导会引导你安装 ComfyUI（选择版本、GPU 加速方式、可选组件）
3. 或者跳过部署，直接将已有的 ComfyUI 便携包导入管理
4. **已经装了 ComfyUI Desktop？** 直接添加 `文档\ComfyUI` 文件夹即可，ModelFinder 会自动识别 Desktop 安装

无需安装 Python 或 .NET，所有依赖已内置。

### 日常使用

打开 ModelFinder → 在首页点击 **启动** → ComfyUI 的运行日志实时显示在内置终端中 → 就绪后在内置浏览器中直接使用 ComfyUI，或在外部浏览器打开。

基础使用就是这么简单。其他功能在你需要时随时可用。

---

## 你可以做什么

### 首页 — 启动与监控

你的起点。全屏终端控制台实时显示 ComfyUI 日志，右下角的悬浮操作岛可以一键启动/停止 ComfyUI、打开 Web UI 或切换实例。**内置浏览器工作区**让你无需离开启动器即可使用 ComfyUI。你也可以在这里配置启动参数（端口、GPU 显存模式、自定义参数），以及快速打开常用目录（models、outputs、custom_nodes）。

遇到问题时，**AI 诊断**功能可以分析你的日志、建议修复命令、在你确认后执行，并验证修复效果 — 不满意还能一键回滚。

<details>
<summary>截图</summary>

| AI 诊断 | 硬件监控 |
|:---:|:---:|
| <img src="screenshots/ai-diagnosis.png" width="400"> | <img src="screenshots/hardware-monitor.png" width="400"> |

</details>

### 环境 — 部署与包管理

**部署**：一键安装全新的 ComfyUI 环境，可选版本、GPU 加速方式（NVIDIA CUDA / AMD ROCm）和预装组件（ComfyUI-Manager、翻译包、常用节点等），可视化分步进度，失败可恢复。

**包管理**：同时管理多个 ComfyUI 安装，包括 **ComfyUI Desktop** 安装。一眼看到 Python/PyTorch/ComfyUI 版本和磁盘占用。可视化切换 PyTorch/CUDA 版本，升级或回滚 ComfyUI 内核，导出/导入 pip 环境，清理 pip 缓存。

<details>
<summary>截图</summary>

| 部署向导 | 包管理 | PyTorch 管理 |
|:---:|:---:|:---:|
| <img src="screenshots/deployment.png" width="270"> | <img src="screenshots/package-manager.png" width="270"> | <img src="screenshots/pytorch-manager.png" width="270"> |

</details>

### 工作流 — 批量任务与体检

**批量任务**通过 ComfyUI API 实现自动化批量出图。加载工作流，配置参数替换（支持从文件批量导入提示词），设置重复次数和随机种子，定义自动重启间隔避免内存泄漏，中断后可恢复。

**工作流体检**帮你在运行前检查工作流是否存在问题。

<details>
<summary>截图</summary>

| 批量任务 | 依赖分析 |
|:---:|:---:|
| <img src="screenshots/batch-queue.png" width="400"> | <img src="screenshots/dependency-analysis.png" width="400"> |

</details>

### 插件 — 管理与安装

浏览所有已安装的自定义节点，查看 Git 信息、大小，支持搜索。可以按 commit 切换插件版本、回滚，或管理 Python 依赖。

加载需要你没装的插件的工作流时，**安装缺失插件** tab 会自动检测并一键安装（Git clone + pip 依赖）。

<details>
<summary>截图</summary>

<img src="screenshots/plugin-management.png" width="80%">
</details>

### 模型 — 模型库、查找与下载

**模型库**提供本地模型文件的可视化浏览，支持按分类筛选（checkpoint、LoRA、VAE 等）和搜索。

**模型查找**是核心差异化功能。拖入工作流（JSON 或 PNG），自动扫描本地模型、识别缺失项，并从云端模型目录中匹配 HuggingFace、ModelScope、Civitai 等来源的下载地址。确认匹配后一键下载全部。支持多文件或整文件夹批量分析。

**下载中心**是统一的下载任务管理器，实时进度、暂停/恢复、批量清理。

<details>
<summary>截图</summary>

| 模型查找 | 模型库 | 下载中心 |
|:---:|:---:|:---:|
| <img src="screenshots/model-finder.png" width="270"> | <img src="screenshots/model-management.png" width="270"> | <img src="screenshots/download-center.png" width="270"> |

</details>

---

## 个性化

- **语言**：简体中文 / English / 跟随系统 — 即时切换，无需重启
- **主题**：深色 / 浅色，切换时 ComfyUI 界面同步生效
- **配色方案**：多种主题配色可选
- **界面密度**：舒适 / 紧凑
- **减少动画**：低配设备可关闭过渡动画
- 采用 **Windows Fluent Design** 设计语言，现代原生体验

<details>
<summary>截图</summary>

| 深色主题（中文） | 浅色主题（英文） | 设置 |
|:---:|:---:|:---:|
| <img src="screenshots/home.png" width="270"> | <img src="screenshots/light-theme-english.png" width="270"> | <img src="screenshots/settings.png" width="270"> |

</details>

---

## 发布通道

| 通道 | 适合 |
|------|------|
| **Stable 稳定版** | 大多数用户 — 推荐的公开稳定版 |
| **Beta 测试版** | 想提前体验新功能、能接受偶尔粗糙的用户 |

所有功能目前免费提供。Beta 版本在同一仓库发布，可能包含未定型的功能或临时性回归。

---

## 系统要求

| 项目 | 要求 |
|------|------|
| **操作系统** | Windows 10 (22H2+) / Windows 11 |
| **磁盘空间** | 启动器本体 ~100 MB |
| **显卡** | 运行 ComfyUI 建议 NVIDIA (CUDA) 或 AMD (ROCm) |
| **运行时** | 无需额外安装，所有依赖已内置 |

---

## 常见问题

<details>
<summary><b>需要单独安装 Python 或 .NET 吗？</b></summary>

不需要。ModelFinder 是独立运行的程序，ComfyUI 的 Python 环境由部署向导自动配置。
</details>

<details>
<summary><b>支持接管已有的 ComfyUI 安装吗？</b></summary>

支持。进入 环境 → 包管理，添加已有的 ComfyUI 便携包目录即可，原有文件不会被修改。
</details>

<details>
<summary><b>支持接管 ComfyUI Desktop 吗？</b></summary>

支持。添加 `文档\ComfyUI` 文件夹，ModelFinder 会自动识别 Desktop 安装，关联其 Python 环境、自定义节点和模型。Desktop 的文件不会被修改，ModelFinder 只读取不写入。
</details>

<details>
<summary><b>支持 AMD 显卡吗？</b></summary>

支持。部署时可选择 AMD ROCm 模式，已有的 AMD 环境也可直接导入。
</details>

<details>
<summary><b>AI 诊断怎么用？</b></summary>

在 设置 → AI 设置 中配置 API Key 和端点。ComfyUI 启动失败时，AI 会分析日志、生成修复命令，确认后执行。不满意可一键回滚。
</details>

<details>
<summary><b>支持 macOS 或 Linux 吗？</b></summary>

目前仅支持 Windows 10/11。
</details>

<details>
<summary><b>从 ComfyLauncher (v1.3.x) 升级？</b></summary>

ModelFinder 会自动迁移 `%AppData%/ComfyLauncher` 中的配置。`ComfyLauncher.exe` 和 `ModelFinder.exe` 均可识别，升级无缝。
</details>

---

## 反馈

- **Bug 反馈 / 功能建议**：[Issues](https://github.com/hu-haibin/ModelFinder-Releases/issues)
- 如果觉得好用，欢迎给个 Star

---

## 许可与声明

ModelFinder 是闭源软件，仅在此仓库发布编译后的可执行程序。
本项目与 ComfyUI 官方无隶属关系，ComfyUI 是独立的开源项目。

---

<div align="center">

**ModelFinder** — 从工作流到出图，告别环境折腾。

Made with ❤️ for the AI Art Community

</div>
