# Install Liltbox 0.3.0 · 安装指引

[English](#english) · [简体中文](#简体中文)

## English

### Before you install

This is a public test build for Apple Silicon Macs running macOS 26 or later. The target is 16 GB RAM or more; testing so far used an M4 Pro / 24 GB / macOS 26.6.2. The DMG is about 113 MB (107.4 MiB). Models are not bundled; the first in-app download needs internet and about 2.26 GB plus room for application data.

**This build is ad hoc signed, not Developer ID signed, and not notarized by Apple.** macOS may block the first launch. A valid ad hoc signature and matching checksum do not constitute Apple review or a guarantee that software is safe. A clean Mac with a browser-downloaded, quarantined copy has not yet been validated.

### Download and install

1. Download `Liltbox-0.3.0-arm64.dmg` from the [official v0.3.0 Release](https://github.com/rainbowroy/liltbox/releases/tag/v0.3.0). The automatically generated “Source code” archives are not installers.
2. Optionally compare its SHA-256 with the attached `SHA256SUMS.txt`. In Terminal, run `shasum -a 256 ~/Downloads/Liltbox-0.3.0-arm64.dmg` (adjust the path if needed). Expected: `5dc4ee7c05e0480f348b6e63a0360f1870cafe9c3e6ee4ba4f5d8d9e3f2b9cdf`.
3. Quit any older Liltbox. Open the DMG and drag `Liltbox.app` into Applications. Eject the disk image, then open Liltbox from Applications.
4. If macOS blocks it because the developer cannot be verified or Apple cannot check it for malicious software, follow the single-app steps below only if you trust this download.

### First launch: Apple's single-app exception

Apple documents this procedure in [Safely open apps on your Mac](https://support.apple.com/en-us/102445):

1. Try opening Liltbox once and dismiss the blocked-launch alert.
2. Open **System Settings → Privacy & Security**, scroll to the security section and find the message about Liltbox.
3. Select **Open Anyway** for Liltbox. Authenticate if macOS asks, then confirm **Open** in the next prompt.

macOS remembers an exception for this app. Keep Gatekeeper, System Integrity Protection (SIP), and other system security protections enabled. No global security change or quarantine-removal command is required by this guide.

If the warning says the app **will damage your computer**, or is **damaged**, stop and report the exact message; do not bypass it. If “Open Anyway” is unavailable, try opening once more and check again; a managed Mac may require your administrator's help. Report unresolved installation issues through the [bug form](https://github.com/rainbowroy/liltbox/issues/new?template=bug-report.yml).

### Prepare models and use the app

Choose your Markdown library folder, download models in **Models & storage**, then import a short non-sensitive audio file to check transcription, organization, and saving. Grant microphone permission when you choose to record. Once the models are ready, processing runs locally and can work offline. Check important facts against the recording; AI output and speaker labels can be wrong.

### Upgrade and backup

Quit Liltbox and back up your whole Markdown library plus `~/Library/Application Support/Huiyi/` before upgrading. Replace the app in Applications; replacing it does not intentionally remove these separately stored files. Keep your backup and previous installer for recovery. Do not delete the data folder merely to reinstall the app. Public feedback should not include private recordings or transcripts.

## 简体中文

### 安装前

本版为公开测试版，目标配置为 Apple 芯片、macOS 26 或更新版本、16 GB 及以上内存。目前实测机器为 M4 Pro / 24 GB / macOS 26.6.2，16 GB 与独立新机仍待验证。DMG 约 113 MB（107.4 MiB），不含模型；首次在应用内下载完整模型约需 2.26 GB，并需为应用数据预留空间。

**本包只有临时签名，未使用 Developer ID 签名，未完成 Apple 公证。** macOS 可能阻止首次启动。临时签名有效、校验值一致均不代表经过 Apple 审核或安全保证；浏览器下载后带隔离标记的新机安装尚未完成验收。

### 下载与安装

1. 从[官方 v0.3.0 Release](https://github.com/rainbowroy/liltbox/releases/tag/v0.3.0)下载 `Liltbox-0.3.0-arm64.dmg`。GitHub 自动生成的“Source code”压缩包不是安装包。
2. 可选：与附件 `SHA256SUMS.txt` 核对 SHA-256。在终端执行 `shasum -a 256 ~/Downloads/Liltbox-0.3.0-arm64.dmg`，如下载位置不同请调整路径。应为 `5dc4ee7c05e0480f348b6e63a0360f1870cafe9c3e6ee4ba4f5d8d9e3f2b9cdf`。
3. 先退出旧版。打开 DMG，将 `Liltbox.app` 拖入“应用程序”，推出磁盘映像，再从“应用程序”打开 Liltbox。
4. 若提示无法验证开发者或 Apple 无法检查恶意软件，仅在你信任下载来源时，按下面的单应用步骤操作。

### 首次打开：Apple 官方单应用例外

依据 Apple 的[在 Mac 上安全地打开 App](https://support.apple.com/zh-cn/102445)：

1. 先尝试打开一次 Liltbox，关闭阻止启动的提示。
2. 打开**系统设置 → 隐私与安全性**，向下找到有关 Liltbox 被阻止的提示。
3. 点击针对 Liltbox 的**仍要打开**；如系统要求，完成身份验证，再在弹窗中确认**打开**。

系统会记住此应用的例外。请保持 Gatekeeper（门禁）、SIP（系统完整性保护）及其他系统安全保护开启；本指引无需全局修改安全设置，也不要求运行移除隔离标记的命令。

如果提示**将损坏你的电脑**或**应用已损坏**，请停止并反馈完整提示，不要绕过。若看不到“仍要打开”，可再尝试打开一次后检查；受管理的 Mac 可能需要管理员协助。仍无法安装，请通过[问题反馈表单](https://github.com/rainbowroy/liltbox/issues/new?template=bug-report.yml)提供版本、机器与提示信息。

### 模型准备与首次使用

选择 Markdown 知识库文件夹，在**模型与保存**下载模型，然后导入一段不含隐私的短音频，检查转写、整理与保存。主动录音时授予麦克风权限。模型准备好后可在本机离线处理。重要事实请对照原始录音核对，AI 内容和说话人标签可能出错。

### 升级与备份

升级前退出应用，备份整个 Markdown 知识库与 `~/Library/Application Support/Huiyi/`，再替换“应用程序”中的 Liltbox。替换应用不会主动删除这些独立存储的数据；请保留备份与旧安装包以便恢复。不要仅为重装而删除数据目录。公开反馈请移除私人录音和原稿。
