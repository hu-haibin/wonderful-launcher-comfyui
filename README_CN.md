🌐 [English](README.md) | **简体中文**

<div align="center">

# ComfyUI 安装 下载教程

### ComfyUI 启动器和管理器 — 模型下载、自定义节点一键安装、环境管理、工作流分析，一站式搞定。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.cumulative_downloads&style=for-the-badge&logo=github&label=下载量)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**下载稳定版**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**Beta / 抢先体验**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**更新日志**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**反馈问题**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

</div>

---

## 为什么需要 ModelFinder

每个新的 ComfyUI 工作流都可能意味着缺模型、缺自定义节点、依赖报错。你还没点"Queue Prompt"，就已经在 HuggingFace、Civitai 和 GitHub 之间来回跳了。

ModelFinder 是一款 **ComfyUI 启动器和管理器**，把工作流分析、模型下载、自定义节点安装和环境管理集中在一个地方 — 让你把时间花在出图上，而不是折腾环境。

---

## 快速开始

### 首次使用

1. 从 [Releases](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) 下载 **Setup 安装包** 或 **免安装 ZIP**
2. 启动 ModelFinder — 一键安装向导引导你部署 ComfyUI（选择版本、GPU 加速方式、可选组件）
3. 或者跳过部署，直接将已有的 ComfyUI 便携包导入管理
4. **已经装了 ComfyUI Desktop？** 直接添加 `文档\ComfyUI` 文件夹即可，ModelFinder 会自动识别 Desktop 安装

无需安装 Python 或 .NET，所有依赖已内置。

### 日常使用

打开 ModelFinder → 在首页点击 **启动** → ComfyUI 的运行日志实时显示在内置终端中 → 就绪后在内置浏览器工作区中直接使用 ComfyUI，或在外部浏览器打开。

基础使用就是这么简单。其他功能在你需要时随时可用。

---

## 你可以做什么

### 首页 — 启动与监控

你的起点。胶囊式控制按钮一键启动/停止 ComfyUI。运行后，内置浏览器工作区直接在启动器内打开 ComfyUI 的 Web UI，无需切换窗口。

底部工具栏提供常用文件夹快捷入口（Models、Output、Workflows、Custom Nodes、Python）和使用统计（今日使用时长、会话时长、总启动次数、上次使用时间）。底部终端抽屉实时显示 ComfyUI 进程日志。

工作区还能检测当前工作流的问题 — 如果缺少自定义节点或模型，顶部会出现通知栏，一键安装节点、下载模型或重启 ComfyUI。

硬件信息（系统、CPU、内存、显卡、显存、主板）一目了然。启动参数 — 端口号、GPU 模式（Auto / RTX fp16 / CPU）和自定义参数 — 通过齿轮按钮配置。

### 环境 — 部署与管理

**部署**：一键安装全新的 ComfyUI 环境，可选版本、GPU 加速方式（NVIDIA CUDA / AMD ROCm）和预装组件。

**管理**：同时管理多个 ComfyUI 安装，包括 **ComfyUI Desktop** 安装。一眼看到 Python、PyTorch、ComfyUI 版本。按标签切换 ComfyUI 内核版本，可视化切换 PyTorch/CUDA 配置，按需安装 Python 开发头文件。

完整的 **pip 依赖管理表格**支持搜索、安装、升级、切换版本、批量卸载 Python 包。还可以直接拖拽 `.txt`（requirements）或 `.whl`（wheel）文件进行安装。一键清理 pip 缓存或升级 pip 本身。

### 工作流 — 模型查找与下载

> 需要登录 ModelFinder 账号。

拖入工作流文件（JSON 或 PNG），自动扫描本地模型、识别缺失项，并从云端模型目录中匹配 **HuggingFace**、**ModelScope**、**Civitai** 等来源的下载链接。当匹配不确定时，你可以从候选列表中选择，或拒绝误匹配。

确认匹配后一键下载全部缺失模型，或将列表复制到剪贴板手动搜索。支持多个工作流文件或整文件夹批量分析。

### 插件 — 自定义节点安装与管理

浏览所有已安装的自定义节点，查看启用状态、Git 信息和依赖情况。可以切换启用/禁用、安装 Python 依赖（支持 pip 镜像：PyPI / 清华 / 阿里 / 腾讯 / 豆瓣）、打开 GitHub 仓库，或彻底删除插件。

从任意 Git URL 一键安装新的自定义节点 — ModelFinder 自动 clone 仓库并安装 Python 依赖。批量启用/禁用和批量依赖安装让大量插件管理更轻松。

### 模型 — 模型库与下载管理器

**模型库**提供所有本地模型文件的可视化浏览 — checkpoint、LoRA、VAE、ControlNet、CLIP 等 — 支持分类筛选和搜索。直接打开模型所在文件夹或删除不需要的模型。切换到**全部包**模式可查看所有 ComfyUI 安装中的模型，支持重复检测和可回收空间估算。

**下载管理器**在一处展示所有活跃和已完成的下载。活跃下载显示实时进度、速度和预估时间，支持暂停/恢复/取消。已完成的下载可打开文件夹或从列表清除。

### AI 助手

标题栏上的全局聊天面板。遇到问题时，AI 可以分析你的日志、建议修复命令、在你确认后执行，并验证修复效果。推荐提示词帮助你快速上手：诊断故障、检查依赖、总结修复步骤。

AI 功能由服务端管理 — 登录账号即可使用。

### 设置

- **账户**：登录/登出、查看订阅计划、积分余额和账单
- **常规**：语言（中文 / English / 跟随系统）、关闭行为、共享模型目录及目录链接
- **网络**：HuggingFace 镜像开关、Aria2 多连接下载加速器
- **AI**：代理配置、原始日志上传偏好
- **高级**：系统依赖管理器（Git、7-Zip、VC Redist）、日志查看、缓存清理、更新管理器

---

## 个性化

- **语言**：简体中文 / English / 跟随系统 — 即时切换，无需重启
- **主题**：深色 / 浅色，切换时 ComfyUI 界面同步生效
- **配色方案**：多种主题配色可选
- 采用 **Windows Fluent Design** 设计语言，现代原生体验

---

## 发布通道

| 通道 | 适合 |
|------|------|
| **Stable 稳定版** | 大多数用户 — 推荐的公开稳定版 |
| **Beta 测试版** | 想提前体验新功能、能接受偶尔粗糙的用户 |

Beta 版本在同一仓库发布，可能包含未定型的功能或临时性回归。

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

支持。进入环境页面，点击「添加目录」，选择已有的 ComfyUI 便携包目录即可，原有文件不会被修改。
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
<summary><b>AI 助手怎么用？</b></summary>

登录 ModelFinder 账号后，点击标题栏的 AI 助手按钮即可打开聊天面板。ComfyUI 出现问题时，AI 会分析日志、生成修复命令，确认后执行。你也可以在聊天界面直接提问。
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
