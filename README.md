# TCode Desktop

**Open the desktop. Move every task forward.**

A graphical AI coding agent for Windows. Manage tasks in a workspace you can see, watch the agent work, and let it understand your codebase, make changes, and verify the result — while you stay in control of every engineering change.

**[Download the latest release →](../../releases/latest)**

`Windows x64` · `Desktop GUI` · `International edition`

---

## Not just code completion — the whole task

From reading context, to editing files, to running commands and checking the outcome, TCode puts the entire coding workflow into one desktop workspace.

### 01 — Task-level coding

Understands project structure and code context, then implements, refactors, and fixes defects across files, verifying the result with real commands.

```
read → plan → edit → run → verify → deliver
```

### 02 — Models and providers

Works with mainstream model services and OpenAI-compatible endpoints, so the team can choose the model and context capabilities that fit its environment.

### 03 — Desktop workspace

Designed for GUI use: task list, execution progress, and file changes in one place — no command memorization required to get started.

### 04 — Observable tool execution

File edits, shell commands, and external tool calls stay visible, and sensitive operations ask for confirmation before proceeding.

```
permission: explicit    execution: observable
```

---

## Install

1. Open the [latest release](../../releases/latest) and download
   `TCode-desktop-international-<version>-win-x64.exe`.
2. Run the installer and follow the prompts.
3. If Windows SmartScreen shows a warning, choose **More info** → **Run anyway**.
4. Launch TCode and pick the repository you want to work in.
5. Describe the task and let the agent read, plan, edit, and verify.

## Upgrade

Download the installer from a newer release and run it. Your settings and projects are kept.

## Verify a download

Every release asset lists its SHA-256 digest on GitHub. To check a file you downloaded:

```powershell
Get-FileHash .\TCode-desktop-international-<version>-win-x64.exe -Algorithm SHA256
```

Compare the output with the digest shown on the release page.

## About this repository

- This repository hosts **installers only**. It contains no source code.
- These are the **international edition** builds, which do not include the Token Manager.
- Only Windows x64 is published here.

## Requirements

- Windows 10 or later, 64-bit
- An internet connection for model access
