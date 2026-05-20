🌐 [English](README.md) | **简体中文**

<div align="center">

# ModelFinder for ComfyUI（Windows 版）

### 一个用于安装、启动、修复和管理 ComfyUI 的桌面控制中心。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/wonderful-launcher-comfyui?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
[![产品下载量](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2Fwonderful-launcher-comfyui%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=%E4%BA%A7%E5%93%81%E4%B8%8B%E8%BD%BD%E9%87%8F)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)

[**下载最新安装包**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest) · [**2.0.15 更新说明**](release-notes/2.0.15.zh-CN.md) · [**所有版本**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases) · [**反馈问题**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## 为什么需要 ModelFinder

ComfyUI 很强，但 Windows 上的安装和维护经常很分散：Python 版本、PyTorch 构建、自定义节点、插件依赖、工作流资源、模型下载和启动日志都在不同地方。

ModelFinder 把这些事情集中到一个桌面应用里，让普通 ComfyUI 用户可以：

- 部署或导入 ComfyUI 环境
- 启动、停止和检查当前运行时
- 安装自定义节点和插件依赖
- 扫描工作流里的缺失模型或缺失节点
- 管理本地模型文件和下载任务
- 基于真实启动器证据诊断启动失败
- 让 AI 助手解释问题，并在授权后执行修复步骤

<p align="center">
  <img src="assets/screenshots/2.0.15-home.png" alt="ModelFinder 2.0.15 首页" width="82%" />
</p>

---

## 2.0.15 更新了什么

发布于 2026 年 5 月 21 日。[查看完整 2.0.15 更新说明](release-notes/2.0.15.zh-CN.md)。

这个版本重点提升 AI 修复流程的可信度。

| 方向 | 变化 |
|------|------|
| **缺失节点修复** | AI 助手会把安装动作绑定到同一次缺失节点检测快照。即使安装前需要停止或重启 ComfyUI，也不会丢掉原来的计划。 |
| **修复过程可见** | 工具结果会包含是否已尝试、原因、snapshot id、终端 job id、是否可重试和推荐下一步。 |
| **任务隔离** | Agent 写操作和用户手动写操作会统一协调，避免插件安装、运行时控制和环境切换互相覆盖。 |
| **界面更少打扰** | 快速环境读取保持静默，耗时较长时才显示延迟的行内状态，不再闪一下。 |
| **反馈闭环** | 在允许上传时，脱敏后的 Agent 会话可以同步对话复盘、工具链、修复 timeline、任务类型和结果，用于调试与回归测试。 |

<p align="center">
  <img src="assets/screenshots/2.0.15-agent-panel.png" alt="ModelFinder 2.0.15 AI 助手面板" width="82%" />
</p>

---

## 核心使用场景

| 场景 | ModelFinder 提供什么 |
|------|----------------------|
| **安装或导入 ComfyUI** | 部署新环境，或接管已有 ComfyUI 文件夹，减少选错目录的概率。 |
| **启动和检查运行时** | 在首页启动/停止 ComfyUI，查看实时日志，打开内置工作区，确认运行状态。 |
| **修复自定义节点** | 检测缺失节点，必要时安装 ComfyUI-Manager，创建终端任务，重启并验证节点注册。 |
| **管理插件** | 从 Git URL 安装自定义节点，启用/禁用插件，删除插件，安装依赖。 |
| **查找缺失模型** | 拖入工作流后检测缺失模型引用，并从支持的目录中匹配候选下载项。 |
| **管理下载** | 在启动器里排队、跟踪、暂停、恢复和查看模型下载任务。 |
| **使用 AI 辅助** | 让 AI 助手诊断问题，授权修复工具，并把多步修复证据保留在同一会话里。 |

---

## 功能图集

<p align="center">
  <img src="assets/screenshots/feature-environment.png" alt="ModelFinder 运行环境页面" width="32%" />
  <img src="assets/screenshots/feature-plugin-manager.png" alt="ModelFinder 插件管理页面" width="32%" />
  <img src="assets/screenshots/feature-model-finder.png" alt="ModelFinder 模型查找页面" width="32%" />
</p>

<p align="center">
  <img src="assets/screenshots/feature-model-manager.png" alt="ModelFinder 模型管理页面" width="32%" />
  <img src="assets/screenshots/feature-download-center.png" alt="ModelFinder 下载中心页面" width="32%" />
  <img src="assets/screenshots/feature-image-workspace.png" alt="ModelFinder 图片工作区" width="32%" />
</p>

---

## AI 助手边界

AI 助手集成在桌面应用里，但它不是一个不受限制的命令行。

它可以：

- 读取启动器收集到的日志和当前选中环境状态
- 解释启动失败、依赖错误和插件失败
- 检查缺失节点和缺失模型证据
- 在授权后调用受支持的启动器工具
- 为耗时安装创建任务终端
- 在同一会话里继续多步修复
- 在开启个性化后使用本地偏好和项目提示

它不会：

- 绕过写入或修复动作的用户授权
- 改变计费或积分规则
- 默认把本地个性化记忆作为云端同步内容
- 把完整终端日志、system prompt、工作流文件、token 或原始环境 dump 作为反馈数据发送

AI 功能需要登录账号，并按积分使用。当前计费规则以官方服务为准，不以这个 release 仓库为准。

---

## 快速开始

### 安装

1. 打开 [最新 GitHub Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)。
2. 下载 `ModelFinderLauncher-Setup-v*.exe`。
3. 运行安装包并打开 ModelFinder。

> [!WARNING]
> 请下载 release 资产里的 **Setup 安装包**。不要下载 GitHub 自动生成的 `Source code.zip` 或 `Source code.tar.gz`，那是源码压缩包，不能直接运行。

> [!TIP]
> 正常安装包对桌面应用运行时是 self-contained，不需要你额外安装 Microsoft .NET Desktop Runtime。

### 导入已有 ComfyUI

1. 打开 ModelFinder，停留在首页。
2. 点击 **导入 ComfyUI**。
3. 选择包含 `main.py` 的目录，或包含 `ComfyUI` 子文件夹的便携包上层目录。
4. 在首页启动 ComfyUI。

这些目录不要误选：

- `models`
- `custom_nodes`
- `output`
- `python_embeded`
- 只有工作流文件的目录

---

## 当前产品边界

- **平台**：Windows 10 / 11
- **发布形态**：公开 Windows 安装包
- **云端能力**：AI 助手和部分工作流匹配能力需要登录与服务端能力
- **本地数据**：启动器配置、日志、包状态和可选个性化数据默认留在本机，除非某个功能明确向服务端发起请求
- **预发布版本**：如果有 beta 构建，会在 GitHub Releases 中单独标记

---

## 常见问题

<details>
<summary><b>需要先安装 Python 吗？</b></summary>

不需要。标准使用场景下，ModelFinder 会帮你管理 ComfyUI 的 Python 环境。

</details>

<details>
<summary><b>可以接管我现有的 ComfyUI 吗？</b></summary>

可以。使用 **导入 ComfyUI**，选择包含 `main.py` 的目录，或包含 `ComfyUI` 子文件夹的便携包上层目录即可。

</details>

<details>
<summary><b>支持自定义节点吗？</b></summary>

支持。你可以从 Git URL 安装自定义节点，管理依赖，启用或禁用插件，也可以使用 Agent 辅助的缺失节点修复。

</details>

<details>
<summary><b>AI 助手会自动执行修复吗？</b></summary>

涉及写入或修复的动作，仍然需要授权后才会执行。

</details>

<details>
<summary><b>支持 macOS 或 Linux 吗？</b></summary>

目前不支持。这个 release 仓库发布的是 Windows 构建。

</details>

---

## 关于这个仓库

这个仓库用于：

- 发布 Windows 安装包
- 保存 [版本更新说明](release-notes/)
- 承担公开版本的问题反馈

ModelFinder 本身是围绕 ComfyUI 生态构建的闭源桌面产品。

ComfyUI 是独立的开源项目：

- ComfyUI: https://github.com/comfyanonymous/ComfyUI

---

<div align="center">

**ModelFinder**：一个面向 ComfyUI 环境的 Windows 控制中心。

</div>
