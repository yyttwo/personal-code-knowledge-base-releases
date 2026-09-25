# PCKB 0.5.0 Public Preview

PCKB 0.5.0 是首个完整支持简体中文与 English 的公开预览版本。

下载、安装或使用 PCKB 受 [PCKB EULA](https://github.com/yyttwo/personal-code-knowledge-base-releases/blob/main/legal/PCKB-EULA.txt) 约束。第三方组件继续适用各自许可证；详见[第三方声明](https://github.com/yyttwo/personal-code-knowledge-base-releases/blob/main/legal/THIRD-PARTY-NOTICES.txt)、[组件源码出处](https://github.com/yyttwo/personal-code-knowledge-base-releases/blob/main/legal/OPEN-SOURCE-COMPONENT-SOURCES.md)与[开源许可证文本](https://github.com/yyttwo/personal-code-knowledge-base-releases/tree/main/legal/OPEN-SOURCE-LICENSES)。

下载文件：`PCKB-0.5.0-Public-Preview-macOS-arm64.zip`

SHA-256：`7256b2ee8bb5a967f146e3bd894a341c9d6513835b2505490f5c2ead486f1ca7`

## 主要更新

- 新增完整简体中文 / English 双语界面
- 支持跟随系统语言，也可在 App 内即时切换语言
- AI Actions 根据当前界面语言选择默认回复语言；用户明确指定其他语言时仍尊重用户要求
- 用户代码、Project、Tag、Notes 与其他正式数据不会因切换语言而改变
- 保持现有 Local-first 数据边界与本地备份/恢复能力
- 保持 Ollama、DeepSeek 与 Qwen 可选 AI 支持
- 保持全文搜索、语义搜索、Hybrid Search 与 Related Code

## 兼容性

- Apple Silicon（arm64）
- macOS 11.0 或更高版本
- 可直接打开现有 0.4.x 代码库，不要求数据库或代码库迁移

## 已知限制

- 当前仍为 Public Preview，不是稳定版或功能完整版本
- 使用 ad hoc 签名，没有 Apple Developer ID 签名，也没有 Apple 公证
- 不提供自动更新
- 当前核心源代码保持私有
- Ollama 模型需要用户自行安装；DeepSeek 与 Qwen 需要用户自己的 API Key、网络连接及服务额度

## English Summary

PCKB 0.5.0 is the first Public Preview with complete Simplified Chinese and English interfaces. It supports System language selection and instant in-app switching while keeping user code, Projects, tags, notes, provider settings, and local data unchanged. Existing 0.4.x libraries remain compatible without migration.

This release remains an Apple Silicon Public Preview for macOS 11.0 or later. It is ad hoc signed, is not signed with an Apple Developer ID, is not notarized by Apple, and does not include automatic updates. The core source code is currently private.
