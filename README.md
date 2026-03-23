🌐 **English** | [简体中文](README_CN.md)


<div align="center">

# ModelFinder

### Run ComfyUI workflows faster on Windows

**Batch workflow analysis · Missing resource downloads · Accelerated download workflows**

[![GitHub Release](https://img.shields.io/github/v/release/hu-haibin/ModelFinder-Releases?style=for-the-badge&logo=github&label=Latest%20Release)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)
[![Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhu-haibin%2FModelFinder-Releases%2Fmain%2Fstats%2Fdownloads.json&query=%24.cumulative_downloads&style=for-the-badge&logo=github&label=Downloads)](https://github.com/hu-haibin/ModelFinder-Releases/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=for-the-badge&logo=windows)](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest)

> Persistent cumulative downloads are refreshed every 15 minutes. Removing older releases later will not retroactively lower the recorded total.

[**Stable Community Build**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest) · [**Beta / Early Access**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**Release Notes**](https://github.com/hu-haibin/ModelFinder-Releases/releases) · [**Report Issues**](https://github.com/hu-haibin/ModelFinder-Releases/issues)

---

</div>

![ModelFinder English interface - light theme home screen](screenshots/light-theme-english.png)

## What It Solves

ModelFinder is a Windows launcher and workflow operations tool for **ComfyUI** users who need to move faster from workflow import to runnable output. It is built to help you batch-check workflows, find missing models and related resources, and complete large download flows without turning setup into manual cleanup work.

> Instead of opening workflows one by one, chasing missing files manually, and juggling multiple ComfyUI environments by hand, you get one place to analyze, download, and launch.

---

## Release Paths

| Track | Access | Release Type | Recommended For |
|------|--------|--------------|-----------------|
| **Stable Community Build** | Free | Standard GitHub release | Most users who want the recommended public build |
| **Pro / Beta Early Access** | Paid beta | GitHub prerelease | Paid testers and power users who want earlier workflow tooling and faster iteration |

### What Pro / Beta Currently Unlocks

- **Batch workflow analysis** across multiple files and folders
- **One-click download of missing resources**, including models and selected dependency-linked files
- **Accelerated download workflows** for large fetch queues and repeated setup work
- **Selected advanced automation features in active testing**, including higher-end workflow tooling and AI-assisted diagnosis

### Beta Access

ModelFinder keeps a free community path, but this repository also hosts a **paid beta track** for early adopters.

- **Stable Community Build** remains the default recommendation for general users
- **Pro / Beta Early Access** is for licensed testers who want earlier access to advanced workflow tooling and faster release cadence
- Beta builds may ship unfinished features, UI changes, or temporary regressions before they are promoted to stable
- Stable and beta builds are published from the same repository so downloads, release history, and upgrade paths stay unified

Who should join: users who regularly deal with missing models, batch-check workflow folders, maintain multiple ComfyUI environments, or want early access to bulk analysis, missing-resource downloads, and advanced automation features.

---

## What You Can Do

### One-click ComfyUI Deployment

No manual Python environment setup required. Deploy from zero to runnable in just a few clicks:

- **Version selection**: choose from official ComfyUI releases and download automatically
- **GPU acceleration options**: NVIDIA default / CUDA 12.6 / CUDA 12.8 (recommended) / AMD ROCm
- **Optional preinstalled components**: ComfyUI-Manager, DD Translation, KJ Nodes, WAN Video Wrapper, and more
- **Visual installation progress**: step-by-step progress (download -> extract -> install components)
- **Failure recovery**: switch mirrors, import local packages, or skip failed steps
- **One-click launch after deployment**: start ComfyUI immediately when setup completes

![Quick deployment - choose version, GPU acceleration, and optional components](screenshots/deployment.png)

![Deployment completed - all steps succeeded, one-click launch](screenshots/deployment-progress.png)

---

### Home: Console + Floating Action Island

The core launcher page with game-launcher-inspired interaction:

- **Full-size terminal console**: real-time ComfyUI logs with macOS-style decoration bar (red/yellow/green dots), copy/clear supported
- **Bottom-right floating action island**: start/stop ComfyUI, open Web UI, switch instance
- **Launch parameter configuration**: set port, GPU memory mode (High/Normal), and custom startup arguments
- **Quick folder access**: open models / output / custom_nodes / workflows and Python terminal from bottom toolbar
- **Automatic environment checks**: validates Python, GPU, and runtime prerequisites before launch

![ModelFinder main interface - dark theme, terminal console + floating action island](screenshots/home.png)

---

### AI Diagnosis

When ComfyUI fails to start or behaves abnormally, the AI assistant helps diagnose and repair:

- **One-click log analysis**: send recent console logs for diagnosis
- **Auto-generated repair plan**: returns concrete repair commands (pip, git, etc.)
- **Execution with approval**: commands require user approval; high-risk actions require extra confirmation
- **Post-repair verification**: can restart ComfyUI automatically and verify results
- **One-click rollback**: rollback changes if repair quality is unsatisfactory
- **Multiple AI providers supported**: configure API key and endpoint in AI Settings

![AI diagnosis - analyze logs, generate repair plan, execute with one click](screenshots/ai-diagnosis.png)

![AI settings - provider, API key, and connection test](screenshots/ai-settings.png)

---

### Model Finder - Smart Model Matching

A key differentiator: load a workflow, detect missing models, and match download sources automatically.

- **Load workflow by drag-and-drop or file picker**: supports JSON / PNG ComfyUI workflows
- **Scan existing local models**: detect "already installed" vs "missing"
- **Automatic multi-source matching**: built-in model catalog (1000+ entries), including HuggingFace / HuggingFace Mirror / ModelScope
- **Online search fallback**: Civitai / HuggingFace / Bing search for unmatched models
- **Single or batch actions**: accept candidate / reject candidate / download one / download all matched
- **Batch analysis**: analyze multiple workflow files or entire folders
- **Export results**: CSV / JSON output for sharing and records

![Model Finder - start by dragging or selecting workflow files](screenshots/model-finder-empty.png)

![Model Finder - auto-matched model sources after workflow load](screenshots/model-finder.png)

---

### Dependency Analysis (Workflow Plugin Analysis)

Analyze custom node dependencies required by workflows:

- **Plugin dependency detection**: list installed and missing custom nodes
- **One-click installation for missing plugins**: auto install with Git clone
- **Automatic Python dependency install**: runs pip install for requirements
- **Batch analysis**: supports multiple files or whole folders

![Dependency analysis - detect missing plugins and install with one click](screenshots/dependency-analysis.png)

---

### Package / Instance Management

Manage multiple ComfyUI environments (portable packages):

- **Take over existing portable packages**: add existing ComfyUI directories without modifying original files
- **Version overview**: Python version (with env type), PyTorch version, ComfyUI version, plugin count, disk usage
- **Set default instance**: choose which package launches by default on Home
- **PyTorch version manager**: switch among versions (CUDA 11.8 / 12.1 / 12.6 / 12.8, etc.)
- **ComfyUI core upgrade**: view version list, upgrade or rollback
- **Environment export/import**: export `pip freeze`, import to restore
- **Terminal tools**: open Python terminal, run pip list / install / uninstall / show
- **pip cache cleanup**: free pip download cache

![Package manager - multi-instance management with complete environment info](screenshots/package-manager.png)

![PyTorch version manager - visual switch for PyTorch/CUDA versions](screenshots/pytorch-manager.png)

---

### Plugin Management

Dedicated page for installed custom nodes:

- **Automatic scanning**: discover plugin name, Git remote URL, size, and more
- **Search and filter**: quickly locate plugins by name
- **Plugin actions**: open folder / open GitHub page / delete plugin
- **Version switching**: browse commit history and switch to a target commit
- **Rollback**: return to previous Git commit
- **Dependency management**: detect and install Python dependencies

![Plugin management - clear list, version switching, and dependency management](screenshots/plugin-management.png)

---

### Hardware Monitor

Real-time system and network visibility:

- **Hardware details**: OS version, CPU, RAM, GPU and VRAM, motherboard
- **Disk usage**: partition capacity / used / free with progress bars
- **Network verification**: built-in multi-node speed test (HuggingFace / ModelScope / GitHub / Civitai, etc.)
- **Config report**: copy complete hardware + network report to clipboard

![Hardware monitor - hardware overview, disk usage, and network speed tests](screenshots/hardware-monitor.png)

---

### Batch Queue

Automate large-scale generation through ComfyUI API:

- **Load workflow JSON**
- **Parameter replacement**: set target node ID and field, supports batch prompt replacement from files
- **Repeat count / random seed**
- **Auto-restart interval**: avoid long-run memory leaks
- **Custom output directory**
- **Resume from interruption**

![Batch queue - load workflow, configure parameters, run automated batch generation](screenshots/batch-queue.png)

---

### Model Management

Visual browsing and management for local model files:

- **Model scanning**
- **Search and filtering**: by filename and type (checkpoint / lora / vae, etc.)
- **Metadata overview**: filename, type, size
- **Quick actions**: open folder, delete model

![Model management - model library browsing, search, and category filtering](screenshots/model-management.png)

---

### Download Center

Unified download task management:

- **Live progress**: speed, downloaded size, remaining time, completion percent
- **Task control**: pause / resume / cancel
- **Batch cleanup**: clear completed tasks
- **Path details**: inspect download destination paths

![Download center - unified task management with real-time progress and controls](screenshots/download-center.png)

---

### Settings

Comprehensive personalization options:

- **Language**: Simplified Chinese / English / Follow system
- **Theme**: dark / light
- **Color schemes**: multiple accent palettes (for example Ocean Blue)
- **UI density**: comfortable / compact
- **Reduced motion**: disable transition animations on low-end devices
- **Sidebar startup state**: default expanded or collapsed

![Settings - language, theme, color scheme, density, and more](screenshots/settings.png)

---

## User Interface

ModelFinder follows **Windows Fluent Design** to provide a modern and immersive experience:

- **Dark/light theme** tuned for long-session usability
- **Smooth animations** for transitions and interactions (optional)
- **Adjustable density** for different screen sizes
- **Bilingual switching** in real time (Chinese / English)
- **Game-launcher-style interaction** with floating action island and terminal chrome
- **Collapsible sidebar** with 12 navigation entries

![About Author - collapsed sidebar mode + light theme](screenshots/about-author.png)

---

## System Requirements

| Item | Requirement |
|------|-------------|
| **OS** | Windows 10 (22H2+) / Windows 11 |
| **Runtime** | No extra installation required (bundled) |
| **Disk Space** | Launcher itself ~100 MB |
| **GPU** | NVIDIA (CUDA) or AMD (ROCm) recommended for ComfyUI workloads |

> ModelFinder is a launcher/manager. Actual runtime requirements depend on your selected models and workflows.

---

## Installation and Usage

### Download and Run

Stable community users can download the latest recommended build from [**latest release**](https://github.com/hu-haibin/ModelFinder-Releases/releases/latest).
Early access users can use licensed **prerelease** builds published on the same [**Releases**](https://github.com/hu-haibin/ModelFinder-Releases/releases) page.

| Option | File | Notes |
|--------|------|-------|
| **Setup Installer** | `ModelFinderLauncher-Setup-vX.X.X.exe` | Recommended — standard install/uninstall, Start Menu shortcut |
| **Portable ZIP** | `ModelFinderLauncher-win-x64-portable-vX.X.X.zip` | No install needed — extract anywhere and run `ModelFinder.exe` |

> Both options are self-contained — no Python or .NET installation required.

### Quick Start

```text
First launch -> Use deployment wizard to install ComfyUI (version/GPU/components)
             -> Or add your existing ComfyUI portable package in Package Manager

Home         -> Click Start -> Watch real-time logs -> Open Web UI when Ready

Model Finder -> Drop workflow -> Detect missing models -> Confirm matches -> Download all

Dependency Analysis -> Load workflow -> Detect missing plugins -> One-click install

Batch Queue   -> Load workflow -> Configure parameters -> Start batch generation
```

---

## Upgrading from Older Versions

If you previously used **ComfyLauncher** (v1.3.x and older):

- ModelFinder will **automatically migrate** your config (`%AppData%/ComfyLauncher` -> `%AppData%/ModelFinder`)
- Both executable names are recognized (`ComfyLauncher.exe` / `ModelFinder.exe`) for seamless transition
- A branding-change notice is shown when launching from old entry points for the first time

---

## FAQ

<details>
<summary><b>Q: What is the difference between ModelFinder and HuiShi Launcher?</b></summary>

Both are excellent ComfyUI launcher tools, but they focus on different strengths:

- **Model Finder capability**: automatic workflow parsing and missing-model source matching (HuggingFace / ModelScope / Civitai)
- **AI diagnosis**: auto analyze startup failures and generate/execute repair commands
- **Batch Queue**: automate repeated workflow execution via ComfyUI API
- **PyTorch version management**: visual switching for PyTorch/CUDA versions
- **UI style**: Windows Fluent dark-theme-first, game-launcher-like interaction

</details>

<details>
<summary><b>Q: Do I need to install Python or .NET separately?</b></summary>

No. ModelFinder is portable and ships with required dependencies. ComfyUI Python setup is handled by the deployment wizard.

</details>

<details>
<summary><b>Q: Can it manage my existing ComfyUI portable package?</b></summary>

Yes. In Package Manager, click "Add Directory" and select your existing ComfyUI root folder. Existing files are not modified.

</details>

<details>
<summary><b>Q: Is AMD GPU supported?</b></summary>

Yes. You can choose AMD ROCm during deployment, and existing AMD environments can also be imported.

</details>

<details>
<summary><b>Q: How do I use AI diagnosis? Is extra setup required?</b></summary>

Configure API key and endpoint in AI Settings (multiple providers supported). Then use the AI diagnosis entry from Home when startup fails.

</details>

<details>
<summary><b>Q: Is macOS or Linux supported?</b></summary>

Currently only **Windows 10/11** is supported.

</details>

<details>
<summary><b>Q: Is ModelFinder free, paid, or both?</b></summary>

ModelFinder now has two release tracks in this repository:

- **Stable Community Build** is the free public path
- **Pro / Beta Early Access** is a paid beta path for licensed testers

If you want the general public build, use stable. If you want earlier access and accept beta risk, use the beta track.

</details>

---

## Feedback

- **Bug reports / feature requests**: open an issue in [Issues](https://github.com/hu-haibin/ModelFinder-Releases/issues)
- If ModelFinder helps you, a star is highly appreciated

---

## License and Notice

ModelFinder is closed-source software. This repository provides compiled release binaries only.
ModelFinder is not officially affiliated with ComfyUI. ComfyUI is an independent open-source project.

---


<div align="center">

**ModelFinder** - Turn ComfyUI from setup friction into out-of-box productivity.

Made with ❤️ for the AI Art Community

</div>


