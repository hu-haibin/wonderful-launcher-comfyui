🌐 **English** | [简体中文](README_CN.md)

<div align="center">

# ModelFinder for ComfyUI on Windows

### A desktop control center for installing, launching, repairing, and using ComfyUI on Windows.

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=Latest%20Release)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![Product Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=Product%20Downloads)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**Download Latest Installer**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**Official Website**](https://wonderfullauncher.com/) · [**Docs**](https://wonderfullauncher.com/docs) · [**Troubleshooting**](https://wonderfullauncher.com/troubleshooting) · [**Current Release**](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.31) · [**Report Issues**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

</div>

---

## Download recommendation

- **Recommended for most users**: [ModelFinder 2.0.31](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.31)
- **Public stable fallback**: [ModelFinder 2.0.26](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.26)

We keep this release repo focused on the current safe download path. Transitional or regression-prone releases may be hidden from the Releases page once a newer installer replaces them.

<p align="center">
  <img src="assets/screenshots/feature-home.png" alt="ModelFinder home screen" width="84%" />
</p>

---

## Why ModelFinder exists

ComfyUI on Windows often turns into a maintenance puzzle: Python, PyTorch, custom nodes, missing models, startup logs, downloads, and half-finished repair attempts all live in different places.

ModelFinder brings those jobs into one desktop workflow so you can:

- install a fresh ComfyUI environment or import an existing one
- launch, stop, and inspect the runtime without hunting for scripts
- manage custom nodes and dependency installs from one app
- find missing workflow models and nodes faster
- generate images, reuse history, and keep reference material nearby
- use an approval-based AI Assistant for supported diagnosis and repair steps

---

## Core workflows

| Workflow | What you get |
|----------|--------------|
| **Install or import ComfyUI** | Attach an existing install or deploy a new one without guessing the real root folder. |
| **Launch and inspect runtime** | Start ComfyUI, open the built-in workspace, and inspect startup logs from the same app. |
| **Manage custom nodes** | Install plugins, run dependency installs, remove broken nodes, and verify whether a node is truly available. |
| **Find missing workflow assets** | Scan workflows for missing models or nodes and jump to the nearest repair or download path. |
| **Use the image workspace** | Generate images, reuse previous results, drag history back into the composer, and send images to Photoshop. |
| **Ask the AI Assistant to help** | Let the assistant explain startup failures, dependency errors, and missing-node problems, then approve supported actions when needed. |

---

## What's new in 2.0.31

Released on June 19, 2026. [Open the full GitHub Release](https://github.com/hu-haibin/ModelFinder-Releases/releases/tag/v2.0.31).

This release stabilizes the Avalonia image workspace so longer-running image jobs no longer interrupt the next creative step.

- **Parallel image turns**: you can draft and send the next image request while earlier jobs are still queued or generating.
- **Reference and history parity**: the left `input` rail now behaves more like the main history rail, including viewing, drag reuse, and context actions.
- **Recovered drag-and-drop**: the larger reference drop zone is back, so dragging images into the composer works closer to the older flow.
- **Clearer loading placeholders**: generation state now lives on the card itself with the workflow-template sweep border instead of a floating global banner.
- **Recent regressions fixed**: Enter-to-send and `Generate again` both recover from the broken behavior seen in earlier Avalonia releases.

---

## Screenshots

<p align="center">
  <img src="assets/screenshots/feature-plugin-manager.png" alt="Plugin manager" width="32%" />
  <img src="assets/screenshots/feature-model-finder.png" alt="Workflow model finder" width="32%" />
  <img src="assets/screenshots/feature-environment.png" alt="Environment management" width="32%" />
</p>

<p align="center">
  <img src="assets/screenshots/feature-image-workspace.png" alt="Image workspace" width="32%" />
  <img src="assets/screenshots/feature-image-photoshop-send.png" alt="Photoshop handoff" width="32%" />
  <img src="assets/screenshots/2.0.15-home.png" alt="Launcher overview" width="32%" />
</p>

---

## Quick start

### Install

1. Open the [latest GitHub Release](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest).
2. Download `ModelFinderLauncher-Setup-v*.exe`.
3. Run the installer and launch ModelFinder.

> [!WARNING]
> Download the **Setup Installer** from the release assets. Do not download GitHub's auto-generated `Source code.zip` or `Source code.tar.gz`. Those are source archives, not runnable desktop builds.

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

## Release policy

- The homepage README is for the current recommended download path, not for preserving every historical note.
- The GitHub Releases page should stay sparse: latest release first, plus only deliberate fallback versions.
- Tags can remain for engineering traceability even when a noisy or buggy release entry is removed from the public Releases page.

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
