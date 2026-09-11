# 个人代码资产库

一个 Local-first 的 macOS 个人代码资产管理工具，用于收集、整理、搜索和复用自己的代码。

## [⬇️ 下载 v0.1.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.1.0)

**当前版本：** v0.1.0 · **系统要求：** Apple Silicon Mac / macOS 11.0+

<p align="center">
  <img src="assets/app-icon.png" alt="个人代码资产库图标" width="160">
</p>

![个人代码资产库主界面](assets/screenshots/01-library.png)

## 核心功能

- 管理代码资产的标题、语言、类型、分类、说明、标签、来源和知识状态。
- 使用 Project 组织资产，同一份资产可以关联多个 Project。
- 本地全文搜索、中文多关键词搜索、结构化筛选和 Project 内搜索。
- 从单个纯文本代码文件导入，自动预填标题、语言、代码和来源文件名。
- 保存前提供潜在 Secret Warning 和 Exact Duplicate 提示。
- 使用可恢复的废纸篓，并在永久删除前再次确认。
- 创建本地版本化 Backup；Restore 前校验备份并创建恢复副本。
- 普通文件保存正式数据，SQLite 只作为可删除、可重建的搜索索引。

## 界面预览

| 代码资产详情 | 全文搜索 |
| --- | --- |
| ![代码资产详情](assets/screenshots/02-asset-detail.png) | ![全文搜索](assets/screenshots/03-search.png) |

| Project 管理 | 单文件导入 |
| --- | --- |
| ![Project 管理](assets/screenshots/04-project.png) | ![单文件导入](assets/screenshots/05-import.png) |

| 本地备份与恢复 |
| --- |
| ![本地备份与恢复](assets/screenshots/06-backup.png) |

所有截图均使用完全虚构的本地演示数据制作。

## 隐私

- 核心功能不需要网络、账号或云服务。
- 不上传代码，不包含 Telemetry、Analytics、AI 或 Cloud Sync。
- 不执行保存或导入的代码。
- Library 存储在用户明确选择的本地目录中。
- App 只围绕用户选择的 Library、单个导入文件和备份位置工作。

完整说明见 [PRIVACY.md](PRIVACY.md)。

## 下载与安装

从 [v0.1.0 Release](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.1.0) 下载：

- `个人代码资产库-v0.1.0-macos-arm64.zip`
- `SHA256SUMS.txt`

ZIP SHA-256：

```text
16c742ea1bef8d5adf3b35f3c4a8dd4feceeac2a8658875072e64dc20fa705ca
```

请在安装前核对完整性。完整安装步骤见 [INSTALL_MACOS.md](INSTALL_MACOS.md)。

当前版本未使用 Apple Developer ID 签名和公证。macOS 可能提示无法验证开发者；请只从本仓库的正式 Release 页面下载。若系统阻止首次启动，请在 Finder 中按住 Control 点击 App 并选择“打开”，或前往“系统设置”→“隐私与安全性”使用系统提供的“仍要打开”选项。

## 系统要求

- Apple Silicon Mac（arm64）
- macOS 11.0 或更高版本

Intel Mac 暂不保证支持。

## 数据归属

Library 是用户自己的数据，位于用户自行选择和管理的文件夹中。删除或替换 App 不会自动删除 Library。建议把 Library 和备份放在容易找到、权限合适并纳入个人备份计划的位置。

## 已知限制

v0.1 不包含 AI、Semantic Search、Cloud Sync、Folder Batch Import、Git Import、GitHub Sync、VS Code Extension、Auto Update 或 Intel 支持保证。

当前发布采用个人本地安装方式，不提供 Mac App Store 版本，也没有 Developer ID 签名或 Apple 公证。

## 源代码状态

当前不公开核心源代码，本仓库仅用于产品说明、使用文档和正式版本下载。

Core source code is not currently distributed. This repository contains product information, user documentation, and official release downloads.

详见 [SOURCE_CODE_NOTICE.md](SOURCE_CODE_NOTICE.md)。

## 安全反馈

公开反馈时，请勿在 GitHub Issue 中粘贴 API Key、Token、密码、私有代码或敏感 Library 内容。发现安全或隐私问题时，请先阅读 [SECURITY.md](SECURITY.md)。
