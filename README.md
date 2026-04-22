🌐 **English** | [简体中文](README_CN.md)


<div align="center">

# ComfyUI Install Windows Download

### A Windows launcher for ComfyUI that gets you from workflow to output, faster.

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=Latest%20Release)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.cumulative_downloads&style=for-the-badge&logo=github&label=Downloads)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**Download Stable**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**Beta / Early Access**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**Release Notes**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**Report Issues**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

</div>

---

## Why ModelFinder

Every new ComfyUI workflow can mean missing models, missing plugins, broken dependencies. You end up chasing files across HuggingFace, Civitai, and GitHub before you can even hit "Queue Prompt".

ModelFinder puts **workflow analysis, resource downloads, environment management, and launching** in one place — so you spend time generating, not debugging setup.

<div align="center">
<img src="screenshots/home.png" width="80%" alt="Home — Launch and monitor ComfyUI with built-in terminal">
</div>

---

## Getting Started

### First Time

1. Download the **Setup Installer** or **Portable ZIP** from [Releases](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
2. Launch ModelFinder — the deployment wizard walks you through installing ComfyUI (version, GPU acceleration, optional components)
3. Or skip deployment and point ModelFinder at your existing ComfyUI portable package
4. **Already using ComfyUI Desktop?** Just add your `Documents\ComfyUI` folder — ModelFinder auto-detects the Desktop installation

No Python or .NET installation required. Everything is bundled.

### Daily Use

Open ModelFinder → click **Start** on the Home page → ComfyUI launches with real-time logs in a built-in terminal → open the Web UI directly inside the launcher or in your browser.

That's it for basic use. The rest of ModelFinder is there when you need it.

---

## What You Can Do

### Home — Launch and Monitor

Your starting point. A full-size terminal console shows ComfyUI logs in real time. A floating action island in the bottom-right lets you start/stop ComfyUI, open the Web UI, or switch between instances. The **built-in browser workspace** lets you use ComfyUI without leaving the launcher. You can also configure launch parameters (port, GPU memory mode, custom arguments) and quickly open common folders (models, outputs, custom_nodes).

When something goes wrong, the **AI Diagnosis** feature can analyze your logs, suggest repair commands, execute them with your approval, and verify the fix — with rollback if needed.

<details>
<summary>Screenshots</summary>

| AI Diagnosis | Hardware Monitor |
|:---:|:---:|
| <img src="screenshots/ai-diagnosis.png" width="400"> | <img src="screenshots/hardware-monitor.png" width="400"> |

</details>

### Environments — Deploy and Manage Packages

**Deploy** a fresh ComfyUI installation with version selection, GPU acceleration options (NVIDIA CUDA / AMD ROCm), and optional preinstalled components (ComfyUI-Manager, translation packs, popular nodes). Visual step-by-step progress with failure recovery.

**Packages** lets you manage multiple ComfyUI installations side by side — including **ComfyUI Desktop** installations. See Python/PyTorch/ComfyUI versions and disk usage at a glance. Switch PyTorch/CUDA versions visually, upgrade or rollback ComfyUI core, export/import pip environments, and clean up pip cache.

<details>
<summary>Screenshots</summary>

| Deployment Wizard | Package Manager | PyTorch Manager |
|:---:|:---:|:---:|
| <img src="screenshots/deployment.png" width="270"> | <img src="screenshots/package-manager.png" width="270"> | <img src="screenshots/pytorch-manager.png" width="270"> |

</details>

### Workflows — Batch Tasks and Diagnosis

**Batch Queue** automates large-scale generation through the ComfyUI API. Load a workflow, configure parameter replacements (supports batch prompts from files), set repeat count and random seed, define auto-restart intervals to avoid memory leaks, and resume from interruption.

**Workflow Diagnosis** checks your workflows for issues before you run them.

<details>
<summary>Screenshots</summary>

| Batch Queue | Dependency Analysis |
|:---:|:---:|
| <img src="screenshots/batch-queue.png" width="400"> | <img src="screenshots/dependency-analysis.png" width="400"> |

</details>

### Plugins — Manage and Install

Browse all installed custom nodes with Git info, size, and search. Switch plugin versions by commit, rollback, or manage Python dependencies.

When you load a workflow that needs plugins you don't have, the **Install Missing Plugins** tab detects them and installs with one click (Git clone + pip dependencies).

<details>
<summary>Screenshot</summary>

<img src="screenshots/plugin-management.png" width="80%">
</details>

### Models — Library, Finder, and Downloads

**Model Library** gives you a visual browser for your local model files with search and category filtering (checkpoint, LoRA, VAE, etc.).

**Model Finder** is the core differentiator. Drop in a workflow (JSON or PNG), and it scans your local models, identifies what's missing, and automatically matches download sources from a cloud catalog across HuggingFace, ModelScope, and Civitai. Accept matches and download all in one go. Supports batch analysis across multiple files or entire folders.

**Downloads** is a unified download manager with live progress, pause/resume, and batch cleanup.

<details>
<summary>Screenshots</summary>

| Model Finder | Model Library | Download Center |
|:---:|:---:|:---:|
| <img src="screenshots/model-finder.png" width="270"> | <img src="screenshots/model-management.png" width="270"> | <img src="screenshots/download-center.png" width="270"> |

</details>

---

## Personalization

- **Language**: English / Simplified Chinese / Follow system — instant switch, no restart
- **Theme**: Dark / Light with synchronized ComfyUI theme
- **Color schemes**: Multiple accent palettes
- **UI density**: Comfortable / Compact
- **Reduced motion**: Disable animations on low-end devices
- Built with **Windows Fluent Design** for a modern, native feel

<details>
<summary>Screenshots</summary>

| Dark Theme (Chinese) | Light Theme (English) | Settings |
|:---:|:---:|:---:|
| <img src="screenshots/home.png" width="270"> | <img src="screenshots/light-theme-english.png" width="270"> | <img src="screenshots/settings.png" width="270"> |

</details>

---

## Release Tracks

| Track | For |
|-------|-----|
| **Stable** | Most users — the recommended public build |
| **Beta** | Users who want early access to new features and accept occasional rough edges |

All features are currently free. Beta builds ship from the same repository and may include unfinished features or temporary regressions before promotion to stable.

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

Yes. Go to Environments → Packages, add your existing ComfyUI portable folder. Your files are not modified.
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
<summary><b>How does AI Diagnosis work?</b></summary>

Configure an API key and endpoint in Settings → AI Settings. When ComfyUI fails, the AI analyzes your logs, generates repair commands, and executes them with your approval. You can rollback if the result isn't satisfactory.
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
