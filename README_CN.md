🌐 [English](README.md) | **简体中文**

<div align="center">

# ModelFinder for ComfyUI

### 一个面向 Windows 的 ComfyUI 启动、管理、诊断与修复工具。

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=最新版本)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.cumulative_downloads&style=for-the-badge&logo=github&label=下载量)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/平台-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**下载**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**所有版本**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**反馈问题**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

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

## 核心能力

| 模块 | 能做什么 |
|------|----------|
| **首页** | 启动/停止 ComfyUI，查看实时日志，打开内置工作区，查看基础运行状态 |
| **环境** | 部署 ComfyUI，管理多个安装，切换 ComfyUI / PyTorch 版本，安装 `.txt` 与 `.whl` 依赖 |
| **工作流** | 分析工作流文件，识别缺失模型，并从支持的目录中匹配候选下载项 |
| **插件** | 从 Git URL 安装自定义节点，管理插件依赖，批量启用或禁用插件 |
| **模型** | 浏览本地模型库，检测跨包重复文件，管理下载任务 |
| **AI 助手** | 诊断日志、解释报错，并在授权后执行支持的修复动作 |
| **下载** | 排队、跟踪、暂停、恢复和管理模型下载 |

---

## AI 助手

AI 助手集成在桌面端聊天面板里。

它目前可以：

- 读取启动器收集到的日志和环境状态
- 解释启动失败、依赖报错、插件安装失败等问题
- 给出修复建议
- 在你授权后调用启动器内置工具执行修复
- 在同一会话里继续多步修复流程

需要注意：

- AI 功能需要登录账号
- 使用按积分计费，由服务端统一管理
- 当前计费和价格规则以官方网站为准，不以本发版仓 README 为准

---

## 快速开始

### 首次使用

1. 从 [Releases](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) 下载最新 **Setup 安装包** 或 **便携 ZIP**
2. 启动 ModelFinder
3. 选择部署新的 ComfyUI 环境，或导入已有环境
4. 在首页点击 **启动**，运行 ComfyUI

> [!TIP]
> 正常使用时，不需要你额外安装 Python 或 .NET。

### 已有环境

ModelFinder 可以管理这些场景：

- 已存在的 ComfyUI 便携包目录
- 多个并行存在的 ComfyUI 环境
- 通过 `Documents\\ComfyUI` 导入的 ComfyUI Desktop 环境

它的定位是管理和诊断这些环境，不是无提示地覆盖你的原有文件。

---

## 当前产品边界

- **平台**：Windows 10 / 11
- **发布形态**：这个仓库发布的是公开 Windows 构建
- **预发布版本**：如果未来有 beta / prerelease，会在 GitHub Releases 中明确标记
- **云端能力**：AI 助手和部分工作流匹配能力依赖登录与服务端能力

---

## 常见问题

<details>
<summary><b>需要先安装 Python 吗？</b></summary>

不需要。标准使用场景下，ModelFinder 会帮你管理 ComfyUI 的 Python 环境。

</details>

<details>
<summary><b>可以接管我现有的 ComfyUI 吗？</b></summary>

可以。你可以添加已有的 ComfyUI 文件夹，让它和新环境一起被管理。

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

- 发布 Windows 安装包与便携包
- 保存 release 历史
- 承担公开版本的问题反馈

ModelFinder 本身是围绕 ComfyUI 生态构建的闭源桌面产品。

ComfyUI 是独立的开源项目：

- ComfyUI: https://github.com/comfyanonymous/ComfyUI

---

<div align="center">

**ModelFinder** —— 一个面向 ComfyUI 环境的 Windows 控制中心。

</div>
