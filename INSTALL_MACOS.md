# 个人代码资产库 v0.3.0：macOS 安装说明

## 系统要求

- Apple Silicon Mac（arm64）
- macOS 11.0 或更高版本

Intel Mac 暂不保证支持。

## 安装步骤

1. 从 [v0.3.0 Release](https://github.com/yyttwo/personal-code-knowledge-base-releases/releases/tag/v0.3.0) 下载 `personal-code-knowledge-base-v0.3.0-macos-arm64.zip` 和 `SHA256SUMS.txt`。
2. 核对 ZIP 的 SHA-256 与 `SHA256SUMS.txt` 一致。
3. 在 Finder 中双击 ZIP 解压。
4. 将“个人代码资产库.app”拖到“应用程序”文件夹。
5. 在“应用程序”中打开“个人代码资产库”。
6. 第一次启动时，选择“创建新的代码库”并指定一个空文件夹；已有代码库请选择“打开已有代码库”。

代码库是用户自己的数据。建议放在容易找到、管理和备份的位置。删除或替换 App 不会自动删除代码库。

## 首次打开时的 macOS 提示

v0.3.0 使用 ad hoc 签名，没有 Developer ID 签名或 Apple 公证。macOS 因此可能显示“无法验证开发者”或等价提示。

请先确认下载来源和 SHA-256。若 macOS 阻止首次启动，只使用系统提供的图形界面流程：

1. 在 Finder 中按住 Control 点击 App，然后选择“打开”；或
2. 打开“系统设置”→“隐私与安全性”，查看系统提供的“仍要打开”选项。

本文不建议关闭 Gatekeeper、停用系统安全保护或运行命令行绕过操作。

## SHA-256 校验

macOS 终端可使用：

```sh
shasum -a 256 personal-code-knowledge-base-v0.3.0-macos-arm64.zip
```

预期结果：

```text
6f072ac98ca90f226e8a57689a9a8d6d3f5c13a1654a1c161fe4123d44d7a47a
```

若不一致，请停止安装并重新从正式 Release 页面下载。

## 从旧版本升级

1. 在旧版本中创建一次有效备份。
2. 退出旧 App。
3. 用 v0.3.0 的“个人代码资产库.app”替换“应用程序”中的旧版本。
4. 启动 v0.3.0，并打开原来的代码库。
5. 检查资产与 Project；如启用语义搜索，根据设置中的提示重新构建语义索引。

代码库位于用户选择的独立文件夹中，升级、重装或删除 App 不应自动删除代码库。API Key 保存在 macOS 钥匙串中，不属于代码库备份。
