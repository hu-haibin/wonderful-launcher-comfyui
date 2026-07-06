🌐 [English](README.md) | **简体中文**

<div align="center">

# Wonderful Launcher for ComfyUI（Windows 版）

### 帮你把下载来的 ComfyUI 工作流真正跑起来。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/wonderful-launcher-comfyui?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
[![产品下载量](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2Fwonderful-launcher-comfyui%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=%E4%BA%A7%E5%93%81%E4%B8%8B%E8%BD%BD%E9%87%8F)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)

[**下载安装包**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.3) · [**更新说明**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.3) · [**官网**](https://wonderfullauncher.com/) · [**文档**](https://wonderfullauncher.com/docs) · [**反馈问题**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## 下载

- **普通用户推荐**：[Wonderful Launcher 2.1.3 Setup 安装包](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.3)
- **更新说明**：[Wonderful Launcher 2.1.3](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.3)

打开安装包 release，下载 `WonderfulLauncher-Setup-v2.1.3.exe`。

> [!WARNING]
> 不要下载 GitHub 自动生成的 `Source code.zip` 或 `Source code.tar.gz`。那些是源码压缩包，不是可以直接运行的 Windows 桌面安装包。

> [!TIP]
> 正常安装路径下，公开安装包已经包含桌面运行所需组件，不需要额外安装 Microsoft .NET Desktop Runtime。

> [!IMPORTANT]
> 如果旧版本下载了更新，但重启后又打开旧应用，请直接下载并运行上面的最新 **Setup 安装包**。这是官方修复路径：会保留启动器数据，把旧 `ModelFinder` / `Wonderful Launcher` 数据收敛到 `WonderfulLauncher`，清理旧更新状态，并启动最新版 Wonderful Launcher。你不需要手动删除旧目录。

<p align="center">
  <img src="assets/screenshots/home-launch-surface.png" alt="Wonderful Launcher 首页" width="84%" />
</p>

---

## 为什么需要它

拿到一个 ComfyUI 工作流，并不等于它能在你的电脑上跑起来。

网上下载的工作流，可能缺模型、缺自定义节点、Python 依赖版本冲突、PyTorch 环境损坏，或者某个模型必须放到特定目录。很多新手并不是不会创作，而是卡在“怎么让这个工作流先跑起来”。

Wonderful Launcher 的目标，是把这些分散的维护动作收进一个 Windows 桌面工作流：

- 接管已有的 ComfyUI Desktop 或便携版 ComfyUI
- 从零部署一个干净的 ComfyUI 包
- 在同一个应用里启动 ComfyUI 并查看启动日志
- 查找工作流缺失的模型，并放到正确目录
- 安装缺失的自定义节点和插件依赖
- 对确定性的启动失败使用启动器原生修复任务，Agent 保持在受控诊断边界内
- 把图片历史、模型管理、运行环境和启动参数放在手边

它不是要替代 ComfyUI，而是让本地 ComfyUI 更容易维持在“可运行”的状态。

---

## 它能解决什么

| 你遇到的问题 | Wonderful Launcher 能帮你做什么 |
|--------------|--------------------------------|
| 已经安装了 ComfyUI Desktop 或便携包 | 导入并在一个桌面界面里管理。 |
| 想重新装一个干净的 ComfyUI | 选择磁盘、运行包，下载、解压并启动。 |
| ComfyUI 启动失败 | 查看日志，确认启动器原生修复任务，安装 core requirements 和 PyTorch，再重启验证。 |
| 工作流提示缺模型 | 查找可能的模型下载入口，复制链接，或直接下载到正确目录。 |
| 模型已经自己下载好了 | 把模型拖进应用，让启动器根据工作流和模型类型放到合适位置。 |
| 工作流缺节点 | 安装缺失节点和依赖，不用手动翻目录。 |
| 插件安装了但导入失败 | 结合日志、任务终端证据和受控诊断排查依赖冲突，并通过重启验证是否修复。 |
| 想生成和复用图片 | 使用图片工作区、历史记录、参考图和 Photoshop 发送功能。 |

---

## 2.1.3 更新了什么

发布于 2026 年 7 月 6 日。[查看完整 GitHub Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.3)。

这个版本是一个桌面端小更新，改善浅色主题下更新提示按钮的可见性。

- **更新提示按钮更清楚**：更新准备完成后的 toast 主按钮改用强调色背景，不再像灰掉的不可点击按钮。
- **减少更新时的误解**：重启更新操作会看起来像可用操作，而不是禁用状态。
- **补丁版打包**：桌面端版本信息和安装包资产更新到 2.1.3。

---

## 快速教程

### 1. 安装 Wonderful Launcher

1. 打开 [安装包下载 release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.3)。
2. 下载 `WonderfulLauncher-Setup-v2.1.3.exe`。
3. 运行安装包并打开 Wonderful Launcher。

这个仓库是公开下载页和教程页，不是桌面应用的公开源码镜像。

### 2. 导入已有 ComfyUI

如果你已经有 ComfyUI Desktop、便携版 ComfyUI，或者其他本地 ComfyUI 文件夹，可以直接导入。

1. 打开 Wonderful Launcher。
2. 选择 **导入 ComfyUI**。
3. 选择包含 `main.py` 的目录，或包含 `ComfyUI` 子文件夹的便携包上层目录。
4. 在首页启动 ComfyUI，并观察启动日志。

不要误选 `models`、`custom_nodes`、`output`、`python_embeded`，也不要选择只放工作流文件的目录。

### 3. 从零部署一个新的 ComfyUI

如果你想要一个干净环境，而不是继续修老环境，可以从零部署。

1. 打开 ComfyUI 设置。
2. 进入部署页面。
3. 选择安装磁盘和适合显卡的运行包。
4. 开始部署，等待下载和解压完成。
5. 回到首页启动新的 ComfyUI 包。

如果你习惯使用外部下载工具，也可以先自己下载压缩包，解压后再导入。

### 4. 跑一个下载来的工作流

如果工作流打开后出现红框、缺节点或缺模型，这不是你一个人的问题，而是 ComfyUI 日常维护的一部分。很多共享工作流都依赖特定模型、自定义节点和 Python 包。

Wonderful Launcher 围绕这个循环设计：

1. 打开或导入工作流
2. 检查缺失模型或节点
3. 安装或放置缺失内容
4. 重启或重新运行 ComfyUI
5. 验证工作流是否可以正常出图

### 5. 修复启动失败

ComfyUI 启动失败，可能是 PyTorch 缺失、Python 依赖损坏、插件改坏了环境，或者运行包被移动。

先看启动日志和运行环境页面。如果原因不明显，可以打开 Agent 面板。Agent 会读取相关状态，解释可能原因，并提出受支持的修复动作。涉及修复的动作需要你授权。

### 6. 处理缺失模型

模型文件通常很大，而且应该放在哪个目录并不总是直观。一个工作流可能需要 checkpoint、LoRA、VAE、ControlNet、diffusion models、text encoders 等不同模型。

Wonderful Launcher 可以帮你：

- 从工作流里识别缺失模型名称
- 在有下载入口时复制或打开链接
- 直接下载到预期目录
- 把已经下载好的模型文件拖进应用，并放到合适位置

### 7. 处理缺失节点和插件错误

ComfyUI 工作流经常依赖第三方自定义节点。安装节点时还可能安装 Python 依赖，而这些依赖又可能和当前环境冲突。

Wonderful Launcher 可以帮你安装缺失节点、运行依赖安装、重新打开任务终端，并通过日志验证节点是否真的注册成功。如果插件导入失败，Agent 可以辅助分析错误并提出受支持的修复步骤。

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

## 更新记录

GitHub Releases 页面只保留最新公开安装包，让新用户只有一个下载选择。

旧版本 tag 会保留作为项目历史归档，但不再作为普通下载入口。除非维护者明确让你使用某个旧版本，否则请下载最新版。

- [最新版本](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
- [Wonderful Launcher 2.1.3 更新说明](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.3)
- [Wonderful Launcher 2.1.3 Setup 安装包](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.3)

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

## 仓库用途

这个仓库是 Wonderful Launcher 的公开发版主页，用于：

- 发布 Windows 安装包
- 查看 release notes
- 展示功能截图
- 收集公开版本的问题反馈

它不是桌面应用的公开源码仓。

ComfyUI 是独立的开源项目：

- ComfyUI: https://github.com/comfyanonymous/ComfyUI

---

<div align="center">

**Wonderful Launcher** 帮你在 Windows 上维持一个更容易跑通工作流的本地 ComfyUI 环境。

</div>
