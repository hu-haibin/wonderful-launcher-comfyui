🌐 [English](README.md) | **简体中文**

<div align="center">

# ModelFinder for ComfyUI（Windows 版）

### 一个面向 Windows 的 ComfyUI 启动、管理、诊断与修复工具。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/wonderful-launcher-comfyui?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
[![产品下载量](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2Fwonderful-launcher-comfyui%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=%E4%BA%A7%E5%93%81%E4%B8%8B%E8%BD%BD%E9%87%8F)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)

[**下载**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest) · [**2.0.13 更新说明**](release-notes/2.0.13.zh-CN.md) · [**所有版本**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases) · [**反馈问题**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## ModelFinder 是什么

ModelFinder 是一个面向 ComfyUI 生态的 Windows 桌面工具。

它主要解决这些经常让人头疼的事情：

- 部署新的 ComfyUI 环境
- 同时管理多个 ComfyUI 安装
- 检查 Python、PyTorch 和依赖状态
- 安装自定义节点及其依赖
- 扫描工作流里的缺失资源
- 从支持的来源下载模型
- 诊断启动失败和环境报错

目标很直接：少折腾环境，多跑工作流。

---

## 2.0.13 更新了什么

发布于 2026 年 5 月 19 日。[查看完整 2.0.13 更新说明](release-notes/2.0.13.zh-CN.md)。

- **工具页只保留已接通入口**：移除了“批量分析”“批量下载”“AI 自动修复”三个占位卡片，等流程真正可用后再展示。
- **部署和导入路径更清楚**：检测到已有 ComfyUI 实例时仍保留导入入口，版本选择相关回退文案也已本地化。
- **窗口和导航更稳**：标题栏显示应用版本，主题色可在当前界面直接刷新，底栏按钮 hover 尺寸更一致。
- **Release 加载更轻**：GitHub release 元数据会被缓存，并通过镜像回退减少重复 API 请求。

<p align="center">
  <img src="assets/screenshots/feature-home.png" alt="ModelFinder 首页启动界面" width="80%" />
</p>

---

## 近期产品亮点

- **图片生成实时进度**：图片生成过程中会显示排队、状态和进度反馈，不再只让用户干等。
- **更强的 AI 诊断**：AI 助手会结合启动器日志、启动失败信息、任务终端证据和当前环境状态，再给出修复建议。
- **本地个性化控制**：开启后，本地偏好和项目提示可以让回复更贴近使用习惯，但不会改变权限、计费或安全规则。
- **更稳的更新判断**：更新检查会避免在当前安装版本已经是最新或更新时，出现误导性的降级/迁移提示。

---

## 功能图集

下面这组截图展示的是当前 WinUI 公共构建里最核心的几个主界面。

<p align="center">
  <img src="assets/screenshots/feature-home.png" alt="ModelFinder 首页启动界面" width="32%" />
  <img src="assets/screenshots/feature-environment.png" alt="ModelFinder 运行环境页面" width="32%" />
  <img src="assets/screenshots/feature-plugin-manager.png" alt="ModelFinder 插件管理页面" width="32%" />
</p>

<p align="center">
  <img src="assets/screenshots/feature-model-manager.png" alt="ModelFinder 模型管理页面" width="32%" />
  <img src="assets/screenshots/feature-model-finder.png" alt="ModelFinder 模型查找页面" width="32%" />
  <img src="assets/screenshots/feature-download-center.png" alt="ModelFinder 下载中心页面" width="32%" />
</p>

- **首页启动面板**：在主界面选择环境并启动 ComfyUI。
- **运行环境**：集中查看 Python、PyTorch、ComfyUI、磁盘占用和已安装包。
- **插件管理**：在独立页面里启用、禁用、安装和删除自定义节点。
- **模型管理**：浏览当前环境中的 checkpoint 和其他本地模型文件。
- **模型查找**：拖入工作流后先扫描缺失模型，再决定如何补齐。
- **下载中心**：在启动器内跟踪排队中和已完成的下载任务。

---

## 核心能力

| 模块 | 能做什么 |
|------|----------|
| **首页** | 启动/停止 ComfyUI，查看实时日志，打开内置工作区，查看基础运行状态 |
| **环境** | 部署 ComfyUI，管理多个安装，切换 ComfyUI / PyTorch 版本，安装 `.txt` 与 `.whl` 依赖 |
| **工作流** | 分析工作流文件，识别缺失模型，并从支持的目录中匹配候选下载项 |
| **插件** | 从 Git URL 安装自定义节点，管理插件依赖，批量启用或禁用插件 |
| **模型** | 浏览本地模型库，检测跨包重复文件，管理下载任务 |
| **图片** | 通过提示词生成图片，查看实时状态/进度，检查生成结果，并把结果直接发送到 Photoshop |
| **AI 助手** | 读取启动器证据、解释报错，并在授权后执行支持的修复动作 |
| **下载** | 排队、跟踪、暂停、恢复和管理模型下载 |

---

## AI 助手

AI 助手集成在桌面端聊天面板里。

它目前可以：

- 读取启动器收集到的日志和环境状态
- 读取启动失败信息、任务终端输出和当前选中环境上下文
- 解释启动失败、依赖报错、插件安装失败等问题
- 给出修复建议
- 在你授权后调用启动器内置工具执行修复
- 在同一会话里继续多步修复流程
- 在开启个性化后使用本地偏好和项目提示

需要注意：

- AI 功能需要登录账号
- 使用按积分计费，由服务端统一管理
- 当前计费和价格规则以官方网站为准，不以本发版仓 README 为准
- 本地个性化不会绕过授权、提升工具权限或改变计费规则
- 本地个性化记忆不会作为默认云端同步内容

---

## 快速开始

### 安装 ModelFinder

1. 打开 [Releases](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
2. 下载最新的 **Setup 安装包**
3. 运行安装包并打开 ModelFinder

> [!WARNING]
> 请下载 release 资产里的 **Setup 安装包**。不要下载 GitHub 自动生成的 `Source code.zip` 或 `Source code.tar.gz`，那是源码压缩包，不能直接运行。

> [!TIP]
> ComfyUI 的 Python 环境由 ModelFinder 管理。Setup 安装包对桌面应用运行时是 self-contained，正常安装不需要你单独安装 Microsoft .NET Desktop Runtime。

<p align="center">
  <img src="assets/screenshots/home-live-startup-logs.png" alt="ModelFinder 首次打开后的首页，包含 导入 ComfyUI 和 部署 ComfyUI 按钮" width="80%" />
</p>

### 导入已有 ComfyUI

1. 打开 ModelFinder，停留在首页
2. 点击 **导入 ComfyUI**
3. 选择你现有的 ComfyUI 目录
4. 导入成功后，在首页点击 **启动**

最稳的选择方式是：

- 直接选择 **包含 `main.py`** 的那个目录
- 如果你用的是便携包，也可以选择它的上层目录，只要里面有一个 `ComfyUI` 子文件夹

这些目录不要误选：

- `models`
- `custom_nodes`
- `output`
- `python_embeded`
- 只有工作流文件的目录

### 已有环境

ModelFinder 可以管理这些场景：

- 已存在的 ComfyUI 便携包目录
- 多个并行存在的 ComfyUI 环境
- 通过 `Documents\\ComfyUI` 导入的 ComfyUI Desktop 环境

它的定位是管理和诊断这些环境，不是无提示地覆盖你的原有文件。

### 常见的导入与启动混淆

- **选错目录**：如果 ModelFinder 提示找不到 `main.py`，说明你选错了目录，重新选择真正的 ComfyUI 根目录即可。
- **导入成功，但启动还是失败**：请先看**应用窗口最上方的标题栏**。如果标题栏里已经显示出类似 `...\\ComfyUI_windows_portable\\ComfyUI` 这样的路径，说明 ModelFinder 已经找到你的 ComfyUI 运行时了。这种情况通常**不是目录选错**，而是启动环境本身有问题。接着请看首页下方的日志区域，确认是否有 `dll`、`torch`、`roc_sdk` 等依赖报错。
- **还是不确定该选哪个目录**：优先选择包含 `main.py` 的目录，或者包含 `ComfyUI` 子文件夹的便携包上层目录。

---

## 当前产品边界

- **平台**：Windows 10 / 11
- **发布形态**：这个仓库发布的是公开 Windows 构建
- **预发布版本**：如果未来有 beta / prerelease，会在 GitHub Releases 中明确标记
- **云端能力**：AI 助手和部分工作流匹配能力依赖登录与服务端能力
- **本地数据**：启动器配置、日志、包状态和可选个性化数据默认留在本机，除非某个功能明确向服务端发起请求

---

## 常见问题

<details>
<summary><b>需要先安装 Python 吗？</b></summary>

不需要。标准使用场景下，ModelFinder 会帮你管理 ComfyUI 的 Python 环境。

</details>

<details>
<summary><b>可以接管我现有的 ComfyUI 吗？</b></summary>

可以。你只需要在首页点击 **导入 ComfyUI**，选择包含 `main.py` 的目录，或包含 `ComfyUI` 子文件夹的便携包上层目录，就可以把它纳入 ModelFinder 管理。

</details>

<details>
<summary><b>支持自定义节点吗？</b></summary>

支持。你可以从 Git URL 安装自定义节点，并在应用内管理它们的 Python 依赖。

</details>

<details>
<summary><b>AI 助手会自动执行修复吗？</b></summary>

对涉及写入、安装、修复的动作，仍然需要授权后才会执行。

</details>

<details>
<summary><b>支持 macOS 或 Linux 吗？</b></summary>

目前不支持。本发版仓只发布 Windows 版本。

</details>

---

## 关于这个仓库

这个仓库主要用于：

- 发布 Windows 安装包
- 版本更新说明与 release 历史（见 [release-notes/](release-notes/)）
- 承担公开版本的问题反馈

ModelFinder 本身是围绕 ComfyUI 生态构建的闭源桌面产品。

ComfyUI 是独立的开源项目：

- ComfyUI: https://github.com/comfyanonymous/ComfyUI

---

<div align="center">

**ModelFinder** —— 一个面向 ComfyUI 环境的 Windows 控制中心。

</div>
