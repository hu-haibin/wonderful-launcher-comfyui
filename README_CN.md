🌐 [English](README.md) | **简体中文**

<div align="center">

# ModelFinder for ComfyUI（Windows 版）

### 一个把 ComfyUI 安装、启动、修复和管理收进同一个桌面应用里的控制中心。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![产品下载量](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=%E4%BA%A7%E5%93%81%E4%B8%8B%E8%BD%BD%E9%87%8F)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**下载最新安装包**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**官网**](https://wonderfullauncher.com/) · [**文档**](https://wonderfullauncher.com/docs) · [**故障排查**](https://wonderfullauncher.com/troubleshooting) · [**2.0.30 更新说明**](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.30) · [**全部 Releases**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**反馈问题**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

</div>

---

## 用户为什么会用 ModelFinder

ComfyUI 很强，但 Windows 上的日常维护往往很碎：Python、PyTorch、自定义节点、缺失模型、启动日志、下载任务和修复步骤经常散在不同地方。

ModelFinder 的目标就是把这些事情收回到一个桌面工作流里，让你可以：

- 部署新的 ComfyUI 环境，或者接管已有环境
- 不用找批处理文件就能启动、停止和检查运行时
- 在启动器里安装自定义节点和依赖
- 更快定位工作流缺失的模型或节点
- 在一个地方管理下载、包状态和环境信息
- 用带审批的 AI 助手解释问题并执行受支持的修复步骤

<p align="center">
  <img src="assets/screenshots/2.0.15-home.png" alt="ModelFinder 首页" width="84%" />
</p>

---

## 现在能做什么

| 场景 | ModelFinder 能帮你做什么 |
|------|--------------------------|
| **安装或导入 ComfyUI** | 部署新环境，或接管已有 ComfyUI 文件夹，尽量减少“选错根目录”的问题。 |
| **启动和检查运行时** | 启动 ComfyUI，打开内置工作区，并在同一个应用里看实时启动日志。 |
| **管理自定义节点** | 安装插件、安装依赖、删除损坏节点，并验证某个节点到底有没有真正可用。 |
| **查缺失工作流资源** | 扫描工作流里的缺失节点或模型，并跳到最接近的修复/下载路径。 |
| **使用图片工作区** | 生成图片、复用历史结果、发送到 Photoshop，并把历史保留在启动器里。 |
| **让 AI 助手辅助修复** | 让助手解释启动失败、依赖错误和缺失节点问题，并在你授权后执行受支持的修复动作。 |

---

## 2.0.30 更新了什么

发布于 2026 年 6 月 18 日。[查看完整 GitHub Release](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.30)。

这是一个安装器热修版本，用来把早期 Avalonia 安装包留下的路径分叉重新收敛回唯一的公开产品身份：ModelFinder。

- **只保留一个用户可见身份**：升级后会清理旧的 `ModelFinder Avalonia` 桌面快捷方式、开始菜单入口和卸载项。
- **旧 Avalonia 路径原地修复**：如果机器上只有旧 Avalonia 安装路径，新安装器会优先装回原路径，避免出现第二个可见 ModelFinder。
- **后续自动更新更稳**：静默调用安装器更新时，会显式传入当前安装目录，避免未来版本再跑到另一条路径。
- **这个版本不做品牌迁移**：`Avalonia` 仍然只是内部框架名。未来 Wonderful Launcher 改名和数据迁移会用单独的安装器引导处理。

---

## 功能截图

<p align="center">
  <img src="assets/screenshots/feature-home.png" alt="ModelFinder 首页" width="32%" />
  <img src="assets/screenshots/feature-plugin-manager.png" alt="插件管理" width="32%" />
  <img src="assets/screenshots/feature-model-finder.png" alt="模型查找" width="32%" />
</p>

<p align="center">
  <img src="assets/screenshots/feature-environment.png" alt="环境管理" width="32%" />
  <img src="assets/screenshots/feature-image-workspace.png" alt="图片工作区" width="32%" />
  <img src="assets/screenshots/feature-image-photoshop-send.png" alt="发送到 Photoshop" width="32%" />
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
> 公开安装包对正常桌面运行时是 self-contained 的，不需要你额外安装 Microsoft .NET Desktop Runtime。

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

## 最近版本

对普通用户来说，**最新 release 是唯一推荐下载的版本**。旧版本在被新的稳定安装包替代后，可能会从 Releases 页面隐藏或下架。

| 版本 | 日期 | 摘要 |
|------|------|------|
| **2.0.30** | 2026 年 6 月 18 日 | 安装器热修版本，修复旧 Avalonia 安装路径分叉，并清理 `ModelFinder Avalonia` 用户可见入口。 |
| **2.0.29** | 2026 年 6 月 17 日 | Avalonia 工作流体验打磨版，重点是更新进度可见、模板可点击导入、预览动图支持和部署页浅色主题选中态优化。 |
| **2.0.28** | 2026 年 6 月 17 日 | Avalonia 体验打磨版，重点是 AI 助手入口、日志诊断防漂移、审批简化和模型查找登录门禁。 |
| **2.0.27** | 2026 年 6 月 16 日 | Avalonia 公开版，重点是 WinUI 到 Avalonia 的升级连续性、图片积分流程和工作区修复体验。 |
| **2.0.26** | 2026 年 6 月 9 日 | WinUI 可靠性版本，重点是 Agent 修复链、图片工作区打磨和支持可观测性。 |

更完整的版本说明请看 [GitHub Releases 页面](https://github.com/hu-haibin/ModelFinder-Releases/releases)。

---

## 常见问题

<details>
<summary><b>需要先安装 Python 吗？</b></summary>

不需要。正常使用路径下，ModelFinder 会帮你管理 ComfyUI 的 Python 环境。

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
<summary><b>AI 助手会自动执行修复吗？</b></summary>

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
