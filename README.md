🌐 **English** | [简体中文](README_CN.md)

<div align="center">

# ModelFinder for ComfyUI on Windows

### Install, launch, repair, and manage ComfyUI from one desktop app.

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=Latest%20Release)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![Product Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=Product%20Downloads)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**Download Latest Installer**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**Official Website**](https://wonderfullauncher.com/) · [**Docs**](https://wonderfullauncher.com/docs) · [**Troubleshooting**](https://wonderfullauncher.com/troubleshooting) · [**2.0.29 Release Notes**](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.29) · [**All Releases**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**Report Issues**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

</div>

---

## Why people use ModelFinder

ComfyUI is powerful, but Windows maintenance is usually spread across too many places: Python, PyTorch, custom nodes, missing models, startup logs, downloads, and half-finished repair attempts.

ModelFinder brings those jobs into one desktop workflow so you can:

- deploy a fresh ComfyUI environment or import an existing one
- start, stop, and inspect the runtime without hunting for batch files
- install custom nodes and dependencies from the launcher
- find missing workflow models and nodes faster
- manage downloads, packages, and environment state in one place
- use an approval-based AI Assistant to explain and run supported repair steps

<p align="center">
  <img src="assets/screenshots/2.0.15-home.png" alt="ModelFinder home screen" width="84%" />
</p>

---

## What you can do today

| Workflow | What ModelFinder gives you |
|----------|----------------------------|
| **Install or import ComfyUI** | Attach an existing install or deploy a new one without guessing which folder is the real root. |
| **Launch and inspect runtime** | Start ComfyUI, open the built-in workspace, and inspect live startup logs from the same app. |
| **Manage custom nodes** | Install plugins, run dependency installs, remove broken nodes, and verify whether a node is really available. |
| **Find missing workflow assets** | Scan a workflow for missing nodes or models and jump to the most relevant repair/download path. |
| **Use the image workspace** | Generate images, reuse previous results, send images to Photoshop, and keep history inside the launcher. |
| **Ask the AI Assistant to repair** | Let the assistant explain startup failures, dependency errors, and missing-node problems, then approve supported repair actions when needed. |

---

## What's new in 2.0.29

Released on June 17, 2026. [Open the full GitHub Release](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.29).

This release keeps Avalonia as the mainline desktop shell and smooths out a few rough edges that were still slowing down real workflow use.

- **Visible app update progress**: Avalonia now shows update download/apply progress directly under the title bar instead of looking idle during silent update flow.
- **One-click workflow template handoff**: clicking a workflow template now opens or starts the embedded ComfyUI workspace and imports the workflow for you.
- **Animated template previews**: official workflow template previews can now animate in Avalonia when the source asset is GIF/WebP/APNG, so video-style templates are easier to judge before opening.
- **Lighter deploy selection styling**: the ComfyUI deploy page uses a softer light-theme selected state for drive and GPU choices, which reads more cleanly in the new shell.

---

## Screenshots

<p align="center">
  <img src="assets/screenshots/feature-home.png" alt="ModelFinder home surface" width="32%" />
  <img src="assets/screenshots/feature-plugin-manager.png" alt="Plugin manager" width="32%" />
  <img src="assets/screenshots/feature-model-finder.png" alt="Workflow model finder" width="32%" />
</p>

<p align="center">
  <img src="assets/screenshots/feature-environment.png" alt="Environment management" width="32%" />
  <img src="assets/screenshots/feature-image-workspace.png" alt="Image workspace" width="32%" />
  <img src="assets/screenshots/feature-image-photoshop-send.png" alt="Photoshop handoff" width="32%" />
</p>

---

## Quick start

### Install

1. Open the [latest GitHub Release](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest).
2. Download `ModelFinderLauncher-Setup-v*.exe`.
3. Run the installer and launch ModelFinder.

> [!WARNING]
> Download the **Setup Installer** from the release assets. Do **not** download GitHub's auto-generated `Source code.zip` or `Source code.tar.gz`. Those are source archives, not runnable desktop builds.

> [!TIP]
> The public installer is self-contained for normal desktop runtime needs. You do not need to install Microsoft .NET Desktop Runtime separately.

### Import an existing ComfyUI

1. Open ModelFinder on the Home page.
2. Click **Import ComfyUI**.
3. Select the folder that contains `main.py`, or the portable parent folder that contains a `ComfyUI` subfolder.
4. Start ComfyUI from the Home page.

Avoid selecting these folders by mistake:

- `models`
- `custom_nodes`
- `output`
- `python_embeded`
- a folder that only contains workflow files

---

## Recent release history

For ordinary users, the latest release is the only recommended download. Older versions may be hidden or removed when a newer stable installer replaces them.

| Version | Date | Summary |
|---------|------|---------|
| **2.0.29** | June 17, 2026 | Avalonia workflow polish release with visible update progress, clickable workflow templates, animated previews, and lighter deploy-page selection styling. |
| **2.0.28** | June 17, 2026 | Avalonia polish release for AI Assistant entry prompts, log-triage drift guards, simplified approvals, and signed-in model lookup gates. |
| **2.0.27** | June 16, 2026 | Avalonia public release with WinUI-to-Avalonia upgrade continuity, Image credit flow polish, and workspace repair improvements. |
| **2.0.26** | June 9, 2026 | WinUI reliability release for Agent repair, image workspace polish, and support observability. |

See the [GitHub Releases page](https://github.com/hu-haibin/ModelFinder-Releases/releases) for full notes.

---

## FAQ

<details>
<summary><b>Do I need to install Python first?</b></summary>

No. In the normal path, ModelFinder manages the ComfyUI Python environment for you.

</details>

<details>
<summary><b>Can it manage my existing ComfyUI install?</b></summary>

Yes. Use **Import ComfyUI** and select the folder that contains `main.py`, or the portable parent folder that contains a `ComfyUI` subfolder.

</details>

<details>
<summary><b>Does it support custom nodes?</b></summary>

Yes. You can install custom nodes, run dependency installs, manage plugin state, and use the assistant for supported repair steps.

</details>

<details>
<summary><b>Does the AI Assistant run actions automatically?</b></summary>

Write or repair actions still require approval. The assistant helps with diagnosis and can run supported launcher tools after you approve them.

</details>

<details>
<summary><b>Is macOS or Linux supported?</b></summary>

Not currently. This repository publishes Windows desktop builds.

</details>

---

## About this repository

This repository is the public release home for ModelFinder:

- Windows installer downloads
- current release notes
- release screenshots
- public issue tracking for released builds

ModelFinder is a closed-source desktop product built around the ComfyUI ecosystem.

ComfyUI itself is an independent open-source project:

- ComfyUI: https://github.com/comfyanonymous/ComfyUI

---

<div align="center">

**ModelFinder**: a Windows control center for ComfyUI environments.

</div>
