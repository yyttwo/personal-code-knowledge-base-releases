# 个人代码资产库

一个 Local-first 的 macOS 个人代码资产管理与学习工具，用于收集、整理、搜索、理解和复用自己的代码。

## [⬇️ 下载 v0.3.0](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.3.0)

**当前版本：** v0.3.0 · **系统要求：** Apple Silicon Mac / macOS 11.0+

<p align="center">
  <img src="assets/app-icon.png" alt="个人代码资产库图标" width="160">
</p>

![个人代码资产库主界面](assets/screenshots/01-library.png)

## v0.3.0 新功能

- AI 内容辅助支持本机 Ollama、DeepSeek API 和 Qwen API。
- 新增 AI 对话，可直接使用“设置”中保存的生成模型学习代码知识。
- 智能搜索的 Embedding Provider 可独立选择 Ollama 或 Qwen API。
- Qwen 使用千问 AI 平台 OpenAI-compatible 接口；默认向量模型为 `text-embedding-v4`，维度为 1024。
- API Key 只保存在 macOS 钥匙串，不写入代码库或普通配置文件。
- 生成模型与向量模型设置相互独立；普通搜索不依赖 AI。

## 核心能力

- 把脚本、命令和代码片段保存为结构化资产，管理标题、语言、类型、分类、说明、标签、来源和知识状态。
- 使用 Project 组织资产；同一份资产可以关联多个 Project。
- 使用普通全文搜索、中文多关键词搜索、结构化筛选，以及可选的语义搜索。
- 安全导入单个纯文本代码文件，自动预填标题、语言、正文和来源；不修改、不执行源文件。
- 通过学习中心整理知识完整度、验证历史、复习时间、状态和复用证据。
- 使用 AI 辅助解释代码、完善知识内容，并通过独立的 AI 对话进行学习。
- 使用可恢复的废纸篓，并在永久删除前再次明确确认。
- 创建版本化本地备份，恢复前校验备份并创建恢复副本。
- 正式数据使用普通文件保存；SQLite 仅作为可删除、可重建的搜索索引。

## 设置与 AI

两类 AI 能力默认关闭，并且彼此独立：

- **Generation Provider：** Ollama、DeepSeek 或 Qwen。AI 内容辅助和 AI 对话自动使用这里保存的 Provider 与模型。
- **Embedding Provider：** Ollama 或 Qwen API。只用于语义索引、智能搜索和相关代码推荐。

DeepSeek 默认地址为 `https://api.deepseek.com`。Qwen 默认地址为 `https://maas.qianwenaiapi.com/compatible-mode/v1`。连接云端模型前，需要用户主动启用、填写 API Key 并保存设置；App 会在真正调用前显示相应说明。

使用 Qwen Embedding 时，v0.3.0 默认模型为 `text-embedding-v4`，向量维度为 1024。更换 Embedding Provider 或模型后，需要重新构建语义索引。

API Key 只写入 macOS 钥匙串。删除 App 不一定会自动删除钥匙串项目，可在 App 设置中使用“删除 API Key”，或通过 macOS“钥匙串访问”管理。

## 本机 Ollama

如需所有 AI 推理都留在本机，可选择 Ollama：

- 推荐生成模型：8 GB 内存可尝试 `qwen2.5-coder:3b`，16 GB 可尝试 `qwen2.5-coder:7b`，24 GB 及以上可尝试 `qwen2.5-coder:14b`。
- 推荐向量模型：`embeddinggemma`；轻量备选为 `nomic-embed-text`。
- App 不会自动下载或管理 Ollama 模型。

## 导入、备份与数据

点击“导入代码文件”可一次选择一个纯文本代码文件。App 只读源文件，自动预填可编辑表单；确认保存后，代码库持有独立副本。明显敏感的文件名、富文本、二进制、无效 UTF-8、超过 5 MiB 的文件和不安全符号链接会被拒绝。

删除资产会先移入废纸篓。App 可创建版本化本地备份；备份可能包含完整代码，且不会被 App 额外加密，请保存在受信任的位置。

## 隐私边界

- 代码库、搜索索引、Project、学习记录和备份仍保存在用户选择的本机位置。
- 不包含 Telemetry、Analytics、Cloud Sync、远程崩溃上传或代码执行。
- 使用本机 Ollama 时，AI 请求只发送到用户配置的本机回环地址。
- 使用 DeepSeek 或 Qwen 时，仅在用户明确开启并发起相应 AI 操作后，将完成请求所需的文本发送给所选服务商。
- App 在发送前执行 Secret 风险检查与脱敏保护，但用户仍应避免提交真实凭据和高度敏感代码。
- API Key 只保存在 macOS 钥匙串。

完整说明见 [PRIVACY.md](PRIVACY.md)，操作步骤见 [USER_GUIDE.md](USER_GUIDE.md)。

## 下载与安装

从 [v0.3.0 Release](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.3.0) 下载：

- `personal-code-knowledge-base-v0.3.0-macos-arm64.zip`
- `SHA256SUMS.txt`

ZIP SHA-256：

```text
6f072ac98ca90f226e8a57689a9a8d6d3f5c13a1654a1c161fe4123d44d7a47a
```

完整安装步骤见 [INSTALL_MACOS.md](INSTALL_MACOS.md)。当前版本使用 ad hoc 签名，未使用 Apple Developer ID 签名和公证。若系统阻止首次启动，请在 Finder 中按住 Control 点击 App 并选择“打开”，或前往“系统设置”→“隐私与安全性”使用系统提供的“仍要打开”选项。

## 已知限制

- 仅保证 Apple Silicon（arm64），Intel Mac 暂不保证支持。
- 不提供 Cloud Sync、文件夹批量导入、Git Import、GitHub Sync、VS Code 扩展、代码执行或自动更新。
- 使用 Ollama 需要用户自行安装并运行模型；使用 DeepSeek 或 Qwen 需要用户自己的 API Key、网络连接及相应服务额度。
- 当前采用个人本地安装方式，不提供 Mac App Store 版本，也没有 Developer ID 签名或 Apple 公证。

## 源代码状态

当前不公开核心源代码。本仓库仅用于产品说明、使用文档和正式版本下载。详见 [SOURCE_CODE_NOTICE.md](SOURCE_CODE_NOTICE.md)。

## 安全反馈

公开反馈时，请勿在 GitHub Issue 中粘贴 API Key、Token、密码、私有代码或敏感代码库内容。发现安全或隐私问题时，请先阅读 [SECURITY.md](SECURITY.md)。
