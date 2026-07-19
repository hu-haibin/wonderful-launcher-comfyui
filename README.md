🌐 **English** | [简体中文](README_CN.md) | [繁體中文](README_ZH_TW.md) | [日本語](README_JA.md) | [한국어](README_KO.md)

<div align="center">

# Wonderful Launcher for ComfyUI on Windows

### You downloaded a ComfyUI workflow. Now make it actually run.

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/wonderful-launcher-comfyui?style=for-the-badge&logo=github&label=Latest%20Release)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
[![Product Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2Fwonderful-launcher-comfyui%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=Product%20Downloads)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)

[**Download 2.1.11**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11) · [**Official Website**](https://wonderfullauncher.com/) · [**Docs**](https://wonderfullauncher.com/docs) · [**Report Issues**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## Download

- **Recommended**: [Wonderful Launcher 2.1.11 Setup](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)
- **Installer file**: `WonderfulLauncher-Setup-v2.1.11.exe`
- **Checksum file**: `SHA256SUMS.txt` in the same release
- **Fallback**: [2.1.10](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.10) is kept as the previous stable release

> [!WARNING]
> Do not download GitHub's auto-generated `Source code.zip` or `Source code.tar.gz`. They are source archives, not Windows installers.

> [!TIP]
> The normal installer is self-contained. You do not need to install Microsoft .NET Desktop Runtime separately.

> [!IMPORTANT]
> If an older build downloads an update but opens the old app again, run the latest **Setup Installer** above. It keeps launcher data, converges legacy `ModelFinder` / `Wonderful Launcher` data into `WonderfulLauncher`, clears old update state, and starts the latest app.

<p align="center">
  <img src="assets/screenshots/home-launch-surface.png" alt="Wonderful Launcher home screen" width="86%" />
</p>

---

## If this sounds familiar

You found a workflow you want to try. You open it in ComfyUI, and suddenly there are red nodes, missing models, dependency errors, or a startup log that only says what broke after you already lost ten minutes.

That is the annoying part this launcher is built for. It keeps the practical cleanup work close to the ComfyUI package you are actually using:

| What you are trying to do | What the launcher helps with |
|---------------------------|------------------------------|
| “I already have ComfyUI somewhere.” | Import ComfyUI Desktop or a portable ComfyUI folder. |
| “I want a clean package instead of fixing this mess.” | Download and deploy a fresh ComfyUI package. |
| “ComfyUI does not start.” | Show the startup log and run approved dependency repair tasks. |
| “This workflow says models are missing.” | Match model names and download or place files into the expected folders. |
| “The workflow has missing nodes.” | Install custom nodes and dependencies without hunting through folders. |
| “I have several ComfyUI packages but one model library.” | Share a model directory between packages. |
| “I want to generate images and keep history nearby.” | Keep image generation, references, history, and Photoshop handoff in one workspace. |

The goal is not to replace ComfyUI. It is to remove the boring “why is this workflow not running on my machine?” work around it.

---

## What's new in 2.1.11

Released on July 20, 2026. [Open the full GitHub Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11).

- **Cleaner ComfyUI startup**: removed the noisy Torch preflight path that could show a misleading repair prompt before ComfyUI actually failed.
- **Missing-model lookup in the running workspace**: the standalone toolbox model-finder entry was removed. The WebView notification opens the current missing-model result list directly.
- **Simpler model result rows**: focus on workflow filename, target model folder, match status, and download. Bulk actions are now “copy model names” and “download all.”
- **Compact shared model directories**: ComfyUI settings now show the A → B model sharing flow clearly and indicate when a package uses the global shared model path.
- **Image prompt copy polish**: generated-image prompts in the conversation can be selected and copied more naturally.

Validation for this release: full Release test suite passed, the self-contained installer was built by the official release script, and the published app root passed an isolated startup smoke.

---

## Quick start

### 1. Install

1. Open the [latest installer release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11).
2. Download `WonderfulLauncher-Setup-v2.1.11.exe`.
3. Run the installer and open Wonderful Launcher.

This repository is the public download, screenshots, and issue-tracking surface. It is not a public source-code mirror for the desktop app.

### 2. Tell the launcher where your ComfyUI is

- If you already have ComfyUI, choose **Import ComfyUI** and select the folder that contains `main.py`, or the portable parent folder that contains a `ComfyUI` subfolder.
- If you want a clean environment, open ComfyUI settings, choose a disk and runtime package, then deploy and start it from the Home page.

Avoid selecting folders such as `models`, `custom_nodes`, `output`, `python_embeded`, or a folder that only contains workflow files.

### 3. Let the workflow tell you what is missing

When a workflow opens with red nodes or missing assets, follow the normal repair loop:

1. inspect missing models or nodes
2. download or place the missing files
3. install missing custom nodes or dependencies
4. restart or rerun ComfyUI
5. verify that the workflow generates output

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

## Releases and repository scope

The GitHub Releases page is kept intentionally sparse: the latest installer plus one previous stable fallback. Older tags are preserved for history, but older release pages may be removed so new users are not encouraged to download stale builds.

- [Latest Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
- [Wonderful Launcher 2.1.11](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.11)
- [Wonderful Launcher 2.1.10 fallback](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/tag/v2.1.10)

Release notes live on GitHub Releases and the current README summary. This repository intentionally avoids a separate pile of stale per-version note files.

This repository intentionally does not expose the full desktop source tree. Public release assets are the Windows installer and checksum file attached to GitHub Releases.
