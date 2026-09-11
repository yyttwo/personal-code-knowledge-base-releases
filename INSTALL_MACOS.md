# 个人代码资产库 v0.1.0：macOS 安装说明

## 系统要求

- Apple Silicon Mac（arm64）
- macOS 11.0 或更高版本

Intel Mac 暂不保证支持。

## 安装步骤

1. 下载 `个人代码资产库-v0.1.0-macos-arm64.zip` 和 `SHA256SUMS.txt`。
2. 核对 ZIP 的 SHA-256 与 `SHA256SUMS.txt` 一致。
3. 在 Finder 中双击 ZIP 解压。
4. 将“个人代码资产库.app”拖到“应用程序”文件夹。
5. 在“应用程序”中打开“个人代码资产库”。
6. 第一次启动时，选择“创建新的代码库”并指定一个空文件夹；已有代码库请选择“打开已有代码库”。

Library 是用户自己的数据。建议放在你容易找到、管理和备份的位置。删除或替换 App 不会自动删除 Library。

## 首次打开时的 macOS 提示

v0.1.0 当前使用 ad hoc 签名，没有 Developer ID 签名或 Apple 公证。原因是 Apple Developer Program 成本目前暂缓投入。macOS 因此可能显示“无法验证开发者”或等价提示；这不代表 App 已获得 Apple 验证。

请先确认下载来源和 SHA-256。若 macOS 阻止首次启动，只使用系统提供的图形界面流程：

1. 在 Finder 中按住 Control 点击 App，然后选择“打开”；或
2. 打开“系统设置”→“隐私与安全性”，查看系统提供的“仍要打开”选项。

按照 macOS 显示的说明继续。本文不建议关闭 Gatekeeper、停用系统安全保护或运行命令行绕过操作。

## SHA-256 校验

可使用自己信任的校验工具核对下载文件。macOS 终端的标准命令为：

```sh
shasum -a 256 个人代码资产库-v0.1.0-macos-arm64.zip
```

输出应与 `SHA256SUMS.txt` 中对应文件的值完全一致。若不一致，请停止安装并重新从正式发布页面下载。

## 升级或重装

退出 App 后替换“应用程序”中的 App Bundle。Library 位于你选择的独立文件夹中，升级、重装或删除 App 不应自动删除 Library。操作前仍建议创建有效备份。
