🌐 **English** | [简体中文](README_CN.md)

<div align="center">

# ModelFinder for ComfyUI on Windows

### A desktop control center for installing, launching, repairing, and managing ComfyUI.

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/wonderful-launcher-comfyui?style=for-the-badge&logo=github&label=Latest%20Release)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)
[![Product Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2Fwonderful-launcher-comfyui%2Fmain%2Fstats%2Fdownloads.json&query=%24.current_product_downloads&style=for-the-badge&logo=github&label=Product%20Downloads)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest)

[**Download Latest Installer**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest) · [**2.0.15 Notes**](release-notes/2.0.15.en.md) · [**All Releases**](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases) · [**Report Issues**](https://github.com/hu-haibin/wonderful-launcher-comfyui/issues)

</div>

---

## Why ModelFinder

ComfyUI is powerful, but Windows setup and maintenance can become messy: Python versions, PyTorch builds, custom nodes, plugin dependencies, workflow assets, model downloads, and launch logs all live in different places.

ModelFinder brings those jobs into one desktop app so ordinary ComfyUI users can:

- deploy or import a ComfyUI environment
- start, stop, and inspect the current runtime
- install custom nodes and plugin dependencies
- scan workflows for missing models or nodes
- manage local model files and download tasks
- diagnose launch failures from real launcher evidence
- ask the AI Assistant to explain and run approved repair steps

<p align="center">
  <img src="assets/screenshots/2.0.15-home.png" alt="ModelFinder 2.0.15 home screen" width="82%" />
</p>

---

## What's New in 2.0.15

Released on May 21, 2026. [Read the full 2.0.15 release notes](release-notes/2.0.15.en.md).

This release focuses on making the AI repair flow more trustworthy.

| Area | What changed |
|------|--------------|
| **Missing-node repair** | The Assistant now binds install actions to the same missing-node snapshot it detected, even if ComfyUI must stop or restart before installation. |
| **Repair visibility** | Tool results now include attempted action, reason, snapshot id, terminal job id, retryability, and recommended next action. |
| **Task isolation** | Agent write operations and manual user operations are coordinated so plugin installs, runtime controls, and environment switches do not run over each other. |
| **Less UI noise** | Fast context reads stay silent; slower environment reads show a delayed inline status instead of a flashing overlay. |
| **Feedback loop** | If enabled, redacted Agent sessions can sync conversation replay, tool sequence, repair timeline, task type, and outcome for debugging and regression tests. |

<p align="center">
  <img src="assets/screenshots/2.0.15-agent-panel.png" alt="ModelFinder 2.0.15 AI Assistant panel" width="82%" />
</p>

---

## Core Workflows

| Workflow | What ModelFinder provides |
|----------|---------------------------|
| **Install or import ComfyUI** | Deploy a new environment or attach an existing ComfyUI folder without guessing which subfolder to choose. |
| **Launch and inspect runtime** | Start/stop ComfyUI, view live logs, open the built-in workspace, and check runtime state from the Home page. |
| **Repair custom nodes** | Detect missing nodes, install ComfyUI-Manager when needed, create terminal tasks, restart, and verify registration. |
| **Manage plugins** | Install custom nodes from Git URLs, enable/disable plugins, remove plugins, and run dependency installs. |
| **Find missing models** | Drop a workflow file, detect missing model references, and match downloadable candidates from supported catalogs. |
| **Manage downloads** | Queue, track, pause, resume, and review model download tasks inside the launcher. |
| **Use AI assistance** | Ask for diagnosis, approve repair tools, and keep multi-step repair evidence in one conversation. |

---

## Feature Gallery

<p align="center">
  <img src="assets/screenshots/feature-environment.png" alt="ModelFinder environment page" width="32%" />
  <img src="assets/screenshots/feature-plugin-manager.png" alt="ModelFinder plugin manager" width="32%" />
  <img src="assets/screenshots/feature-model-finder.png" alt="ModelFinder workflow model finder" width="32%" />
</p>

<p align="center">
  <img src="assets/screenshots/feature-model-manager.png" alt="ModelFinder model manager" width="32%" />
  <img src="assets/screenshots/feature-download-center.png" alt="ModelFinder download center" width="32%" />
  <img src="assets/screenshots/feature-image-workspace.png" alt="ModelFinder image workspace" width="32%" />
</p>

---

## AI Assistant Boundaries

The Assistant is built into the desktop app, but it is not a free-form shell.

It can:

- read launcher-collected logs and selected-environment state
- explain startup failures, dependency errors, and plugin failures
- inspect missing-node and missing-model evidence
- call supported launcher tools after approval
- create task-terminal jobs for long-running installs
- continue repair flows in the same conversation
- use local preferences and project hints when personalization is enabled

It does not:

- bypass user approval for write or repair actions
- change billing or credit rules
- upload local personalization memory as default cloud content
- send full terminal logs, system prompts, workflow files, tokens, or raw environment dumps as feedback data

AI features require sign-in and are credit-based. Current billing rules live on the official service, not in this release repository.

---

## Quick Start

### Install

1. Open the [latest GitHub Release](https://github.com/hu-haibin/wonderful-launcher-comfyui/releases/latest).
2. Download `ModelFinderLauncher-Setup-v*.exe`.
3. Run the installer and open ModelFinder.

> [!WARNING]
> Download the **Setup Installer** from the release assets. Do **not** download GitHub's auto-generated `Source code.zip` or `Source code.tar.gz`. Those are source archives, not runnable desktop builds.

> [!TIP]
> The normal installer is self-contained for desktop runtime needs. You do not need to install Microsoft .NET Desktop Runtime separately.

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

## Current Product Notes

- **Platform**: Windows 10 / 11
- **Release type**: public Windows installer
- **Cloud-backed features**: AI Assistant and some workflow matching features require sign-in and server-side services
- **Local data**: launcher configuration, logs, package state, and optional personalization data stay on the local machine unless a feature explicitly sends a request to the service
- **Prereleases**: beta builds, if available, are marked separately in GitHub Releases

---

## FAQ

<details>
<summary><b>Do I need to install Python first?</b></summary>

No. For standard use, ModelFinder manages the ComfyUI Python environment for you.

</details>

<details>
<summary><b>Can it manage my existing ComfyUI install?</b></summary>

Yes. Use **Import ComfyUI** and select the folder that contains `main.py`, or the portable parent folder that contains a `ComfyUI` subfolder.

</details>

<details>
<summary><b>Does it support custom nodes?</b></summary>

Yes. You can install custom nodes from Git URLs, manage dependencies, enable or disable plugins, and use Agent-assisted missing-node repair.

</details>

<details>
<summary><b>Does the AI Assistant run actions automatically?</b></summary>

It can run supported repair tools only after approval for write or repair actions.

</details>

<details>
<summary><b>Is macOS or Linux supported?</b></summary>

Not currently. This release repository publishes Windows builds.

</details>

---

## About This Repository

This repository hosts:

- compiled Windows installer releases
- [versioned release notes](release-notes/)
- public issue tracking for released builds

ModelFinder is a closed-source desktop product built around the ComfyUI ecosystem.

ComfyUI is an independent open-source project:

- ComfyUI: https://github.com/comfyanonymous/ComfyUI

---

<div align="center">

**ModelFinder**: a Windows control center for ComfyUI environments.

</div>
