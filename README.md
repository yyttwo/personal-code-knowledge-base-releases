# 个人代码资产库

**v0.1.0 · Local-first macOS App**

个人代码资产库是一款面向个人的软件工程学习与复用工具。它把代码、用途、来源、验证记录和项目关系保存在你自己选择的本机文件夹中，帮助你收集、整理、搜索、理解和复用代码资产。

<p align="center">
  <img src="assets/app-icon.png" alt="个人代码资产库图标" width="192">
</p>

## 截图

公开截图将在后续使用完全虚构的演示代码库制作。

- Home / Library
- Asset Detail
- Search
- Project
- Single File Import
- Backup

## 核心功能

- 创建和编辑 Code Asset，记录标题、语言、类型、分类、说明、标签、来源与知识状态。
- 创建 Project，并把同一资产关联到多个 Project。
- 本地全文搜索、中文多关键词搜索、结构化筛选和 Project 内搜索。
- 从单个纯文本代码文件导入，自动预填标题、语言、代码和来源文件名。
- 保存前潜在 Secret Warning 和 Exact Duplicate 提示。
- 可恢复的废纸篓，以及明确确认后的永久删除。
- 本地版本化 Backup / Restore，恢复前校验并创建恢复副本。
- Local-first：普通文件是正式数据，SQLite 只作为可删除、可重建的搜索索引。

## 系统要求

- Apple Silicon Mac（arm64）
- macOS 11.0 或更高版本

Intel Mac 暂不保证支持。

## 下载与安装

前往 [v0.1.0 Release](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.1.0)（或 [Latest Release](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/latest)），下载 `个人代码资产库-v0.1.0-macos-arm64.zip` 和 `SHA256SUMS.txt`。

ZIP SHA-256：

```text
16c742ea1bef8d5adf3b35f3c4a8dd4feceeac2a8658875072e64dc20fa705ca
```

请在安装前核对完整性。详细步骤见 [INSTALL_MACOS.md](INSTALL_MACOS.md)。

当前版本没有 Developer ID 签名或 Apple 公证，macOS 可能显示“无法验证开发者”或等价提示。请只从你信任的正式发布页面下载，并使用 macOS Finder 或“系统设置”的官方打开流程。

## 数据与隐私

- 核心功能不要求网络、账号或云服务。
- 不包含 Telemetry、Analytics、AI、Cloud Sync 或用户代码执行。
- App 只围绕用户明确选择的代码库、导入文件和备份位置工作。
- 导入不修改、不删除、不执行或上传源文件。
- App 创建的本地备份不会被额外加密。

完整说明见 [PRIVACY.md](PRIVACY.md)。

公开反馈时，请勿在 GitHub Issue 中粘贴 API Key、Token、密码、私有代码或敏感 Library 内容。发现安全或隐私问题时，请先阅读 [SECURITY.md](SECURITY.md)。

## 数据归属

Library 是用户自己的数据，位于用户自行选择和管理的文件夹中。删除或替换 App 不会自动删除 Library。建议把 Library 和备份放在容易找到、权限合适并纳入个人备份计划的位置。

## 已知限制

v0.1 不包含 AI、Semantic Search、Cloud Sync、Folder Batch Import、Git Import、GitHub Sync、VS Code Extension、Auto Update 或 Intel 支持保证。

当前发布采用个人本地安装方式，不提供 Mac App Store 版本，也没有 Developer ID 签名或 Apple 公证。

## 源代码状态

当前不公开核心源代码。本公开仓库仅用于产品说明、用户文档和正式下载，不代表开源发布。Source code is not currently distributed.

详见 [SOURCE_CODE_NOTICE.md](SOURCE_CODE_NOTICE.md)。
