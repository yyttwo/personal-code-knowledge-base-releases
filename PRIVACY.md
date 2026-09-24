# PCKB 0.4.0 Public Preview 隐私说明

个人代码资产库采用 Local-first 设计。代码库、Project、学习记录、普通搜索索引、语义索引和备份保存在用户选择的本机位置。AI 功能默认关闭；用户可以选择完全本机的 Ollama，也可以主动配置 DeepSeek 或 Qwen API。

## 本机处理

App 不包含 Telemetry、Analytics、Cloud Sync、远程 Crash Upload 或代码执行。普通搜索、结构化筛选、Secret 风险提示、重复检查、备份与恢复都在本机完成。

SQLite 只用于可删除、可重建的搜索索引，普通代码库文件是正式数据来源。

## AI Provider 与网络请求

只有用户在“设置”中明确启用 AI、保存 Provider 与模型，并主动执行 AI 操作时，App 才会发起对应请求。

- **Ollama：** 请求发送到用户配置的本机回环地址。
- **DeepSeek：** Generation 与 AI Chat 请求发送到用户配置的 DeepSeek API 地址，默认地址为 `https://api.deepseek.com`。
- **Qwen：** Generation、AI Chat 或 Embedding 请求发送到用户配置的千问 AI 平台地址，默认地址为 `https://maas.qianwenaiapi.com/compatible-mode/v1`。

Generation Provider 与 Embedding Provider 相互独立。AI 内容辅助和 AI Chat 使用保存的 Generation Provider；语义索引与智能搜索使用保存的 Embedding Provider。

使用 DeepSeek 或 Qwen 时，完成当前请求所需的代码或文字会发送给相应第三方服务商，并受其服务条款与隐私政策约束。App 会在发送前执行 Secret 风险检查与脱敏保护，但这不是完整的安全审计；请勿提交真实凭据、私钥或不适合交给第三方的代码。

使用 Qwen API 建立语义索引时，需要把待索引资产的相关文本分段发送到 Qwen Embedding 服务。索引向量及激活状态仍保存在本机。

## API Key

DeepSeek 与 Qwen API Key 只保存在 macOS 钥匙串，不写入代码库、搜索索引、备份或普通配置文件。App 界面不会回显完整 Key。

删除 App 不一定会自动删除钥匙串项目。用户可以先在 App 设置中删除 API Key，或之后通过 macOS“钥匙串访问”管理相应项目。

## App 可以访问哪些文件

App 只围绕用户通过 macOS 系统选择器明确选择的位置工作：

- 当前代码库文件夹；
- 用户主动选择的单个导入文件；
- 用户选择的备份保存位置；
- 用户选择的恢复备份。
- 用户为 App 背景明确选择的本机图片。

App 不自动扫描整个 Home 目录，也不自动扫描项目文件夹。

自定义 App 背景保存在本机，不会发送给 AI Provider。

## 单文件导入与 Sensitive Guardrail

导入时，App 对所选文件进行只读检查和读取，不修改、删除、重命名或执行源文件。保存成功后，代码副本进入用户自己的代码库。

App 会阻止明显的凭据文件名，并对普通代码中看起来像 Secret 的片段给出警告或脱敏保护。这些检查不能保证代码中没有任何 Secret，保存、发送给 AI、分享或备份前仍应由用户检查内容并撤销已经暴露的真实凭据。

## 备份与恢复

本地备份可能包含完整代码、笔记、来源、验证记录、废纸篓和 Project 关系。App 不会对备份额外加密，请将备份保存在受信任的位置，并使用系统磁盘加密、访问控制或离线保管。

## 权限与发布范围

0.4.0 Public Preview 不申请摄像头、麦克风、位置、联系人、日历或屏幕录制权限。文件访问由用户在系统选择器中的明确操作限定。

0.4.0 Public Preview 面向 Apple Silicon Mac 和 macOS 11.0 及以上版本，采用个人本地安装方式。正式下载由本仓库的 GitHub Release 页面提供；目前不提供 Mac App Store 版本、自动更新或 Intel Mac 兼容保证。
