# TCode Desktop — Early Preview

<p align="center">
  <img src="assets/banner.png" alt="TCode Desktop" width="820">
</p>

> **This is an early test build, not a finished product.** We're sharing it with a small group of developers to find out what breaks, what's confusing, and what actually helps. If you try it, please tell us — see [How to give feedback](#how-to-give-feedback).

**TCode is a graphical AI coding agent for Windows.** It takes on whole engineering tasks instead of suggesting the next line: it reads your project, plans a change, edits across files, runs commands, and checks the result. This is an early test build, and we put it out now because real codebases tell us things a demo never will — which is exactly why we're here.

<p align="center">
  <a href="../../releases/latest"><img src="https://img.shields.io/badge/Download-Latest%20Release-2ea44f?style=for-the-badge" alt="Download"></a>
</p>

<p align="center">
  <code>Windows x64</code> · <code>Desktop GUI</code> · <code>Free to download during the preview</code>
</p>

<p align="center">
  <img src="assets/desktop-home.png" alt="TCode Desktop home screen" width="900">
</p>

<!-- Optional later: a 30s screen recording showing cross-file bug location → edit → running tests. No marketing intro, just the work. -->

---

## What's in this build

We kept this section short on purpose — the useful way to understand TCode is to run it on a real task. A few things worth knowing before you start:

- **Task-level agent, not autocomplete.** Reads your project, plans a change across files, edits, runs commands, and verifies the outcome.
- **Everything stays visible.** File diffs, terminal activity, tool calls and progress live in one workspace. Sensitive operations ask for permission first (`allow once` / `always` / `deny`).
- **Bring your own model.** Configure a provider in Settings → Providers: a long list of model services, OpenAI-compatible endpoints, plus API-key and OAuth sign-in.
- **Works with GitHub and MCP.** A built-in read-only GitHub MCP Server can look at repos, issues, PRs and Actions; connectors include design tools like Figma.
- **Offline voice input.** Speech-to-text runs locally on your machine (models download on first use) — no audio leaves the device.
- **Extensible.** Skills, plugins, agents, scheduled tasks and an inbox are part of the app, alongside multiple UI languages.

---

## What we're looking for

We'd rather hear one concrete problem than ten compliments. Especially useful:

- Tasks where TCode **failed** or produced a wrong fix — the repo, the prompt, and what you expected
- Cross-file changes, legacy codebases, and unfamiliar project structures
- Model setup friction (providers, API keys, OpenAI-compatible endpoints)
- Windows-specific issues: install, SmartScreen, permissions, paths, encodings
- Anything in the UI that made you hesitate or guess

You don't need to write a polished report. A screenshot, a short description and your version number is plenty.

---

## Install

1. Download the latest test build from **[Releases](https://github.com/bjyiyuan/tcode-desktop-releases/releases/latest)** — pick the Windows x64 `.exe` of the newest version.
2. Run the installer. If Windows SmartScreen warns, choose **More info → Run anyway**.
3. Launch TCode, open the repository you want to work in, and connect a model in **Settings → Providers**.
4. Describe a task and watch it read → plan → edit → run → verify.

**Requirements:** Windows 10 or later (64-bit) · internet connection for model access · a model provider configured in Settings → Providers (your own API key or a supported account sign-in).

### Verify your download

Every release lists the SHA-256 digest of the installer:

```powershell
Get-FileHash .\<downloaded-file>.exe -Algorithm SHA256
```

Compare it with the digest shown next to the file on the release page.

---

## Try this first

Not sure what to throw at it? These three tasks tend to tell us the most:

1. **Fix a failing test** in a small open-source repo — let TCode find the cause, then check whether it edited the right file.
2. **Make sense of an unfamiliar module** — open a repo you've never seen and ask what a specific part does and where to start.
3. **Add a small feature** with a clear acceptance criterion (a CLI flag, an extra field), then read the diff yourself.

A task that touches more than one file is worth ten that don't. And if something goes wrong, that's exactly the report we want.

---

## How to give feedback

**Please use GitHub Issues** — it's the channel we read first during this preview, and it's public, so other testers can confirm what you're seeing.

- **[Open a feedback issue](https://github.com/bjyiyuan/tcode-desktop-releases/issues/new/choose)** — a short form, takes about a minute
- Found a reproducible bug? Use the **Bug report** template instead
- A screenshot, a short description and your version number is plenty — rough notes are fine

> The in-app feedback dialog is not wired up in this build, so please don't rely on it.

**What we commit to:** every report gets a first response within one business day, and we'll tell you within two business days whether it's being fixed and in which version. Fixes are listed in the release notes with the issue number, so you can see what your report changed.

---

## Known limitations (we know, we're working on it)

- Windows only for now; macOS and Linux are not supported in this preview
- Model access depends on how you configure it in Settings → Providers; most configurations require an API key or an account sign-in
- The in-app feedback dialog may not deliver in this build — please use GitHub Issues instead
- Large repositories and very long tasks may be slow or hit context limits
- SmartScreen may warn because the installer is not yet signed by a widely trusted certificate
- The interface and wording are still rough — this is a test build
- Automatic updates are not available in this build — download each new version from Releases instead of waiting for an in-app update
- You may still see billing- or credits-related wording in Settings left over from an earlier build; it does not apply during this preview
- Offline voice input needs a one-time download of its speech model on first use; on some networks that download can fail

---

## Data & privacy

**What we collect.** Anonymous usage metadata only: app version, operating system, event names, session and turn identifiers, model provider and model names, task durations, and error categories. Never your prompts, your code, file contents, repository paths, or model responses.

**What we don't do.** We don't use your code or prompts for training, and we don't sell or share this data.

**Where your code goes.** Straight to the model provider you configure in Settings → Providers, over that provider's own connection. We don't relay or store it. Model costs are set by that provider.

**Two separate uploads, and we say so.**

| Upload | What it contains | Can you turn it off? |
|-|-|-|
| Usage statistics | The event metadata described above | Yes — at first launch, and later in **Settings → Usage statistics** |
| Install count | A random installation ID, app version, OS, and install source | No — sent once per install, independent of that switch |

Turning usage statistics off stops any upload in progress and clears the local queue. It does not delete statistics already received by our server.

**Deleting data that was already sent.** Open a [privacy request](https://github.com/bjyiyuan/tcode-desktop-releases/issues/new/choose) and include the installation ID shown in **Settings → Usage statistics**. We remove the associated statistics within 30 days and confirm when it's done.

**Retention.** Raw usage events are kept for 12 months, then deleted or reduced to aggregate counts that carry no installation identifier.

**Age.** This preview is intended for users who are 18 or older, or the age of majority in their jurisdiction.

**Changes.** If this policy changes in a material way, we'll say so in the release notes and in the in-app announcement.

---

## FAQ

**Is it free?**
The desktop app is free to download during this preview. Model access is configured by you in Settings → Providers — bring your own API key or sign in with a supported account. Any model costs are set by that provider, not by us. We're still working out the billing details for this build; the in-app Settings are the source of truth.

**Where does my code go?**
Your code and prompts go to the model provider **you** configure, not to us, and are never used for training. Separately, TCode collects anonymous usage metadata and sends a one-time install count. Both are described in **[Data & privacy](#data--privacy)** — what's collected, how to turn it off, and how to have data already sent deleted. This repository contains installers only, no application source.

**Is the source code available?**
No. This repository distributes Windows installers only. The `Source code (zip)` / `Source code (tar.gz)` entries that GitHub adds to every release are snapshots of this download page, not the application. Use the `.exe` installer.

**Who's behind this?**
A small team building TCode. We're running this preview ourselves and reading every report.

**Will there be a stable release?**
That depends on what we learn here. We're not making promises until the preview tells us what to fix.

---

## About this repository

This repository is the download page for the TCode Desktop early preview. It hosts Windows installers only. Releases include SHA-256 digests so you can verify what you downloaded.

**License / terms:** the installer is proprietary software, distributed as a binary for evaluation. No source code is licensed or granted here. See [NOTICE.md](NOTICE.md).
