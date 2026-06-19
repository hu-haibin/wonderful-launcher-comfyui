🌐 [English](README.md) | **简体中文**

<div align="center">

# Wonderful Launcher for ComfyUI（Windows 版）

### `Wonderful Launcher` 是对外品牌名，当前桌面应用本体暂时仍叫 `ModelFinder`。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/wonderful-launcher-comfyui?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
[![产品下载量](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2Fwonderful-launcher-comfyui%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=%E4%BA%A7%E5%93%81%E4%B8%8B%E8%BD%BD%E9%87%8F)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)

[**下载最新安装包**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest) · [**官网**](https://wonderfullauncher.com/) · [**文档**](https://wonderfullauncher.com/docs) · [**故障排查**](https://wonderfullauncher.com/troubleshooting) · [**当前版本**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.0.32) · [**反馈问题**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## 下载建议

- **普通用户推荐**：[Wonderful Launcher 2.0.32](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.0.32)
- **公开稳定回退版本**：[ModelFinder 2.0.31](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.0.31)

现在对外产品品牌统一按 `Wonderful Launcher` 表达，但下载后的安装包、程序窗口和部分界面在过渡期内仍可能显示当前应用名 `ModelFinder`。

<p align="center">
  <img src="assets/screenshots/home-launch-surface.png" alt="ModelFinder 首页" width="84%" />
</p>

---

## Wonderful Launcher 为什么存在

ComfyUI 在 Windows 上经常会变成一组分散的维护动作：Python、PyTorch、自定义节点、缺失模型、启动日志、下载任务和修复步骤都散在不同地方。

Wonderful Launcher 的目标，是通过当前的 ModelFinder 桌面应用，把这些事情收回到一个桌面工作流里，让你可以：

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

## 2.0.32 更新了什么

发布于 2026 年 6 月 19 日。[查看完整 GitHub Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.0.32)。

这个版本重点是把公开安装表面切到 `Wonderful Launcher`，同时保留旧 `2.0.x` 的原地升级路径，不把用户拆成两个并列安装。

- **安装包文件名更新**：公开下载的 setup 安装器现在是 `WonderfulLauncher-Setup-v2.0.32.exe`。
- **升级链路保持原地迁移**：已有 `2.0.x` 用户仍可直接升级，不会因为改名被拆成一个新的并列安装。
- **Windows 安装表面更统一**：安装器面向用户显示的产品名改为 `Wonderful Launcher`，重装时也会顺手清理旧的 `ModelFinder` 快捷方式痕迹。
- **全新安装默认目录更新**：新安装默认落在 `%LocalAppData%\\Wonderful Launcher`，但已有安装升级时仍优先沿用原路径。
- **2.0.31 的图片工作区修复继续保留**：并行生图、多轮追加、拖拽恢复、参考图/历史图复用、卡片内生成占位，这些能力都包含在本版内。

> [!NOTE]
> 这是一次过渡版改名。安装器和安装表面已经切到 `Wonderful Launcher`，但任务栏、进程名或部分系统级标识里，仍可能暂时看到 `ModelFinder` 或 `mf`。

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

1. 打开 [最新 GitHub Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)。
2. 下载 `WonderfulLauncher-Setup-v*.exe`。
3. 运行安装包并启动 Wonderful Launcher。

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
<summary><b>为什么有些 Windows 位置里还是会看到 ModelFinder 或 mf？</b></summary>

`2.0.32` 先切的是公开安装器和安装表面的品牌。为了兼容已有升级链路，这一版还保留了一部分内部标识，所以任务栏、进程相关位置里暂时仍可能显示 `ModelFinder` 或 `mf`。

</details>

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

这个仓库是 Wonderful Launcher 以及当前 ModelFinder 桌面应用的公开发版主页，主要用于：

- 发布 Windows 安装包
- 展示当前版本更新说明
- 放 release 截图
- 承担公开版本的问题反馈

Wonderful Launcher 是对外产品品牌；当前可下载的 Windows 桌面应用名暂时仍为 ModelFinder。

ComfyUI 是独立的开源项目：

- ComfyUI: https://github.com/comfyanonymous/ComfyUI

---

<div align="center">

**Wonderful Launcher**：一个把 ComfyUI 日常维护收进桌面工作流里的 Windows 控制中心，目前通过 ModelFinder 桌面应用交付。

</div>
