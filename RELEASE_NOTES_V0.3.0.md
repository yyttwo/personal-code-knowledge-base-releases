# 个人代码资产库 v0.3.0

v0.3.0 为 AI Multi-Provider 正式版本。在保留 Local-first 数据边界的基础上，新增 DeepSeek 与 Qwen API，并加入独立的 AI 对话与云端 Embedding 选择。

## 新功能

- Generation Provider 支持 Ollama、DeepSeek 和 Qwen。
- AI 内容辅助与 AI Chat 自动继承“设置”中保存的 Generation Provider 与模型。
- 新增 AI Chat，用于直接与本地或 API 模型对话学习。
- Embedding Provider 独立支持 Ollama 与 Qwen API。
- Qwen 默认使用千问 AI 平台 OpenAI-compatible 地址：`https://maas.qianwenaiapi.com/compatible-mode/v1`。
- Qwen Embedding 默认使用 `text-embedding-v4`，维度为 1024。
- API Key 只保存在 macOS 钥匙串。

## 安全与兼容性

- AI 默认关闭，核心资产管理和普通搜索仍可离线使用。
- Generation 与 Embedding 设置相互独立，不进行 Provider、Endpoint 或模型自动回退。
- 云端请求前保留 Secret 风险检查与脱敏保护。
- 代码库、正式数据、搜索索引和备份仍保存在本机。
- 保持 Apple Silicon（arm64）与 macOS 11.0+ 支持。

## 验证结果

- 完整自动回归：847 PASS。
- macOS 正式 Bundle 构建与发布审计：PASS。
- 正式 ZIP 解压与 SHA-256 校验：PASS。
- Qwen Generation、AI Chat、Qwen Embedding 与语义搜索已完成人工验收。

## 下载文件

- `personal-code-knowledge-base-v0.3.0-macos-arm64.zip`
- `SHA256SUMS.txt`

SHA-256：

```text
6f072ac98ca90f226e8a57689a9a8d6d3f5c13a1654a1c161fe4123d44d7a47a
```

当前版本使用 ad hoc 签名，未进行 Apple Developer ID 签名与公证。安装前请核对 SHA-256，并阅读 [INSTALL_MACOS.md](INSTALL_MACOS.md)。
