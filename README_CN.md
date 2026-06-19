🌐 [English](README.md) | **简体中文**

<div align="center">

# ModelFinder for ComfyUI（Windows 版）

### 一个把 ComfyUI 安装、启动、修复和使用收进同一个 Windows 桌面应用里的控制中心。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![产品下载量](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=%E4%BA%A7%E5%93%81%E4%B8%8B%E8%BD%BD%E9%87%8F)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**下载最新安装包**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**官网**](https://wonderfullauncher.com/) · [**文档**](https://wonderfullauncher.com/docs) · [**故障排查**](https://wonderfullauncher.com/troubleshooting) · [**当前版本**](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.31) · [**反馈问题**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

</div>

---

## 下载建议

- **普通用户推荐**：[ModelFinder 2.0.31](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.31)
- **公开稳定回退版本**：[ModelFinder 2.0.26](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.26)

这个发版仓以后尽量只保留当前安全下载路径。过渡期版本或回归较多的版本，在被更稳定的新安装包替代后，可以从 Releases 页面下架，避免继续误导用户。

<p align="center">
  <img src="assets/screenshots/home-launch-surface.png" alt="ModelFinder 首页" width="84%" />
</p>

---

## ModelFinder 为什么存在

ComfyUI 在 Windows 上经常会变成一组分散的维护动作：Python、PyTorch、自定义节点、缺失模型、启动日志、下载任务和修复步骤都散在不同地方。

ModelFinder 的目标就是把这些事情收回到一个桌面工作流里，让你可以：

- 部署新的 ComfyUI 环境，或者接管已有环境
- 不用再找脚本就能启动、停止和检查运行时
- 在一个应用里管理自定义节点和依赖安装
- 更快定位工作流缺失的模型或节点
- 生图、复用历史结果、把参考图放在手边
- 用带审批的 AI 助手辅助诊断和执行受支持的修复步骤

---

## 核心场景

| 场景 | 你能得到什么 |
|------|--------------|
| **安装或导入 ComfyUI** | 接管已有安装，或部署新环境，尽量减少“选错根目录”的问题。 |
| **启动和检查运行时** | 启动 ComfyUI，打开内置工作区，并在同一个应用里看启动日志。 |
| **管理自定义节点** | 安装插件、安装依赖、删除损坏节点，并验证某个节点是否真正可用。 |
| **查缺失工作流资源** | 扫描工作流里的缺失模型或节点，并跳到最接近的修复或下载路径。 |
| **使用图片工作区** | 生成图片、复用历史结果、把历史图拖回输入区，并发送图片到 Photoshop。 |
| **让 AI 助手辅助处理** | 让助手解释启动失败、依赖错误和缺失节点问题，并在你授权后执行受支持的动作。 |

---

## 2.0.31 更新了什么

发布于 2026 年 6 月 19 日。[查看完整 GitHub Release](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.31)。

这个版本重点是把 Avalonia 图片工作区从“能用”拉回到“适合持续创作”。

- **支持并行追加生图轮次**：前一轮还在排队或生成时，你可以继续编辑并发送下一轮图片请求。
- **参考图和历史图区交互更一致**：左侧 `input` 栏现在更接近右侧历史栏，支持查看、拖回和上下文操作。
- **拖拽回填恢复**：更大的参考图区命中范围回来了，把图片拖回输入区的体验更接近旧版本。
- **生成占位更清楚**：状态附着在卡片本身，复用工作流模板的描边流光动画，不再靠漂浮的全局横条提示。
- **修掉最近回归**：回车发送和“再生成一张”都修回来了，不再延续前几个 Avalonia 版本的问题。

---

## 功能截图

<p align="center">
  <img src="assets/screenshots/feature-plugin-manager.png" alt="插件管理" width="32%" />
  <img src="assets/screenshots/feature-model-manager.png" alt="模型管理" width="32%" />
  <img src="assets/screenshots/feature-environment.png" alt="环境管理" width="32%" />
</p>

<p align="center">
  <img src="assets/screenshots/feature-image-workspace.png" alt="图片工作区" width="32%" />
  <img src="assets/screenshots/feature-image-photoshop-send.png" alt="发送到 Photoshop" width="32%" />
  <img src="assets/screenshots/home-live-startup-logs.png" alt="启动日志与启动状态" width="32%" />
</p>

---

## 快速开始

### 安装

1. 打开 [最新 GitHub Release](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)。
2. 下载 `ModelFinderLauncher-Setup-v*.exe`。
3. 运行安装包并启动 ModelFinder。

> [!WARNING]
> 请下载 release 资产里的 **Setup 安装包**。不要下载 GitHub 自动生成的 `Source code.zip` 或 `Source code.tar.gz`，那是源码压缩包，不能直接运行。

> [!TIP]
> 公开安装包对正常桌面运行时是 self-contained 的，不需要额外安装 Microsoft .NET Desktop Runtime。

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

## 发版页策略

- README 首页用于呈现当前推荐下载路径，不再承担保存所有历史说明的职责。
- GitHub Releases 页面应尽量保持简洁，只保留最新版本和少量明确保留的回退版本。
- 为了工程追踪可以保留 tag，但有问题或噪音较大的 release 条目可以从公开发布页移除。

---

## 常见问题

<details>
<summary><b>需要先安装 Python 吗？</b></summary>

不需要。正常路径下，ModelFinder 会帮你管理 ComfyUI 的 Python 环境。

</details>

<details>
<summary><b>可以接管我现有的 ComfyUI 吗？</b></summary>

可以。使用 **导入 ComfyUI**，选择包含 `main.py` 的目录，或包含 `ComfyUI` 子文件夹的便携包上层目录即可。

</details>

<details>
<summary><b>支持自定义节点吗？</b></summary>

支持。你可以安装自定义节点、运行依赖安装、管理插件状态，也可以让 AI 助手辅助执行受支持的修复步骤。

</details>

<details>
<summary><b>AI 助手会自动执行动作吗？</b></summary>

涉及写入或修复的动作，仍然需要你的授权。AI 助手主要负责诊断和调用受支持的启动器工具。

</details>

<details>
<summary><b>支持 macOS 或 Linux 吗？</b></summary>

目前不支持。这个仓库发布的是 Windows 桌面构建。

</details>

---

## 关于这个仓库

这个仓库是 ModelFinder 的公开发版主页，主要用于：

- 发布 Windows 安装包
- 展示当前版本更新说明
- 放 release 截图
- 承担公开版本的问题反馈

ModelFinder 本身是围绕 ComfyUI 生态构建的闭源桌面产品。

ComfyUI 是独立的开源项目：

- ComfyUI: https://github.com/comfyanonymous/ComfyUI

---

<div align="center">

**ModelFinder**：一个把 ComfyUI 日常维护收进桌面工作流里的 Windows 控制中心。

</div>
