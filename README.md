🌐 **English** | [简体中文](README_CN.md)

<div align="center">

# ModelFinder for ComfyUI on Windows

### Deploy, launch, manage, and repair ComfyUI from one desktop app.

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=Latest%20Release)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.cumulative_downloads&style=for-the-badge&logo=github&label=Downloads)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

[**Download**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**All Releases**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**Report Issues**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

</div>

---

## What ModelFinder Is

ModelFinder is a Windows desktop launcher and manager for the ComfyUI ecosystem.

It is built for the messy parts around ComfyUI:

- deploying a fresh environment
- managing multiple ComfyUI installs
- checking Python / PyTorch / dependency state
- installing custom nodes and their dependencies
- scanning workflows for missing assets
- downloading models from supported sources
- diagnosing launch and environment failures

The goal is simple: spend less time fixing setup and more time running workflows.

---

## Core Capabilities

| Area | What it does |
|------|---------------|
| **Home** | Start and stop ComfyUI, view live logs, open the built-in workspace, inspect basic hardware and runtime status |
| **Environments** | Deploy ComfyUI, manage multiple installs, switch ComfyUI / PyTorch variants, install `.txt` and `.whl` dependencies |
| **Workflows** | Analyze workflow files, detect missing models, and resolve downloadable candidates from supported catalogs |
| **Plugins** | Install custom nodes from Git URLs, manage plugin dependencies, bulk enable or disable plugins |
| **Models** | Browse local model libraries, detect duplicates across packages, and manage downloads |
| **AI Assistant** | Diagnose logs, explain failures, and execute approved repair actions inside the launcher |
| **Downloads** | Queue, track, pause, resume, and manage model downloads |

---

## AI Assistant

The AI Assistant is integrated into the desktop app as a chat panel.

What it can do today:

- inspect launcher-collected logs and environment state
- explain startup failures and dependency errors
- suggest repair actions
- execute launcher-native repair tools after your approval
- continue multi-step repair flows inside the same conversation

Important boundaries:

- AI features require sign-in
- usage is credit-based and managed server-side
- current billing and pricing rules live on the official website, not in this release repo

---

## Quick Start

### First Launch

1. Download the latest **Setup Installer** or **Portable ZIP** from [Releases](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
2. Start ModelFinder
3. Either deploy a new ComfyUI environment or add an existing one
4. Click **Start** on the Home page to launch ComfyUI

> [!TIP]
> Python and .NET do not need to be installed separately for normal use.

### Existing Installs

ModelFinder can work with:

- existing ComfyUI portable folders
- multiple side-by-side ComfyUI installs
- ComfyUI Desktop environments imported through your `Documents\\ComfyUI` folder

ModelFinder is meant to manage and inspect these environments, not overwrite them blindly.

---

## Current Product Notes

- **Platform**: Windows 10 / 11
- **Release type**: this repository publishes public Windows builds
- **Prereleases**: if beta or prerelease builds are available, they will be explicitly marked in GitHub Releases
- **Cloud-backed features**: AI Assistant and some workflow matching capabilities rely on sign-in and server-side services

---

## FAQ

<details>
<summary><b>Do I need to install Python first?</b></summary>

No. For standard use, ModelFinder manages the ComfyUI Python environment for you.

</details>

<details>
<summary><b>Can it manage my existing ComfyUI install?</b></summary>

Yes. You can add an existing ComfyUI folder and let ModelFinder manage it alongside new environments.

</details>

<details>
<summary><b>Does it support custom nodes?</b></summary>

Yes. You can install custom nodes from Git URLs and manage their Python dependencies from inside the app.

</details>

<details>
<summary><b>Does the AI Assistant run actions automatically?</b></summary>

It can execute supported repair tools, but only after approval for write or repair actions.

</details>

<details>
<summary><b>Is macOS or Linux supported?</b></summary>

Not currently. This release repository is for Windows builds.

</details>

---

## About This Repository

This repository hosts:

- compiled Windows releases
- release notes and release history
- issue tracking for public builds

ModelFinder itself is a closed-source desktop product built around the ComfyUI ecosystem.

ComfyUI is an independent open-source project:

- ComfyUI: https://github.com/comfyanonymous/ComfyUI

---

<div align="center">

**ModelFinder** — a Windows control center for ComfyUI environments.

</div>
