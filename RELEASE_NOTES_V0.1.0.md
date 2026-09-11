# 个人代码资产库 v0.1 发布说明

## 下载提示

- 适用于 Apple Silicon Mac，要求 macOS 11.0 或更高版本。
- 当前没有 Developer ID 签名，也没有 Apple 公证；首次打开时 macOS 可能要求额外确认。
- Local-first：核心功能不需要网络，不包含 Telemetry。

## 版本信息

- 版本：`0.1.0`
- Build：`1`
- 平台：Apple Silicon Mac，macOS 11.0+
- 发布方式：个人本地安装

## 主要能力

- Local-first 代码资产库，以普通文件长期持有数据。
- 创建、编辑、分类、标记和理解 Code Asset。
- 本地全文搜索、多关键词搜索、结构化筛选和 Project 内搜索。
- Project 组织、多 Project 关联、状态与只读完成复盘。
- 安全的单文件纯文本代码导入。
- 保存前潜在 Secret 警告和 Exact Duplicate 保护。
- 可恢复废纸篓和明确确认的永久删除。
- 本地版本化备份、完整性校验、恢复副本与安全恢复。
- 可删除并重建的 SQLite 搜索索引。

## 数据与隐私

App 不上传代码、代码库或搜索词，不包含 Telemetry、Analytics、AI、Cloud Sync 或代码执行。单文件导入不修改、不删除、不执行或上传源文件。

App 创建的备份不额外加密。包含敏感代码时，用户需要自行保护代码库、备份和恢复副本。

## 已验证的发布安全

v0.1 候选已完成安装、替换、卸载、重装、代码库移动、索引删除与重建、备份与恢复测试。App Bundle 与用户代码库保持独立。

## 已知限制

- 仅保证 Apple Silicon `arm64`；不保证 Intel Mac。
- 当前仅为个人本地安装，不提供公开下载或 Mac App Store 发布。
- 当前 App 使用 ad hoc 签名，不含 Developer ID 签名或 Apple 公证，也不提供自动更新。
- 不包含 AI、Cloud Sync、语义搜索、文件夹批量导入、Git Import、GitHub Sync 或 VS Code 扩展。
