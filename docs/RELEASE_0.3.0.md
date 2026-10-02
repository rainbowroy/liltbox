# Liltbox 0.3.0 — Public test release · 公开测试版

2026-10-02 · Build / 构建 11 · GitHub pre-release

[English](#english) · [简体中文](#简体中文)

## English

The first public test release turns recordings or imported audio into an original transcript, readable dialogue, title, description, summary, and local Markdown files. Chinese and English interfaces are included.

**Ad hoc signed only; no Developer ID signature and no Apple notarization.** First launch may be blocked by macOS. Read the [installation guide](INSTALL.md#english) for Apple's single-app “Open Anyway” procedure; keep system security protections enabled.

### Downloads

- `Liltbox-0.3.0-arm64.dmg`: Apple Silicon, macOS 26+, 112,612,991 bytes (107.4 MiB).
- `SHA256SUMS.txt`: SHA-256 verification file.
- `INSTALL.md`: English and Chinese installation, first launch, upgrade, and backup instructions.

[Download from v0.3.0](https://github.com/rainbowroy/liltbox/releases/tag/v0.3.0). Models are downloaded separately in the app (about 2.26 GB). 16 GB RAM is the target minimum, still awaiting device validation.

### Changes

- Clear states for recording, interruption, model waiting, queueing, processing, completion, partial completion, failure, and retry.
- Recover saved recording fragments after interruption; remove stale recovery messages after successful recovery.
- Retry the failed part of a result; organize existing text when the audio copy is no longer available.
- Persistent connection-error notices clear after recovery; safeguards against duplicate submissions and stale page responses.
- Open the results folder after completion; consistent version labels and new bilingual messages.
- Long-text organization and summary-preservation fixes, with the smaller bundled runtime and fixed model configuration.

### Verification and known limitations

The final package has recorded evidence for 192 Python regression checks, two client state/language checks, DMG read-only mounting, bundle comparison, strict ad hoc signature verification, controlled recording recovery, repeated window reopening, and a 90.56-second offline audio-to-Markdown run on an M4 Pro / 24 GB / macOS 26.6.2. These checks do not establish general accuracy or fresh-machine compatibility.

- Recognition errors, repetitive summaries, and incorrectly combined facts remain possible. Review important facts and transcript references. Speaker labels do not verify identity.
- Natural long multi-person meetings, real microphone permission recovery/device switching, 16 GB Macs, and clean-machine first model setup are not fully validated.
- Gatekeeper rejected the unsigned-by-Developer-ID build in the recorded assessment. Browser-downloaded installation with a quarantine flag on a clean Mac remains untested.
- Full VoiceOver, keyboard-only, display scaling, power consumption, and battery checks remain pending.
- Intel Macs and macOS versions older than 26 are outside this test build's target.

Back up before upgrading. Report bugs with the [bug form](https://github.com/rainbowroy/liltbox/issues/new?template=bug-report.yml), request changes with the [feature form](https://github.com/rainbowroy/liltbox/issues/new?template=feature-request.yml), and ask usage questions in [Discussions](https://github.com/rainbowroy/liltbox/discussions). Remove private content from public reports.

## 简体中文

首个公开测试版：录音或导入音频，在本机生成原稿、通顺对话、标题、描述、摘要与 Markdown 文件，提供中英文界面。

**仅有临时签名，未使用 Developer ID，未完成 Apple 公证。** macOS 可能阻止首次启动。请阅读[安装指引](INSTALL.md#简体中文)，按 Apple 官方“仍要打开”步骤仅为此应用添加例外，并保持系统安全保护开启。

### 附件

- `Liltbox-0.3.0-arm64.dmg`：Apple 芯片、macOS 26+，112,612,991 字节（107.4 MiB）。
- `SHA256SUMS.txt`：SHA-256 校验文件。
- `INSTALL.md`：中英文安装、首次打开、升级与备份指引。

[前往 v0.3.0 下载](https://github.com/rainbowroy/liltbox/releases/tag/v0.3.0)。模型在应用内另行下载，完整模型约 2.26 GB。目标最低内存为 16 GB，该配置仍待实机验证。

### 本版变化

- 明确录音、中断、等待模型、排队、整理、完成、部分完成、失败与重试状态。
- 中断后恢复已保存的录音片段，恢复成功清除旧提示。
- 针对失败部分重试；音频副本已清理时仍可整理现有文字。
- 连接错误持续提示，连接恢复后清除；防止重复提交及过期响应覆盖当前页面。
- 完成后可打开结果文件夹，版本与新增中英文提示同步。
- 包含长文本整理和摘要保留修复，沿用精简运行库及固定模型配置。

### 验证与已知限制

最终包已有 192 项 Python 回归、两组客户端状态/语言检查、DMG 只读挂载、包内容对照、临时签名严格校验、受控录音恢复、窗口重复关闭重开，以及 90.56 秒音频离线识别至 Markdown 保存的记录。实测环境为 M4 Pro / 24 GB / macOS 26.6.2；这些检查不能代表普遍内容准确率或新机兼容性。

- 仍可能出现识别错词、摘要重复和信息拼接不当。重要内容请核对录音及原稿引用，说话人标签不代表真实身份确认。
- 自然多人长会议、真实麦克风权限恢复/设备切换、16 GB Mac、全新机器首次模型准备尚未完成完整验收。
- 已有 Gatekeeper 评估拒绝此未使用 Developer ID 的包；浏览器下载后带隔离标记的新机安装仍待验证。
- VoiceOver、纯键盘操作、系统缩放、功率与电池检查尚未完整覆盖。
- Intel Mac 与 macOS 26 以下版本不在本测试包目标范围内。

升级前请备份。问题使用[反馈表单](https://github.com/rainbowroy/liltbox/issues/new?template=bug-report.yml)，建议使用[功能表单](https://github.com/rainbowroy/liltbox/issues/new?template=feature-request.yml)，使用问题可到 [Discussions](https://github.com/rainbowroy/liltbox/discussions)提问。公开反馈前请移除私人内容。
