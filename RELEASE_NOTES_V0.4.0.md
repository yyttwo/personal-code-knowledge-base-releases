# PCKB 0.4.0 Public Preview

First public preview release.

PCKB is under active development. This is an early public preview, not a stable or feature-complete release.

Downloading, installing, or using PCKB is subject to the [PCKB EULA](https://github.com/yyttwo/personal-code-knowledge-base-releases/blob/main/legal/PCKB-EULA.txt). Third-party components remain governed by their own licenses; see the [Third-Party Notices](https://github.com/yyttwo/personal-code-knowledge-base-releases/blob/main/legal/THIRD-PARTY-NOTICES.txt), [component source references](https://github.com/yyttwo/personal-code-knowledge-base-releases/blob/main/legal/OPEN-SOURCE-COMPONENT-SOURCES.md), and [open-source license bundle](https://github.com/yyttwo/personal-code-knowledge-base-releases/tree/main/legal/OPEN-SOURCE-LICENSES).

Download: `PCKB-0.4.0-Public-Preview-macOS-arm64.zip`

SHA-256: `5eb94c958958ce96f10c4cb9f5ec91ca3716602de90004b9eafd11d17006a4fc`

## Highlights

- Personal code library with Projects, tags, favorites, learning status, and validation history
- Full-text search, structured filtering, semantic search, and related-code discovery
- AI code actions and AI Chat
- Optional local Ollama support
- Optional DeepSeek and Qwen BYOK providers with API keys stored in macOS Keychain
- Local backup/restore and recoverable Trash
- Accepted visual redesign and custom local App backgrounds

## Privacy and provider behavior

- The library is primarily stored locally in a folder selected by the user.
- Generation and Embedding providers are configured independently.
- There is no automatic cloud-provider fallback.
- A cloud AI operation sends the content required for that user-requested operation to the selected provider.

## Known limitations

- Apple Silicon (arm64) and macOS 11.0 or later only.
- Ad hoc signed; no Apple Developer ID signature and no Apple notarization.
- If macOS blocks first launch, use Finder to Control-click or right-click `PCKB.app`, choose **Open**, then confirm. Do not disable macOS security protections.
- No cloud sync, automatic updates, folder batch import, Git/GitHub sync, VS Code extension, or code execution.
- Ollama models must be installed separately. DeepSeek and Qwen require the user's own API key, network access, and service quota.
- Active development: behavior and documentation may change in later previews.

Feedback and contributions to documentation and issue reports are welcome. The core source code is currently private.
