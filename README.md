# PCKB

Personal Code Knowledge Base

Turn the code you write, learn, and collect into a searchable personal knowledge base — with local or cloud AI.

[English](README.md) | [简体中文](README.zh-CN.md)

**Public Preview · macOS Apple Silicon · Active Development · Source code currently private**

PCKB is under active development. This repository is the public binary release repository; it does not contain the product's core source code.

## Download for macOS

**Recommended for new users:** [PCKB 0.4.0 Public Preview](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.4.0).

Download the macOS arm64 ZIP from that release.

System requirements: Apple Silicon Mac (arm64), macOS 11.0 or later.

This Public Preview is ad hoc signed. It is **not** signed with an Apple Developer ID and is **not** notarized by Apple. Verify the published SHA-256 before installing. See [INSTALL_MACOS.md](INSTALL_MACOS.md) for the normal macOS UI steps if first launch is blocked.

![PCKB Main Library and Code Detail](screenshots/public/01-main-library.png)

The images below are real PCKB screenshots from a synthetic demo library. Personal local paths are covered with opaque rectangles; no product controls or other content were changed.

## Features

- Personal code library with Projects, tags, favorites, learning status, and validation history
- Full-text and structured search
- Optional semantic search and related-code discovery
- Safe single-file import, recoverable Trash, and local backup/restore
- AI code actions and AI Chat
- Custom App backgrounds stored locally

## Screenshots

### Capture and organize

| Create a code asset | Manage a project |
| --- | --- |
| ![New asset editor](screenshots/public/02-new-asset.png) | ![Project management](screenshots/public/03-project-management.png) |

### Learn and review

| Learning overview | Asset learning cards |
| --- | --- |
| ![Learning Center overview](screenshots/public/04-learning-overview.png) | ![Learning Center asset cards](screenshots/public/05-learning-assets.png) |

### Configure and safeguard

| AI and semantic search settings | Backup and restore |
| --- | --- |
| ![AI and semantic search settings](screenshots/public/06-ai-settings.png) | ![Local backup and restore settings](screenshots/public/07-backup-restore.png) |

### Make it yours

![Local App background settings](screenshots/public/08-app-background.png)

The current demo has no generation model selected, so this preview does not include an AI Chat screenshot. AI Chat remains an available feature.

## AI options

- **Ollama:** optional local Generation and Embedding workflows
- **DeepSeek API:** optional BYOK Generation and AI Chat
- **Qwen API:** optional BYOK Generation, AI Chat, and Embedding
- Generation and Embedding providers are configured independently
- API credentials are stored using macOS Keychain
- There is no automatic cloud-provider fallback

Cloud AI operations send the content required for the user-requested operation to the selected provider. See [PRIVACY.md](PRIVACY.md).

The App includes the built-in PCKB night-lake background. You can choose a local image and adjust its overlay, blur, and Cover/Contain display mode; the background image remains on the Mac.

## Quick Start

1. Download the latest Public Preview ZIP.
2. Extract the ZIP.
3. Move `PCKB.app` to Applications.
4. Open PCKB and create or open a local library.

## Privacy

The library is primarily stored in ordinary files at a local folder selected by the user. Ollama supports local AI workflows. DeepSeek and Qwen are optional external BYOK providers. PCKB does not automatically fall back to another cloud provider.

## Documentation

- [macOS installation](INSTALL_MACOS.md)
- [User guide](USER_GUIDE.md)
- [Privacy](PRIVACY.md)
- [Security](SECURITY.md)
- [Source-code status](SOURCE_CODE_NOTICE.md)

## Legal

PCKB is distributed as proprietary freeware under the [PCKB EULA](legal/PCKB-EULA.txt). Downloading, installing, or using PCKB is subject to that EULA. Third-party open-source components remain subject to their own licenses. See the [Third-Party Notices](legal/THIRD-PARTY-NOTICES.txt), [component source references](legal/OPEN-SOURCE-COMPONENT-SOURCES.md), and [open-source license bundle](legal/OPEN-SOURCE-LICENSES/).

## Known limitations

- Apple Silicon (arm64) only; Intel Mac is not currently supported.
- No Apple Developer ID signature or Apple notarization.
- No cloud sync, automatic updates, folder batch import, Git/GitHub sync, VS Code extension, or code execution.
- Ollama models must be installed and managed separately. DeepSeek and Qwen require the user's own API key, network access, and service quota.
- This is an active-development Public Preview, not a stable or feature-complete release.

## Previous Releases

PCKB follows an iterative preview release model. Older versions remain available for rollback and historical reference.

- [v0.3.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.3.0) — AI Multi-Provider release
- [v0.2.2](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.2.2) — Feedback workflow update
- [v0.2.1](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.2.1) — Previous public release
- [v0.1.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.1.0) — Initial public release

For new installations, use [PCKB 0.4.0 Public Preview](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.4.0) unless you specifically need an older version.

## License

The PCKB application is not open source. Installation and use are governed by the [EULA](legal/PCKB-EULA.txt), which is also included with the download. Third-party notices are provided separately and do not reduce rights granted by third-party open-source licenses.
