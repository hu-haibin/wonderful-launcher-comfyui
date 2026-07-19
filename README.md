🌐 **English** | [简体中文](README_CN.md)

<div align="center">

# Wonderful Launcher for ComfyUI on Windows

### A desktop launcher that helps downloaded ComfyUI workflows actually run.

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/wonderful-launcher-comfyui?style=for-the-badge&logo=github&label=Latest%20Release)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
[![Product Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2Fwonderful-launcher-comfyui%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=Product%20Downloads)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)

[**Download 2.1.11**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11) · [**Release Notes**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11) · [**Official Website**](https://wonderfullauncher.com/) · [**Docs**](https://wonderfullauncher.com/docs) · [**Report Issues**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## Download

- **Recommended installer**: [Wonderful Launcher 2.1.11 Setup](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)
- **Installer file**: `WonderfulLauncher-Setup-v2.1.11.exe`
- **Checksums**: included as `SHA256SUMS.txt` in the same release

> [!WARNING]
> Do not download GitHub's auto-generated `Source code.zip` or `Source code.tar.gz`. Those are source archives, not runnable Windows desktop builds.

> [!TIP]
> The normal installer is self-contained for desktop runtime needs. You do not need to install Microsoft .NET Desktop Runtime separately.

> [!IMPORTANT]
> If an older build downloads an update but opens the old app again, download and run the latest **Setup Installer** above. The installer is the supported repair path: it keeps your launcher data, moves legacy `ModelFinder` / `Wonderful Launcher` data into `WonderfulLauncher`, cleans old update state, and starts the latest Wonderful Launcher.

<p align="center">
  <img src="assets/screenshots/home-launch-surface.png" alt="Wonderful Launcher home screen" width="84%" />
</p>

---

## Why It Exists

Downloading a ComfyUI workflow is only the first step. To make it run locally, you may still need the right model files, custom nodes, Python packages, PyTorch build, folder placement, startup arguments, and repair steps when the environment breaks.

Wonderful Launcher turns those maintenance tasks into one Windows desktop workflow:

- import an existing ComfyUI Desktop or portable ComfyUI folder
- deploy a fresh ComfyUI package when you want a clean start
- launch ComfyUI and read startup logs in the same app
- find missing workflow models and put them in the expected folder
- install missing custom nodes and plugin dependencies
- use launcher-native repair tasks for deterministic startup failures, with Agent kept to bounded diagnosis
- manage image generation, reference images, history, and Photoshop handoff close to the ComfyUI runtime

The goal is not to replace ComfyUI. The goal is to make local ComfyUI easier to keep in a working state.

---

## What It Helps With

| When this happens | Wonderful Launcher helps you |
|-------------------|------------------------------|
| You already installed ComfyUI Desktop or a portable package | Import it and manage it from one desktop surface. |
| You want a clean ComfyUI install | Pick a disk, choose a runtime package, download, extract, and launch. |
| ComfyUI will not start | Inspect logs, approve launcher-native repair tasks, install core requirements or PyTorch, then restart for verification. |
| A workflow says models are missing | Find likely model downloads, copy links, or download into the correct folder. |
| You already downloaded a model manually | Drag the model file into the app and let the launcher place it where the workflow expects it. |
| A workflow has missing nodes | Install the needed nodes and dependencies without hunting through folders manually. |
| A plugin imports but fails at runtime | Use logs, task-terminal evidence, and bounded diagnosis to work through dependency conflicts. |
| You want to generate and reuse images | Use the image workspace, reference thumbnails, generation history, and Photoshop handoff. |

---

## What's New in 2.1.11

Released on July 20, 2026. [Open the full GitHub Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11).

This release smooths the ComfyUI launch path and moves missing-model work into the place where users actually need it: the running ComfyUI workspace.

- **Cleaner ComfyUI startup**: startup no longer blocks on a noisy Torch preflight probe. Real ComfyUI process failures still produce logs and can lead to dependency repair when the error is genuine.
- **Missing-model flow in the workspace**: the standalone toolbox model-finder entry was removed. The WebView notification bar now opens the current missing-model result list directly, using the live ComfyUI workflow context.
- **Less confusing model results**: the missing-model list focuses on the workflow filename, target model folder, match status, and the download action. The bulk actions are clearer: copy model names or download all available models.
- **Simpler shared model directories**: ComfyUI settings now use a compact A → B sharing layout and show when a package is using a global shared model path.
- **Small image workflow polish**: generated-image prompts in the conversation can be selected and copied more naturally.
- **Release validation**: the self-contained v2.1.11 package passed the full Release test suite and a published-root startup smoke.

---

## Quick Tutorial

### 1. Install Wonderful Launcher

1. Open the [2.1.11 installer release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11).
2. Download `WonderfulLauncher-Setup-v2.1.11.exe`.
3. Run the installer and open Wonderful Launcher.

This repository is the public download and guide page. It is not a public source-code mirror for the desktop app.

### 2. Import an existing ComfyUI

Use this when you already have ComfyUI Desktop, a portable ComfyUI package, or another local ComfyUI folder.

1. Open Wonderful Launcher.
2. Choose **Import ComfyUI**.
3. Select the folder that contains `main.py`, or the portable parent folder that contains a `ComfyUI` subfolder.
4. Start ComfyUI from the Home page and watch the startup log.

Avoid selecting folders such as `models`, `custom_nodes`, `output`, `python_embeded`, or a folder that only contains workflow files.

### 3. Deploy a new ComfyUI

Use this when you want a clean environment instead of repairing an old one.

1. Open ComfyUI settings.
2. Go to the deployment section.
3. Choose the target disk and runtime package for your GPU.
4. Start deployment and wait for download and extraction to finish.
5. Launch the new ComfyUI package from the Home page.

If you prefer an external downloader, you can download the package yourself and then import the extracted folder.

### 4. Run a downloaded workflow

When a workflow opens with red nodes or missing assets, treat that as normal ComfyUI maintenance. Most shared workflows depend on specific models, custom nodes, and Python packages.

Wonderful Launcher is designed around that loop:

1. open or import the workflow
2. inspect missing models or nodes
3. install or place what is missing
4. restart or rerun ComfyUI
5. verify that the workflow can generate output

### 5. Fix startup failures

ComfyUI may fail because PyTorch is missing, Python dependencies are broken, a plugin changed the environment, or a runtime package was moved.

Use the startup log and environment pages first. When the cause is not obvious, open the Agent panel. The Agent can read the relevant state, explain likely causes, and propose supported repair actions. Repair actions require your approval.

### 6. Handle missing models

Model files are often large, and the correct target folder is not always obvious. A downloaded workflow may need checkpoints, LoRA, VAE, ControlNet, diffusion models, text encoders, or other model types.

Wonderful Launcher can help you:

- detect missing model names from a workflow
- copy or open download links when available
- download directly into the expected folder
- drag an already-downloaded model file into the app and place it correctly

### 7. Use the image workspace

The image workspace keeps generation controls, reference thumbnails, history, and Photoshop handoff in one place.

Reference-image behavior introduced in 2.1.5 remains available:

- thumbnails appear immediately but dim while the file is still preparing
- a centered circular `0%` indicator marks the preparing state
- ready thumbnails return to the normal image preview
- double-clicking a path-backed current reference opens the viewer

---

## Screenshots

<p align="center">
  <img src="assets/screenshots/feature-environment.png" alt="Environment management" width="32%" />
  <img src="assets/screenshots/feature-model-manager.png" alt="Model manager" width="32%" />
  <img src="assets/screenshots/feature-plugin-manager.png" alt="Plugin manager" width="32%" />
</p>

<p align="center">
  <img src="assets/screenshots/home-live-startup-logs.png" alt="Startup logs and launch status" width="32%" />
  <img src="assets/screenshots/feature-image-workspace.png" alt="Image workspace" width="32%" />
  <img src="assets/screenshots/feature-image-photoshop-send.png" alt="Photoshop handoff" width="32%" />
</p>

---

## Updates

The GitHub Releases page keeps the current public installer so new users have a clear download choice.

Older release tags are kept for project history, but they are not recommended as public downloads unless a maintainer explicitly points you to one.

- [Latest Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
- [Wonderful Launcher 2.1.11 Release Notes](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)
- [Wonderful Launcher 2.1.11 Setup Installer](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)

---

## FAQ

<details>
<summary><b>Why do I still see ModelFinder or mf in some Windows places?</b></summary>

Wonderful Launcher is the public product name. Some internal identifiers intentionally remain `ModelFinder` or `mf` to preserve installed paths, update compatibility, logs, and Windows identity.

</details>

<details>
<summary><b>Do I need to install Python first?</b></summary>

No. In the normal path, Wonderful Launcher manages the ComfyUI Python environment for you.

</details>

<details>
<summary><b>Can it manage my existing ComfyUI install?</b></summary>

Yes. Use **Import ComfyUI** and select the folder that contains `main.py`, or the portable parent folder that contains a `ComfyUI` subfolder.

</details>

<details>
<summary><b>Does the Agent run repair actions automatically?</b></summary>

No. Write or repair actions require your approval. The Agent helps with diagnosis and can run supported launcher tools after you approve them.

</details>

<details>
<summary><b>Is macOS or Linux supported?</b></summary>

Not currently. This repository publishes Windows desktop builds.

</details>

---

## Repository Scope

This repository is the public release, download, README, screenshot, and issue-tracking surface for Wonderful Launcher.

It intentionally does not expose the full desktop source tree. Public release assets are the Windows installer and checksum file attached to GitHub Releases.
