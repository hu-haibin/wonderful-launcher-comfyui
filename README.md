🌐 **English** | [简体中文](README_CN.md)


<div align="center">

# ComfyUI Install Windows Download

### All-in-one ComfyUI launcher and manager — model downloader, custom nodes installer, environment manager, and workflow analyzer.

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=Latest%20Release)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.cumulative_downloads&style=for-the-badge&logo=github&label=Downloads)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**Download Stable**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**Beta / Early Access**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**Release Notes**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**Report Issues**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

</div>

---

## Why ModelFinder

Every new ComfyUI workflow can mean missing models, missing custom nodes, broken dependencies. You end up chasing files across HuggingFace, Civitai, and GitHub before you can even hit "Queue Prompt".

ModelFinder is a **ComfyUI launcher and manager** that puts workflow analysis, model downloading, custom nodes installation, and environment management in one place — so you spend time generating, not debugging setup.

---

## Getting Started

### First Time

1. Download the **Setup Installer** or **Portable ZIP** from [Releases](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
2. Launch ModelFinder — the one-click installer walks you through deploying ComfyUI (version, GPU acceleration, optional components)
3. Or skip deployment and point ModelFinder at your existing ComfyUI portable package
4. **Already using ComfyUI Desktop?** Just add your `Documents\ComfyUI` folder — ModelFinder auto-detects the Desktop installation

No Python or .NET installation required. Everything is bundled.

### Daily Use

Open ModelFinder → click **Start** on the Home page → ComfyUI launches with real-time logs in the built-in terminal → open the Web UI in the embedded workspace or in your browser.

That's it for basic use. The rest of ModelFinder is there when you need it.

---

## What You Can Do

### Home — Launch and Monitor

Your starting point. A capsule-shaped control button lets you start/stop ComfyUI with one click. When running, a built-in browser workspace opens ComfyUI's Web UI right inside the launcher — no need to switch windows.

The bottom toolbar gives you quick access to common folders (Models, Output, Workflows, Custom Nodes, Python) and usage statistics (today's usage time, session duration, total launches, last used). A real-time terminal drawer at the bottom shows ComfyUI process logs.

The workspace also detects issues with the current workflow — if custom nodes or models are missing, a notification bar appears with one-click actions to install nodes, download models, or restart ComfyUI.

Hardware info (OS, CPU, Memory, GPU, VRAM, Motherboard) is displayed at a glance. Launch parameters — port, GPU mode (Auto / RTX fp16 / CPU), and custom arguments — are configurable from the gear button.

### Environments — Deploy and Manage

**Deploy** a fresh ComfyUI installation with version selection, GPU acceleration options (NVIDIA CUDA / AMD ROCm), and optional preinstalled components.

**Manage** multiple ComfyUI installations side by side — including **ComfyUI Desktop** installations. See Python, PyTorch, and ComfyUI versions at a glance. Switch ComfyUI core versions by tag, switch PyTorch/CUDA configurations visually, and install Python development headers when needed.

A full **pip dependency table** lets you search, install, upgrade, switch versions, or batch-uninstall Python packages. You can also drag-and-drop `.txt` (requirements) or `.whl` (wheel) files to install them directly. Pip cache cleanup and pip self-upgrade are one click away.

### Workflows — Model Finder and Downloader

> Requires sign-in to a ModelFinder account.

Drop in a workflow file (JSON or PNG), and ModelFinder scans your local models, identifies what's missing, and automatically finds download links from a cloud catalog across **HuggingFace**, **ModelScope**, and **Civitai**. When a match is uncertain, you can pick from a list of candidates or reject false positives.

Accept matches and download all missing models in one go — or copy the list to your clipboard for manual searching. Supports batch analysis across multiple workflow files or entire folders.

### Plugins — Custom Nodes Installer and Manager

Browse all installed custom nodes with status, Git info, and dependency indicators. Toggle plugins on/off, install Python dependencies (with pip mirror selection: PyPI / Tsinghua / Aliyun / Tencent / Douban), open GitHub repos, or delete plugins entirely.

Install new custom nodes from any Git URL — ModelFinder clones the repository and auto-installs its Python dependencies. Bulk enable/disable and bulk dependency installation are available for managing large plugin sets.

### Models — Model Library and Download Manager

**Model Library** gives you a visual browser for all your local model files — checkpoints, LoRAs, VAEs, ControlNets, CLIP, and more — with category filtering and search. Open any model's folder or delete unused ones directly. Switch to **All Packages** mode to see models across every ComfyUI installation, with duplicate detection and reclaimable space estimates.

**Download Manager** shows all active and completed downloads in one place. Active downloads show live progress, speed, and ETA with pause/resume/cancel controls. Completed downloads can be opened or cleared from the list.

### AI Assistant

A global chat panel accessible from the title bar. When something goes wrong, the AI can analyze your logs, suggest repair commands, execute them with your approval, and verify the fix. Suggested prompts help you get started: diagnose failures, check dependencies, or summarize recovery steps.

AI features are managed server-side — sign in to your account to use them.

### Settings

- **Account**: Sign in/out, view subscription plan, credit balance, and billing
- **General**: Language (English / Chinese / System), close behavior, shared model directory with junction linking
- **Network**: HuggingFace mirror toggle, Aria2 multi-connection download accelerator
- **AI**: Proxy configuration, raw log upload preference
- **Advanced**: System dependency manager (Git, 7-Zip, VC Redist), log viewer, cache cleanup, update manager

---

## Personalization

- **Language**: English / Simplified Chinese / Follow system — instant switch, no restart
- **Theme**: Dark / Light with synchronized ComfyUI theme
- **Color schemes**: Multiple accent palettes
- Built with **Windows Fluent Design** for a modern, native feel

---

## Release Tracks

| Track | For |
|-------|-----|
| **Stable** | Most users — the recommended public build |
| **Beta** | Users who want early access to new features and accept occasional rough edges |

Beta builds ship from the same repository and may include unfinished features or temporary regressions before promotion to stable.

---

## System Requirements

| Item | Requirement |
|------|-------------|
| **OS** | Windows 10 (22H2+) / Windows 11 |
| **Disk** | ~100 MB for the launcher itself |
| **GPU** | NVIDIA (CUDA) or AMD (ROCm) recommended for ComfyUI |
| **Runtime** | Nothing extra — all dependencies are bundled |

---

## FAQ

<details>
<summary><b>Do I need to install Python or .NET?</b></summary>

No. ModelFinder is self-contained. ComfyUI's Python environment is set up by the deployment wizard.
</details>

<details>
<summary><b>Can it manage my existing ComfyUI installation?</b></summary>

Yes. Go to Environments, click "Add Directory", and select your existing ComfyUI portable folder. Your files are not modified.
</details>

<details>
<summary><b>Can it take over ComfyUI Desktop?</b></summary>

Yes. Add your `Documents\ComfyUI` folder and ModelFinder will auto-detect the Desktop installation, including its Python environment, custom nodes, and models. The Desktop app's files are never modified — ModelFinder only reads from them.
</details>

<details>
<summary><b>Is AMD GPU supported?</b></summary>

Yes. Choose AMD ROCm during deployment, or import an existing AMD environment.
</details>

<details>
<summary><b>How does the AI Assistant work?</b></summary>

Sign in to your ModelFinder account. The AI Assistant panel is accessible from the title bar. When ComfyUI encounters issues, the AI analyzes your logs, generates repair commands, and executes them with your approval. You can also ask it questions directly in the chat interface.
</details>

<details>
<summary><b>Is macOS or Linux supported?</b></summary>

Not currently. Windows 10/11 only.
</details>

<details>
<summary><b>Upgrading from ComfyLauncher (v1.3.x)?</b></summary>

ModelFinder automatically migrates your config from `%AppData%/ComfyLauncher`. Both `ComfyLauncher.exe` and `ModelFinder.exe` are recognized for a seamless transition.
</details>

---

## Feedback

- **Bug reports / feature requests**: [Issues](https://github.com/hu-haibin/ModelFinder-Releases/issues)
- If ModelFinder helps you, a star is appreciated

---

## License

ModelFinder is closed-source software. This repository provides compiled release binaries only.
ModelFinder is not affiliated with ComfyUI. ComfyUI is an independent open-source project.

---

<div align="center">

**ModelFinder** — From workflow to output, without the setup friction.

Made with ❤️ for the AI Art Community

</div>
